---
redirect_from: /blog/beginners-guide-test-automation
layout: post
title:  "A Beginner's Guide to Test Automation"
date:   2019-02-20
permalink: /articles/beginners-guide-test-automation
comments: true
tags: automation cross-post
---

If you’re new to automated testing, you’re probably starting off with a lot of questions: How do I know which tests to automate? Why is automated testing useful for me and my team? How do I choose a tool or framework? The options for automated testing are wide open, and you may feel overwhelmed.

I want to help turn some of your “unknown unknowns” into “known unknowns”! The goal of automation is to create anti-fragile tests that are easy to understand, maintain, and hand off. I’ll get you closer to that goal by answering some questions that many of us had when we first started with automated testing, and I’ll also give you some additional questions that are good to consider.

## Introducing Automation

Once you’ve decided to start automating, the next step is probably to introduce the idea to your team. Automation may not be the only work you’re doing, but it is going to be a lot of work! Trying to squeeze it in between your regular work means it probably won’t end up getting completed. In order to really succeed with automation work, you’ll need to get buy-in from the team to dedicate your time and effort toward it.

I started the conversation by explaining why automation is important and how it’s useful to our work. One of the things I try to establish with engineering teams is the idea that no single type of testing should bear the responsibility for quality. Different methods serve different purposes, and they are all part of the whole.

Automation can be useful for testing lower-risk functionality, which frees you up to focus on higher-risk, high-priority, or more complicated functionality. On the other hand, maybe you have some high-risk items that will need to be tested regularly, and creating automated testing for those items would create more confidence in them.

Our biggest risk as a team was transitioning from our existing monolith repository to a new microservices codebase. Offering to create automated regression tests had a lot of support from the team: engineers benefited because they could have higher confidence that their work wasn’t breaking anything, and our product owner had confidence that any breaking changes would be quickly found before releasing to production. It also benefited me, since I was now going to automate all the repetitive testing scenarios!

When you’re proposing automation, consider what the team needs are, then determine how you can include automation in a way that balances those needs. You’re more likely to get support if the benefits are more easily felt, so ask your product owner or developers what’s important to them. Overall, the goal is to make sure your automation efforts are supported by the team so you can focus on creating tests that support the team in turn.

## Choosing a Tool

One of the most common questions when starting automated testing is “What tool or framework should I use?” The answer, as with many things, is “It depends.” There are several questions you’ll want to consider: 

- Who is writing the automated tests?
- What kinds of tests are you running?
- For paid frameworks, does your department have a budget?
- If the tool is open source, is there good documentation and community support?

If the developers are writing unit tests, they’re probably going to write them in the same language as the rest of the codebase. If they’re using PHP, they might look at PHPUnit; for JavaScript, they might check out Jest. The goal here is really to make it as easy as possible for developers to incorporate testing in their regular development workflow. So instead of being prescriptive about the framework they use for testing, the focus should be on helping them find the right tool for their needs.

When I’m considering automation tools, my main considerations are usually choosing between code-based and codeless, and open source versus paid.

In my role as a QA engineer, I’ve typically been responsible for QA and testing on multiple engineering teams at a time. It’s not feasible that I’d be solely responsible for automation on all of the teams, so I approach automation with the idea that the developers will also be contributing to these tests. That leads me to choose code-based frameworks, because it follows a pattern of working that the developers are familiar with, and it keeps the work in the same repo as the codebase. A codeless solution would mean learning a totally new tool, another login to keep track of, and testing that’s a bit removed from the codebase they’re already in every day. 

When considering open source versus paid, I’ve often run into budgetary restrictions that cause me to choose open source. In comparing open source options, I consider how actively the tool is maintained—are there lots of open, unanswered issues and pull requests? When was the codebase last updated? I look at the documentation and see how easy it is to install and start writing my first tests. If I can, I ask other testers if they’ve had experience with the tool and what they thought of it.

Keep in mind that your needs and situation may differ from mine. This information isn’t intended to tell you what your answers should be, but to give you things to think about. The goal is to consider what you need from an automation tool and understand how to sift through the options to figure out what tool meets your needs.

