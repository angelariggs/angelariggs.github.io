---
redirect_from: /blog/creating-culture-quality
layout: post
title:  "Creating a Culture of Quality"
date:   2018-10-14
permalink: /articles/creating-culture-quality
comments: true
---

*[ Originally published on [TechBeacon](https://techbeacon.com/how-i-created-culture-quality) ]*

Quality assurance is often assumed to be a narrow slice of work — something that happens in between writing code and getting it deployed to production. 

But software quality doesn't happen at just one point in time, and it encompasses more than your testing tools or your bug count. QA is a mindset, and it's a culture that your team — and your entire company — should be involved in.

During my tenure at a previous job, I helped implement this culture shift across departments and teams. It was not without challenges, my experiences and lessons learned should help you understand the importance of this culture, and how to create it at your company. 

## Creating the culture

A culture of QA is based on the premise that no single tool, test, or person can guarantee quality. For quality to be a solid part of the company culture, everyone needs to support and contribute to it—from management and sales teams to developers, architects, and product managers.

As with any new project, I had some challenges to solve when I first started this culture shift at my company. Change management and onboarding were two of the big ones, which is pretty common for instituting any kind of extended change.

### Thoughtful change management

Introducing a culture of QA means new workflows, processes, and tools—that's a lot of change. The important thing to remember is that change is an emotional process for people, so empathetic and thoughtful change management is crucial to success.

People like to know what's coming, so it's important to give them some transition time. Most of our process and tool changes started on a single project, with a period of feedback before we did a wider rollout.

For instance, one goal toward improving our culture of QA was introducing centralized static code analysis. We started with one project on one team, and spent about a month getting feedback and refining the process before rolling it out to another team.

> It's like writing an essay: Tell them what you’re going to tell them, tell them, and tell them what you told them.

Don’t just drop a change in their laps and walk away; raise the topic early and often so your team members can ask questions. Make sure they feel informed and that they're comfortable with the upcoming tool or process change. People like being kept in the loop, and well-informed people can make better decisions.

When you’re having these conversations, also remember to include the "why." Why are we solving this problem? Why are we choosing this solution? Why will this iteration make it better?

Talking about the "why" with your team adds context and helps make sure everyone is on the same page. When your team members are a consistent part of the conversation, they'll be more invested in the decisions being made. That means they'll be an active part of the culture shift, which increases your likelihood of success.

### Onboarding: A crucial part of culture change

Onboarding is the second barrier to successfully creating your culture of QA. Just like change management, onboarding can be really difficult to execute well. It includes making sure people know what they need to know, when they need to know it; whom to ask when they have a question; and where information is stored. It's a lot to keep up with!

Find ways to make the onboarding process easier for your team. If you can reduce the churn that goes along with messy onboarding, it's much easier for the team to focus on the actual changes.

A makefile is a great way to do this. It lets you create simpler commands for running and setting up new tools, so your developers have one less thing to worry about. When I introduced a suite of end-to-end tests to one of my engineering teams, the initial command for a full test run ended up looking like this:

```
pkill -f selenium-standalone; selenium-standalone start;
sleep 2s && codeceptjs run --grep "admin-workflow" --profile https://website.com
--reporter mochawesome --reporter-options reportDir=./output,reportFilename=desktop-admin.html;
pkill -f selenium-standalone
```

Understandably, there was a lot of resistance to using these tests. Yes, the tool itself and the actual tests were useful, but the overhead of using them in daily work was a big blocker—and a tool that people won't use is ultimately useless.

With a makefile, that initial command became this:

`make desktop-admin`

The new command took care of stopping and starting the Selenium server, and drastically reduced the chance of a typo from the long command causing the tests to fail. Guess which one the team preferred?

Another way to ease the process of onboarding is to practice "I do, we do, you do." I learned this method when I was a teacher, and it works just as well for adults as it does for fifth-graders. 

Start by doing a demo for your team; run through the setup, and write and execute a test. Then let one of the developers guide you through writing another test, or let the developer guide while someone else drives. This helps you make sure your team members can understand and use their tools effectively before you hand control over for them to continue on their own.

## Defining the culture - Roles and responsibilities

### Management

At the top level, you need buy-in from management. You can't create a culture of QA from the top-down, but management does need to support it. They can influence the conversation around this culture shift, and their backing gives you credibility in the company.

For me, that support came in the form of quarterly and yearly objectives and key reports that were geared toward setting a foundation of quality practices throughout the company. Instead of just myself or a handful of people setting goals and doing the work, our management team set the goals. So, from the beginning, there was an expectation of shared responsibility for implementing a culture of QA.

### The sales team's role

If you have a sales team, include it in this culture shift. Salespeople are in a perfect position to seed the ground early for conversations about culture. At my company, I worked with our sales team to create collateral materials on the process and benefits of quality.

That collateral was used for responding to requests for proposals and for sending data sheets to prospective clients. We even included it in contracts to describe the expectations of service.

The type of collateral that works for you and your company may differ, so talk with your salespeople to see what they need from you in order to start these conversations with customers and other stakeholders.

### Working with product managers

Product managers also contribute to a culture of QA via their relationship with stakeholders. They’re in a great position to advocate for the benefits of including quality practices throughout the project—in other words, why quality is worth paying for. If stakeholders don’t hear about the importance of quality until the project has already started, they’ll feel as if paying for quality means sacrificing their minimum viable product.

At my company, a tester's time used to be budgeted at 0% to 10% in a project. One of the changes that our product managers made was to increase that to a minimum of 30% for every sprint in the project, which was then included in the overall cost that we gave to the stakeholder.

This meant that my time and my work had more value to the company, and the role of quality was raised to the stakeholders early in the process.

Invisible work can’t be valued, so work with your product manager to find ways to elevate the visibility of quality within the projects. There’s no one-size-fits-all solution, but there are solutions—for example, doing consistent billing for testers' time or creating specific testing tickets when testers scope out the project with stakeholders. Lean on your product managers' expertise and stakeholder knowledge to find the solution that works for your team.

### Developers' roles

Of course, developers also contribute to a culture of QA. When it comes to building the product, I know that test-driven development (TDD) is not always possible; timelines may be short, or there may be a lot of legacy code. However, TDD can always be supported by developers and team leads, and setting team goals to increase code coverage with each personal record is a great way to encourage it.

Developers can also contribute through code reviews. When developers review their colleagues' work, it allows more people to be familiar with what's being built, which means more developers will have a broader understanding of the product. Code reviews also encourage better communication, but it takes practice to give—and receive—useful code reviews. I recommend Vaheidi Joshi’s "Better Code Reviews" and Angie Jones' "10 Commandments of Code Reviews" as resources for building that skill.

These roles and responsibilities are a good representation of how we implemented a culture of QA, but it's not the only way for that culture to exist.

Ultimately, a good culture of QA is flexible, with the ability to meet changing requirements.

## Benefiting from the culture

When you create this culture shift, you also create a way for people to collaborate across teams and departments, with everyone working toward the same goal. In my organization, our culture of QA helped build a foundation of communication and a shared understanding among verticals about the importance of quality.

With a rise in quality comes a rise in confidence, which improves team cohesiveness and overall morale. At the core, a culture of quality assurance enhances your ability to build and launch high-quality products that meet your stakeholders’ needs — and that's a culture that benefits everyone.


*Interested in learning more about creating a culture of quality? Join Angela for her talk at TestBash San Francisco, which takes place November 8-9, 2018. She'll take you on a deeper dive into the details of creating this culture, and how your company can experience long-term benefits it.*
