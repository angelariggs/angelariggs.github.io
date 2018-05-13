---
layout: post
title:  "BackstopJS Part Deux: Javascript Config and Makefile"
date:   2017-09-11
permalink: /blog/backstopjs-part-deux-javascript-config-and-makefile
comments: true
tags: case-study
---

I’ve [written previously](https://www.metaltoad.com/blog/visual-regression-testing-backstopjs) about my setup for BackstopJS (which I’m still excited to say is the creator-recommended [tutorial](https://www.npmjs.com/package/backstopjs#tutorials-extensions-and-more) for V2 of the package!). Since that article, I’ve switched from JSON to Javascript configuration, and added a Makefile as the main method of running visual regression tests with BackstopJS.

## Iterating the Process

The main motivation behind changing my BackstopJS setup was to simplify the configuration for our development workflow. We typically have three separate environments for each website - dev, staging, and production. The JSON config required three separate configuration files for each environment, which also meant that any changes typically had to be made three times. With a Javascript config and the minimist package, I can add argument variables to a single configuration file, so it’s WAY easier to update URLs or scenarios across the board.

Additionally, Javascript config means that I can add code comments! This is important because for the most part, I don’t run the visual regression tests anymore. My team’s current practice is that the developer in charge of weekly deploys runs the visual regression tests. Being able to include code comments, and the further change of adding a Makefile for easy commands, made it really simple to hand off the responsibility of BackstopJS to the devs on my team.

BackstopJS Setup

The current setup steps haven’t changed much - the main difference is adding the minimist package locally with `npm install minimist` (global install doesn’t seem to work; to be honest, I haven’t really taken the time to troubleshoot it since installing locally works just fine). I created a standalone visual regression repo, so anyone can copy over the templates to a new project. The BackstopJS test directory now looks like this:

```
tests
     |_ backstop
          |_ backstop_data
               |_ casper_scripts
               |_ env_reference
               |_ env_test
               |_ env_html_report
          |_ nodemodules
          |_ .env
          |_ backstop.js
          |_ package-lock.json
          |_ paths.js
          |_ README.md
```

The `backstop_data folder` is a directory that gets created automatically when you run the references and tests, as are the `*_reference`, `*_test`, and `*_html_report` folders within it. The `backstop_data` folder, along with `node_modules`, should get added to your `.gitignore` file - there’s no real value in adding the screenshots to version control, and doing to adds a lot of unnecessary bloat.

The `backstop.js` file is the configuration for BackstopJS, and I’ll be sharing my config a bit further down. It includes variables for the base environment URLs, directory paths for saving screenshots, a choice of how to set the URLs for the screenshots, and general configuration like viewport size and casper flags. The `paths.js` file, which I’ll also be sharing here, is an array of URL paths to use for the screenshots. So if I set my base dev URL as `http://dev-site.com`, then the list of paths would be something like `/about, /contact-us, /case-studies`. Note that the list of paths includes the leading forward slash - you can choose to do it this way, or have an ending forward slash on the base URL. To me, it seemed more natural to have the base URL without the ending slash, but it also means a slight bit more work of having to remember the leading forward slash each time when you create a list of URL paths.

## Pathfile

There isn’t much to the `paths.js` file; it looks something like this:

```
var pathConfig = {};

pathConfig.array = [
  '/', // homepage
  '/company',
  '/blog',
  '/our-work',
  '/careers/open-positions',
  '/contact'
]

module.exports = pathConfig;
```

## Javascript Config

Here’s the fun part! This is my current setup for the BackstopJS config:

```
/* Quick guide to BackstopJS commands

  backstop reference --configPath=backstop.js --pathFile=paths --env=local --refHost=http://site.dev
  backstop test --configPath=backstop.js --pathFile=paths --env=local --testHost=http://site.dev

*/

var args = require('minimist')(process.argv.slice(2)); // grabs the process arguments
var dotenv = require('dotenv').config(); // handles basic auth
var defaultPaths = ['/']; // default path just checks the homepage as a quick smoke test
var scenarios = []; // The array that'll have the URL paths to check

// env argument will capture the environment URL
// if you use one of the options below to pass in, e.g. --env=dev
var environments = {
  'dev': 'http://dev-site.com',
  'staging': 'http://staging-site.com',
  'prod': 'http://www.site.com'
};
var default_environment = 'prod';

// Environments that are being compared
if (!args.env) {
  args.env = default_environment;
}
// if you pass in a bogus environment, it’ll still use the default environment
else if (!environments.hasOwnProperty(args.env)) {
  args.env = default_environment;
}

// Site for reference screenshots
if (!args.refHost) {
  args.refHost = environments[args.env];
}

// Site for test screenshots
if (!args.testHost) {
  args.testHost = environments[args.env];
}

// Directories to save screenshots
var saveDirectories = {
  "bitmaps_reference": "./backstop_data/"+args.env+"_reference",
  "bitmaps_test": "./backstop_data/"+args.env+"_test",
  "html_report": "./backstop_data/"+args.env+"_html_report",
  "ci_report": "./backstop_data/"+args.env+"_ci_report"
};

// Work out which paths to use: an array from a file, a supplied array, or defaults
// We'll be using the array from paths.js
if (args.pathFile) {
  var pathConfig = require('./'+args.pathFile+'.js'); // use paths.js file
  var paths = pathConfig.array;
} else if (args.paths) {
  pathString = args.paths; // pass in a comma-separated list of paths in terminal
  var paths = pathString.split(',');
} else {
  var paths = defaultPaths; // keep with the default of just the homepage
}

// Scenarios are a default part of config for BackstopJS
// Explanations for the sections below are at https://www.npmjs.com/package/backstopjs
for (var k = 0; k < paths.length; k++) {
  scenarios.push (
    {
      "label": paths[k],
      "referenceUrl": args.refHost+paths[k],
      "url": args.testHost+paths[k],
      "hideSelectors": [],
      "removeSelectors": [],
      "selectors": ["document"], // "document" will snapshot the entire page
      "delay": 1000,
      "misMatchThreshold" : 0.1
    }
  );
}

// BackstopJS configuration
module.exports =
{
  "id": "project_"+args.env+"_config",
  "viewports": [
    {
      "name": "desktop",
      "width": 1600,
      "height": 2000
    },
    {
      "name": "mobile",
      "width": 375,
      "height": 2000
    }
  ],
  "scenarios":
    scenarios,
  "paths":
    saveDirectories,
  "casperFlags": ["--ignore-ssl-errors=true", "--ssl-protocol=any"],
  "engine": "phantomjs", // alternate can be slimerjs
  "report": ["browser"],
  "debug": false
};
```

The goal for the Javascript config was to make running visual regression tests as easy as possible - maximum return for minimum effort. For instance, 90% of the time, we’re going to be checking an environment against itself; e.g. running references on staging, deploying changes, and then running tests on staging. So if all of the arguments are going to need parameters that refer to staging, we let the `env` parameter decide the naming for screenshot directories, as well as the URL that gets passed in. And if you don’t pass in any parameter for `env`, the config allows for production URLs and naming to be the default.

## Handling Basic Auth

In addition to updating my approach to configuration, I've also updated my approach to sites with basic auth. I use an npm package called [dotenv](https://www.npmjs.com/package/dotenv). I create a local `.env` file in the root of my `backstop` folder to hold the username and password for the site's basic auth. It looks something like this:

```
# Format for basic auth getting passed in is:
# `username:password`
BASIC_AUTH=uname:pwrd
```

Back in my `backstop.js` file, I would modify the values in my environments section like so:

```
var environments = {
  'dev': ''http://'+process.env.BASIC_AUTH+'\@dev-site.com'', // note we need to escape the @ symbol
  'staging': 'http://staging-site.com',
  'prod': 'http://www.site.com'
};
```

This setup means that we never have to commit our basic auth information to the repo. The project `.gitignore` includes this file; so anyone using BackstopJS on a project would just create a `.env` file locally and fill out the `BASIC_AUTH` value.

## Makefile

The Makefile is what really simplified the visual regression process. The BackstopJS commands can be pretty tedious, and condensing them down to a short Make command was a huge boost to the devs on my team.

```
BACKSTOP_BASE := ./tests/backstop
# ------------------------------------------------------------------------------

# NOTES:
# This Makefile assumes you've gone through the README steps in tests/backstop
# This Makefile is also only for running references and tests against the same environment
# Use the setup in tests/backstop to compare different environments

prod-reference:
  @cd $(BACKSTOP_BASE) && backstop reference --configPath=backstop.js --pathFile=paths --env=prod

prod-test:
  @cd $(BACKSTOP_BASE) && backstop test --configPath=backstop.js --pathFile=paths --env=prod

prod-report:
  @cd $(BACKSTOP_BASE) && backstop openReport --configPath=backstop.js --env=prod

staging-reference:
  @cd $(BACKSTOP_BASE) && backstop reference --configPath=backstop.js --pathFile=paths --env=staging

staging-test:
  @cd $(BACKSTOP_BASE) && backstop test --configPath=backstop.js --pathFile=paths --env=staging

staging-report:
  @cd $(BACKSTOP_BASE) && backstop openReport --configPath=backstop.js --env=staging

dev-reference:
  @cd $(BACKSTOP_BASE) && backstop reference --configPath=backstop.js --pathFile=paths --env=dev

dev-test:
  @cd $(BACKSTOP_BASE) && backstop test --configPath=backstop.js --pathFile=paths --env=dev

dev-report:
  @cd $(BACKSTOP_BASE) && backstop openReport --configPath=backstop.js --env=dev
  ```

Before the Makefile, a command would look something like this: `backstop reference --configPath=backstop.js --pathFile=paths --env=dev`. Now, they just have to run `make prod-reference`!

Note that the Makefile only allows for running references and tests against the same environment. This is because the comparison is done off of the directory naming, e.g. `staging_reference` screenshots are compared to `staging_test` screenshots. So if you needed to pass in two different URLs, you’d need you run the whole command manually, with a specific `env` parameter and `refHost` / `testHost` parameter. Something like: `backstop reference --configPath=backstop.js --pathFile=paths --env=screenshots --refHost=http://site-dev.com`, followed by `backstop test --configPath=backstop.js --pathFile=paths --env=screenshots --testHost=http://site-staging.com`. The `env` argument is how the screenshot directories are named, so you just have to pass in the same parameter for the reference and test commands.

## Benefits

The biggest benefit for me is the value of simplifying process. We do deploys every week, which means we run visual regression tests every week, against multiple sites and multiple environments per site. Switching to the Javascript configuration with minimist, and especially adding a Makefile for commands, vastly simplified our deployment process. Now each project has a single configuration file, and a single file for URL paths to screenshot, instead of three.

Creating argument variables in the config reduces the chance of typos or mistakes. It’s frustratingly easy to forget the `--` for an argument (e.g. `--env`), or to mis-type the `refHost` or `testHost` URL. With the variables and defaults set, it’s one less thing for a developer to worry about.

The Makefile, by far, is the biggest win. It greatly reduces the complexity of the BackstopJS commands, and makes it really easy for devs to run visual regression tests against dev, staging, and production as they deploy up the environment chain each week.

It was fun to revisit my BackstopJS setup and figure out how to make it a simpler process. If you're using BackstopJS and have been looking for a way to simplify your workflow, I hope this post helps! As always, feel free to leave any questions or comments in the comment section below.