## Writing Your First Test

When I started writing my regression tests, I was focused on getting the tests to pass—that’s the goal, right? I’d get one part of the user journey passing, and then start writing tests for the next bit. It was exciting to see the growing list of green checks every time I ran the tests. Eventually, I had our three main user journeys tested and passing. I was giddy with the power of automation!

I also had an enormous test file.

There are a couple of drawbacks to this. First, all the user journeys were being tested as a single test flow. So if something failed along the way, all of the subsequent tests were useless, because they would also now fail. It would also be much harder to update this file if something changed, because I’d have to go through every single step in all of the user journeys to see what else might be affected by the change. In short, I had created a fragile test.

To improve my automation suite and make it more resilient, I broke out the user journey into smaller chunks and placed those chunks into their own test files. It was a fairly tedious process, as I now had to rerun every test to make sure I hadn’t broken it in the extraction.

In my initial excitement over automating my tests, I’d also committed the basic authentication for our staging site. I figured I’d come back to the credentials with a proper setup later, because my focus was writing the tests and having them pass. Fortunately, I realized what I had done before I pushed my commits, and I was able to do some Git maneuvering to remove the committed credentials.

This experience, tedious as it was, taught me the importance of outlining my tests before I start writing them. An outline gives me a better estimate of the time and effort that creating the tests might take, and it can help me prioritize which are most important to complete if my time is more limited. I also realized that dealing with credentials securely should be one of the first tasks to go in the outline.

It’s important not to get caught up in the idea that you need to write tests that pass. Focus instead on creating your tests so that they’re easy to run and maintain and are as secure and anti-fragile as possible.

## Best Practices

Security and test structure are just a couple of things you’ll need to think about as you’re writing automated tests. Here are some of the questions I didn’t know I needed to ask when I first started:

- Do the tests depend on each other for data?
- Are failures easily understood from the logs?
- How easy would it be for someone else to update your tests?

Ideally, your tests can be run in isolation from each other. If they depend on other tests for their data, a failure in one test can have a cascading effect. Whether you’re using fixture data to test at the unit or service level, or testing a user journey at the UI level, make sure the tests can be run independently. Not only does this help you create anti-fragile tests, it makes it much easier to pinpoint failures when they do occur.

And you will have failures, but that doesn’t mean you wrote a bad test. On the contrary, this means you wrote a useful test that caught a failure! Once a test has failed, you need to investigate why, and there are ways to make this easier on yourself.

Don’t just stick to the happy paths as you’re writing tests—make sure you’re including error messaging. If your test doesn’t have an error message, a failure only tells you that the test didn’t succeed; it doesn’t tell you why it wasn’t successful. Having a clear error message helps you narrow down where the failure occurred. For instance, throwing an error like “Service didn’t return the expected 200 response” is much clearer than “It didn’t work” or a silent failure.

By the same token, your test descriptions and test steps should be written for clarity. Test output acts as a log, so you should write your automation with that in mind. Consider a description like “It 404s” versus “Sends a 404 if the file does not exist.” The first one is generic, providing no information beyond expecting a 404. The second example is much more informative, because it tells me that I’m checking for an expected 404 response when the test doesn’t find a file.

Having clear steps and error messages also makes it much easier for the test suite to be maintained and updated, whether it’s by you or someone else. Once the automation is in place, it’s likely that other people on the team will start contributing as well. If you’ve already established a good pattern of writing tests, it’ll be relatively simple for someone else to pick up where you left off.

## Go Forth and Automate

The important thing to remember is that it’s not about the One Right Answer to anything. It’s about understanding the questions you’ll need to ask, and how to find the answers that will work for you and your team. Getting support for automation work, creating a practical infrastructure, and choosing the right tool for your needs will give you an excellent foundation for beginning your automation endeavors.

So go forth and automate with confidence. You may not have all the answers yet, but having the questions is a really good start!

*Originally published on [Techwell's StickyMinds](https://www.stickyminds.com/article/beginners-guide-test-automation)*