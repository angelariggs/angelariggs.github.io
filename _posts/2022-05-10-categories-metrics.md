---
layout: post
title:  "The 5 Categories of Engineering Metrics"
date:   2022-05-10
permalink: /articles/five-categories-engineering-metrics
comments: true
tags: guest-post metrics series-metrics-categories
---

As [Mojtaba Hosseini helps guide Zapier]({% post_url 2022-03-30-metricsep1 %}) toward being a more data- and metrics-driven engineering organization, and as teams continue to add and use metrics, he finds that they sometimes come across this question: _What other metrics should I be looking out for and using?_ 

Let's join Mojtaba in another guest series as he explores the 5 categories of engineering metrics that can help teams diversify and balance their metrics!

But first, an analogy...

## An Analogy

Think of a car’s main dashboard:

<div id="blog-photo">
	<img src="https://cdn.zappy.app/11e732ad5dfd5a2172935a9fec29785f.png" alt="" width="500" height="300">
</div>

There are many indicators and dials, each helping the driver in different ways:

- **Speed and performance:** how fast is the car going? How hard is the engine working?
- **Maintenance:** engine health, oil and battery health, gasoline level, engine temperature.
- **Status:** doors, trunk, hood open/close, lights on/off, indicators on/off, hand-brake on/off.

The more complex the car, the more dials and dashboards within these categories. If a driver only has access to one category, they can damage the car (or worse).

## The 5 Categories of Engineering Metrics

There are arguably 5 categories of metrics that engineering teams can use. 

### 1. Customer Metrics

These metrics are focused on gauging how the team’s customers are doing. Metrics in this category include:

- Customer Net Promoter Scores (NPS)
- [Product HEART metrics](https://www.productplan.com/glossary/heart-framework/): Happiness, Engagement, Adoption, Retention, Task Success
- Service Level Indicators (SLI) around how quickly we respond to customer queries

<div id="blog-photo">
	<img src="https://cdn.zappy.app/b2d35ad4ca39243465da769d0754ddd9.png" alt="" width="400" height="300">
</div>

These are often considered some of the most important metrics for a team since they are concerned with the team’s customers. However, these metrics can be lagging indicators and may not give a team enough insight into why customers are happy (or not). 

### 2. Team Workload Metrics

Some teams find it useful to measure the workload of the team and gain insight into the various categories of workload. For example:

- % of feature work vs non-feature work
- Support load on the team and its impact on capacity
- Bug-fixing load on the team and its impact on capacity
- % Tactical vs Strategic work

<div id="blog-photo">
	<img src="https://cdn.zappy.app/d5639d228ab248ad9ad0bd7bc57ea712.png" alt="" width="400" height="300">
</div>

These metrics can help teams understand and articulate their pain-points, and can even sometimes be tied to customer metrics. They can also sometimes reveal issues and bottlenecks outside of the team that impact the workload placed on the team. 

### 3. Team Performance Metrics

If Team Workload metrics measure the input of work into a team, Team Performance metrics aim to see how well the team is dealing with their workload. For example:

- Cycle Time and Throughput and Work-In-Progress (WIP) size: how a team works through its workload
- 4 DORA metrics: how quickly and often a team deploys to production and the quality of those deployments
- Team Velocity: the average velocity of completing stories

<div id="blog-photo">
	<img src="https://cdn.zappy.app/f4d23e2a1750ac50e35ba2f9336f3f29.png" alt="" width="400" height="300">
</div>

[These metrics are typically the ones most in danger of being incorrectly used by management - and at worst weaponized]({% post_url 2022-01-18-pitfalls-of-engineering-metrics %}). When used properly, they are great companion metrics to Team Workload and Customer Metrics.

### 4. Service Level Metrics

Software teams can also measure the health of the services they own. For example:

- Resource usage (CPU/Memory): how much the service uses resources, typically viewed over time
- (Cloud) cost: the cost of resources (typically broken down further) and typically viewed over time
- Service uptime: the % of time a service is up
- Service error rates: how often a service errors out or times out

See [this article](https://aws.amazon.com/builders-library/building-dashboards-for-operational-visibility/) from Amazon on the various levels of service metrics and creating dashboards for operational visibility. 

Note that for some teams, these service metrics have direct or indirect relationship to customer metrics - and may even _be_ customer metrics when customers are the direct user of a service.

### 5. Team Happiness/Engagement

Another category of metrics revolves around the team’s engagement and happiness. Some examples include:
- Employee engagement surveys
- High Functioning team surveys
- Ambiguity of workload and strategy surveys

<div id="blog-photo">
	<img src="https://cdn.zappy.app/ddbe4496d05302515c3a82e60dfd8e8b.png" alt="" width="450" height="300">
</div>

These metrics aim to balance some of the performance, workload, and customer metrics with team engagement. For example, engaged teams often are high-performing teams. 

## How to Use the 5 Categories

Tune in to the next post to get ideas on how you use these five categories of metrics to balance each other!
