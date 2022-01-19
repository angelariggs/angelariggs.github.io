---
layout: post
title:  "Engineering Metrics: 12 Pitfalls"
date:   2022-01-19
permalink: /articles/twelve-pitfalls-engineering-metrics
comments: true
tags: guest-post metrics
---
 
_[Today's article is a guest post from Mojtaba Hosseini, a Director of Engineering at Zapier!]_ The reasons and motivations for having metrics in engineering are well-known and well-documented, but it may suffice to refer to this quote: “What gets measured, gets managed.” However - the full quote is [“What gets measured gets managed — even when it’s pointless to measure and manage it, and even if it harms the purpose of the organisation to do so”](https://medium.com/centre-for-public-impact/what-gets-measured-gets-managed-its-wrong-and-drucker-never-said-it-fe95886d3df6), something this post will also touch on later. The purpose of this is to share some lessons learned and pitfalls along the “metric journey” for an engineering organization.

## Pitfall #1: Measure all the things

Sometimes, due to the enthusiasm for metrics and drive for completeness, a team tries to find all the metrics it could possibly measure. It can get bogged down trying to enumerate them and weigh their pros and cons, thereby never actually starting on the metric journey. 

**What are the symptoms?**
- Trying to come up with all the metrics we could measure
- Large committees to cover all the stakeholders and angles

**Why do we fall for this?**
- Falling in love with the idea of metrics and metrics for metrics sake
- Falling in love with tooling of visualizing metrics
- Trying to balance all metrics (see opposite pitfall #2)

**How can we mitigate it?**
- Focus on outcomes: what problem would metrics solve? What problem are we trying to solve at this point?
- Pick a small number of metrics and start measuring
- Adopt agility: start with some and iterate to add/remove metrics and learn to use some metris before trying to cover all metrics

## Pitfall #2: Measure only 1 category

Some metrics are easier to measure than others (see [Pitfall #3](#pitfall-3-rush-to-automate-and-visualize-first)). Similar to the proverbial [“searching for keys under the street light because everywhere else is dark”](https://en.wikipedia.org/wiki/Streetlight_effect), a team can sometimes only focus on metrics that are easy to measure. 


**What are the symptoms?**
- Focusing on only one category (e.g. SLOs)
- Staying away from tough and uncomfortable metrics
- Focusing only on easy to measure metrics

**Why do we fall for this?**
- We like to measure what is easy, avoiding difficult to measure metrics that may be more valuable 
Exhaustive approach (depth first)

**How can we mitigate it?**
- Focus on outcomes: what problems are you trying to solve? Which metrics would help?
- Recognize the various categories of metrics (e.g. customer-based, service-based, team productivity, team happiness, etc.)
- Track where the current metrics are concentrated and which categories are under-measured

## Pitfall #3: Rush to automate and visualize first

[“Premature optimization is the root of all evil.”](https://wiki.c2.com/?PrematureOptimization) -- Donald Knuth

As engineers we love building the robot, and there can be a propensity to rush to automate collection and visualization of metrics. For some metrics (e.g. a subset of DORA metrics, see below, or some service-level metrics) it is quite easy and indeed convenient to automate collection and visualization. For others (see [Pitfall #2](#pitfall-2-measure-only-1-category)), collection of metrics can be tricky. For these, instead of focusing on their automatic collection, it’s best to start collecting them and then see if the metrics are useful - and only when their collection becomes painful to seek automation. 

**What are the symptoms?**
- Rush to automate collection
- Rush to tools (for collection and visualization)

**Why do we fall for this?**
- Automation is fun
- Visualization is fun
- As engineers we love automation

**How can we mitigate it?**
- Focus on outcomes: what problem are we trying to solve? The tools and scripts are means to that end
- Only automate when the collection becomes too laborious
- Avoid premature optimization

## Pitfall #4: Trying to find the perfect metrics or to measure them perfectly

“Perfect is the enemy of good”. Sometimes a team can begin a search for the metrics to “rule them all”; metrics that perfectly capture all the nuances and aspects of a team and its services. There is no such thing. It is far better to learn to take steps in the ‘metrics journey’ than to have the destination set and decided in advance. Furthermore, usefulness of metrics varies over time (see [Pitfall #9](#pitfall-9-not-reviewing-evolving-and-deprecating-metrics)). Metrics will never fully capture the work we do. Driving to perfectly measure it is futile. 

**What are the symptoms?**
- Agonizing over metrics and whether they are the ‘right’ metrics (before collecting them)
- Delaying collection and use of metrics while debating the merit of metrics

**Why do we fall for this?**
- Seeking perfection

**How can we mitigate it?**
- Adopt agility: the muscle to learn and iterate wins over the muscle to plan everything in advance

## Pitfall #5: Dismissing the DORA metrics

It can be difficult for a team to choose the metrics it should measure. Luckily for engineering organizations, [meticulous, peer-reviewed, scientific-based research into metrics has come up with the 4 DORA metrics, published in the book Accelerate](https://bookshop.org/books/accelerate-the-science-of-lean-software-and-devops-building-and-scaling-high-performing-technology-organizations-9781942788331/9781942788331). These are 4 fairly simple metrics that balance velocity with quality, have been shown to correlate with team performance and market share and to have causation with generative engineering culture. So the question for every team should be: why shouldn’t we be using the DORA metrics?

**What are the symptoms?**
- Long search for engineering metric (see Pitfalls [#1](#pitfall-1-measure-all-the-things), [#2](#pitfall-2-measure-only-1-category), and [#4](#pitfall-4-trying-to-find-the-perfect-metrics-or-to-measure-them-perfectly))
- Dismissing or not being aware of the 4 DORA metrics

**Why do we fall for this?**
- “Not invented here” syndrome
- “Our org is different” syndrome

**How can we mitigate it?**
- Quick read up on the 4 DORA metrics
- Start with at least 2/4 of the metrics (deployment frequency and lead time)

## Pitfall #6: Demanding the same metrics for all teams

Sometimes engineering organizations mandate that all teams measure the same metrics. Although some metrics are indeed applicable to all/most teams (see DORA metrics above), every team is different in the nature of what it does and its customers (e.g. external customer-focused vs internal or development-focused vs operational), or is in a different place in the ‘metric journey’. It is reasonable to ask that all teams consider the same metrics (e.g. DORA metrics) in their journey but it is best to leave teams to find which metrics help them with the outcomes they are after, given their context. 

**What are the symptoms?**
- Trying to compare metrics of one team against another
- Demanding the same visualization tool for metrics across all teams and all levels

**Why do we fall for this?**
- Demanding consistency for consistency’s sake
- Wanting to look at every team the same way (and wanting to assess them against each other, instead of against a standard)

**How can we mitigate it?**
- Focus on outcomes: what problem is each team trying to solve? Metrics should help them with that problem
- Adopt agility: collaboration over process. Teams can collaborate to come up with what is useful instead of having metrics mandated for them
- Make clear that metrics are collected to improve processes, not to encourage competition between teams, so there is no need for them to be comparable across teams

## Pitfall #7: Not considering audience for the metrics

As a team matures in its ‘metrics journey’, it can find itself having many metrics to track. It is helpful to identify stakeholders/audience groups and tailor the collection and visualization of metrics to them. 

Some metrics are most relevant at the executive level, others for directors, and yet others are for the team and its management. The executive level metrics are typically high level (and lack nuance), are fewer and are collected less often. The team level metrics are typically detailed and there are many of them and can be collected far more often.
It’s important to choose the collection and visualization form of the metric for the intended audience

**What are the symptoms?**
- Mixing of high level and team-level metrics on dashboards
- Executives diving into team-level metrics

**Why do we fall for this?**
- It is difficult to put ourselves in others’ shoes. What an executive cares about is at a different level of granularity than what a team cares about. Both are important but they each are produced and consumed differently

**How can we mitigate it?**
- Identify the stakeholder for the metric collected
- Separate team level metrics visualization from higher level metrics visualization

## Pitfall #8: Not using collected metrics

Once a team takes the first (significant) steps in the ‘metrics journey’ and starts to collect metrics, it can sometimes simply stay in the “collection stage”. As a first step, it is good to start collecting but that is not the destination. Using the metrics to help ask questions, to form hypotheses and to help with decision making is the next step. It is a difficult step after collection and that’s why some teams don’t progress past it. 

**What are the symptoms?**
- Lots and lots of metrics dashboards but no further action based on them
- Absence of periodic review of metrics
- Metrics that are not referenced in decisions or in plans
- Not deprecating metrics (see [Pitfall #9](#pitfall-9-not-reviewing-evolving-and-deprecating-metrics))

**Why do we fall for this?**
- Use of metrics to form hypotheses or ask questions is harder than their collection
- Revert to what we are good at (collecting)
- Visualization and collection can be fun (see [Pitfall #3](#pitfall-3-rush-to-automate-and-visualize-first))

**How can we mitigate it?**
- Focus on outcomes: what problems did the team intend to solve with a collection of metrics? What questions were the metrics hoping to answer or help ask?
- Institute a periodic review of metrics (both of what they are supposed to measure and the metrics themselves)
- Ask tough questions (both of what the metrics are supposed to measure and the metrics themselves)

## Pitfall #9: Not reviewing, evolving and deprecating metrics

Just like a team changes and learns along the ‘metric journey’, the metrics it uses can evolve in the value they provide. In other words, some metrics that were valuable early on, may not be valuable later and vice versa. Teams can sometimes hold on to metrics that no longer provide value. 

**What are the symptoms?**
- There is no periodic review of the metrics themselves
- Metrics are not deprecated (and so they can grow in number and never decrease)

**Why do we fall for this?**
- Metrics are cool so we want to have them around (even past their expiry date)
- We don’t use a metric to ask questions (see [Pitfall #8](#pitfall-8-not-using-collected-metrics)) and so don’t know if it’s useful or not

**How can we mitigate it?**
- A periodic review of metrics and their efficacy 
- Focus on outcomes: are these metrics helping us solve problems?

## Pitfall #10: Using metric as purely goals

[“A measure that becomes a goal, fails to be a good measure."](https://en.wikipedia.org/wiki/Goodhart%27s_law) -- Goodhart's Law

Once a team gets to the point of having metrics collected and reviewed, there can be a propensity to purely use metrics to set goals. This can be fraught. The primary purpose of metrics is to help a team ask questions, form hypotheses and to help make decisions. It is sometimes good to set goals based on metrics, but that is not the purpose of metrics and one must be very careful (see [Pitfall #11](#pitfall-11-tying-metric-goals-to-rewards)). 

In the analogy of driving a car: think of metrics as the dashboard in the car. The goal is to drive to a destination, and not to reach a particular speed or engine RPM. One may need to monitor the speedometer for speed and even set a target for a time (e.g. speed limit) but must be aware of Goodhart’s law

**What are the symptoms?**
- Metrics are predominantly used by directors and executives to set goals
- Metrics aren’t used for asking questions and forming hypotheses
- Teams start to be anxious about not meeting goal-based metrics (losing sight of the outcomes)

**Why do we fall for this?**
- Metrics provide an easy convenient mechanism for goal setting (i.e. lazy goal setting)
- Metric-based goals can provide a clear ‘pass/fail’ mechanism

**How can we mitigate it?**
- Be extremely careful and mindful about setting goals based on metrics
- Avoid attaching rewards to meeting a metric-based goal (see [Pitfall #11](#pitfall-11-tying-metric-goals-to-rewards))
- Allow for context and nuance in assessment of teams

## Pitfall #11: Tying metric goals to rewards

Incentivizing metrics heavily leads to gaming them and typically to poor outcomes over time

**What are the symptoms?**
- Team and company incentives tied to specific metric goals

**Why do we fall for this?**
- Mistaken belief that motivation works purely based on reward

**How can we mitigate it?**
- Avoid it

## Where is pitfall 12?!
To make a point that numbers don’t tell the full story, there is no 12th pitfall. 12 is an arbitrary number. What is far more important is the conversation around pitfalls, be they 12 or 2. And that can be the 12th pitfall: forgetting the context and nuance around all numbers. 

**Huge thanks to Mojtaba for writing this really thoughtful post! Have you run into any of the pitfalls he mentions here, or do you have some new and exciting pitfalls to share? How did you solve them?**
