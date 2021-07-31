---
redirect_from: /blog/many-hats-quality-assurance-engineers-tester
layout: post
title:  "The Many Hats of Quality Assurance Engineers: Tester"
date:   2018-04-05
permalink: /articles/many-hats-quality-assurance-engineers-tester
comments: true
tags: quality testing series-many-hats
---

Quality Assurance Engineer is a broad term that can cover a wide variety of roles and responsibilities. It can refer to a more specialized role, like Automation Engineer or Technical Support. It might be used to describe someone responsible for DevOps practices, or the person in charge of Scrum Master duties and feature testing.

At Metal Toad, I’ve had the benefit of creating my role as I go, adding responsibilities and accountability for things that I think are important. On the flip side, I’ve had to create my role. Before I was hired, quality assurance at Metal Toad existed solely as a Tester role on specific high-stakes projects. There were no stable quality assurance processes, no CI/CD, and very little ownership to go along with the responsibilities. As a result, I end up wearing a lot of hats in my day-to-day. The work I do encompasses a variety of roles - Scrum Master, Tester, Architect, DevOps, even a little Product Owner and UX / Design.

So what does that look like? What do I implement as I role-switch?

I’m so glad you asked! Let’s start where my role started, and see what it looks like when I put on my Tester hat.

### Tester

In my capacity as a Tester, one of my main responsibilities is acceptance testing websites and mobile apps for several Agile teams. During projects, I review each Jira ticket against the acceptance criteria, to make sure it matches the stated client and business needs. Part of acceptance testing is exploratory testing - I’ll typically merge the feature branch into our main branch, so I can make sure it integrates with the existing code and functionality without introducing regressions or bugs. I test via different browsers and devices, as both anonymous users and logging in with any roles we've created.

I also have a bit of my UX / Design hat on here. Through acceptance testing, I focus on the user and admin experiences that we’re creating. It’s rarely captured as explicit acceptance criteria, but it’s one of the most important parts of our work. It’s my goal to give our clients a simple, intuitive admin experience. When I’m reviewing features, I try to look at it from our clients’ point of view - someone who may not have experience updating and maintaining a website or app. Something that may be obvious to an engineer could be - and often is - confusing or unintuitive to someone acting in a site administrator role.

When I think a ticket needs rework, I try to explore root causes for the bug or regression, or make a specific recommendation for improvement - I don’t want to just throw it back over the wall. Clear, empathetic communication always plays a part, but especially here. It’s easy to take QA feedback personally, so I try to make my feedback as collaborative as possible. My goal in giving feedback or asking for changes is the same as everyone’s on the team - to create the best version of our product.

I also do accessibility testing over the life cycle of each project. The tech industry is becoming more aware of accessibility needs - and the importance of meeting those needs as we create new products and apps, instead of being an afterthought (or worse, totally ignored). Currently, I use a product called [Pa11y Dashboard](https://github.com/pa11y/pa11y-dashboard) for my accessibility testing, and you can check out my setup [here](https://github.com/angelariggs/pa11y-setup) if you’re interested! The dashboard lets us track accessibility issues over time, which gives us something meaningful to show our clients. I capture the accessibility errors in a Google Sheet, and use it to create tickets in Jira that we can bring into our sprints.

Occasionally, we’ll have a bug or regression that calls for a deeper dive. When that happens, I’ll take the time to write up a formal test plan, create and implement test cases, and report my findings with recommendations for improvement or future-proofing. In the most recent instance of this, our VP of Technology asked for some extra care on a feature that had been a continuing problem for our clients. I started by meeting with the clients to reassure them that I was prioritizing this issue, and that we would end up with an improved feature that functioned as expected. I created and carried out about 25-30 testing scenarios, wrote up a summary of my findings, and met with one of our engineers to talk about recommendations for improvement. We reviewed the results of my testing, and he re-wrote the feature to align with the assumed and needed functionality. This testing and feature change wrapped up with a client meeting, where I did a demo of the revised feature. I also took the time to summarize the process behind exploring, troubleshooting, and updating the feature - one of the desired outcomes of all this was to re-establish trust and confidence in Metal Toad and our team, and we wanted to make sure they felt taken care of.

The need for building that trust and confidence is a large part of why we offer Quality Assurance practices in the first place. By including QA practices throughout our software development life cycles, we show our clients that we take the quality of our work seriously, and ensure at each step that we’re producing the type of work we’re proud to deliver. And we reassure ourselves - from engineers and product owners all the way up to our C-suite executives - that we have checks in place to prevent and catch bugs, regressions, or otherwise sub-par code. We give *ourselves* the ability to trust in our code and our processes, to have confidence in the products we’re creating.

**What other hats do I wear as a QA Engineer? Read on for more insight into what it looks like when I wear my [DevOps](http://angelariggs.github.io/blog/many-hats-quality-assurance-engineers-devops) hat!**