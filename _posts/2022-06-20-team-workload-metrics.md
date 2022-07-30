---
layout: post
title:  "Team Workload Metrics: What are they good for?"
date:   2022-06-20
permalink: /articles/team-workload-metrics
comments: true
tags: guest-post metrics series-metrics-categories
---

Out of the [5 category of engineering metrics]({% post_url 2022-05-10-categories-metrics %}), the most used are often [Service Level metrics]({% post_url 2022-06-06-service-level-metrics %}), Team Performance metrics, and Customer metrics. The least used are often Team Workload and Team Happiness/Engagement metrics. 

## What Do We Mean by Team Workload Metrics?

As enumerated in [5 categories of engineering metrics]({% post_url 2022-05-10-categories-metrics %}), examples of Team Workload metrics are:

- % of feature work vs non-feature work
- Support load on the team and its impact on capacity
- Incident load (response and corrective action) on the team
- Bug fixing load on the team and its impact on capacity
- % Tactical vs Strategic work

In short, metrics to track the nature of and source of work for the team can help the team understand its performance in the context of the workload placed on it. 

## Measuring Performance Without Workload

The analogy of using team performance metrics without measuring workload would be to measure the speed of a car without knowing its weight! A truck fully loaded with tonnes of material going at 60km/h is getting more done compared to a very light small car going at 100km/h. 

As such, workload and performance are typically good companion metrics for a team. 

## When Should A Team Measure Workload?

If a team is early in its metric-journey and doesn’t have many of the 5 metric categories covered, it may need to prioritize one category over the other to start. So when should teams prioritize measuring workload metrics over other categories? Here are some signals that the team really needs to start measuring its workload:

- The team feels that they never have time to address long-term problems (that they are in fire-fighting mode all the time)
- The team feels pulled in too many directions (incidents, Production Ready Checklist, bug fixes, support and answering questions, features, etc.)
- The team feels they don’t have time to improve themselves (no time to learn new technology or to learn about other teams)
- The team feels they don’t have enough time to tackle technical debt (see [Episode 6]({% post_url 2022-05-17-metrics-ep6 %}) on using metrics to pay back technical debt)
- The team is unable to improve on its performance metrics and hit its goals
- The team is struggling to have any consistency in its velocity
- The team feels like it covers a very large "surface area" or “too many” services

In these and similar situations, it typically means that the team’s workload is not being measured (and therefore controlled) and any attempt to increase performance or learning or technical debt payback is likely to flounder. 

## How Should A Team Measure Workload?

The way a team measures its workload differs widely based on its nature (charter, mission, customers, stakeholders) as well as its processes so it’s difficult to provide a definitive answer. However, there are some high level tips on measuring workload:

### Make sure there is an ‘in-take’ process 

One of the first rules of improving a team (see [Theory of Constraints](https://www.leanproduction.com/theory-of-constraints)) is to “make work visible”. If the team’s work is not visible, it won’t be accounted for. 

For example, if a team often does substantial work based on Slack DMs or email without much traceability, then there is no hope of measuring the workload. Working with the Product Manager of the team to create and uphold an ‘in-take’ process is a key first step in accounting for the work coming to the team.

### Categorize the work of the team

As soon as a team starts to “make work visible” and measure it, it starts to ask for further break-down of the work. The breakdown could be along the lines of (or a matrix combination of these):

- Source of work: product, support, stakeholder, team itself, adjacent team, regulatory/security
- Component/service: to which service or component is the work most relevant to
- Nature of work: new features, bug fix, exploration and learning, technical debt payback, incident response, corrective action, etc.)

## Size the work

After ‘making work visible’ and categorizing, a team sometimes needs to do some level of sizing in order to compare more accurately. Sometimes it is enough to rely on the number of items, but sizing will help decision making further. Note that sizing doesn’t need to be very exact, and most times a very simple relative sizing (small, medium, large) will provide the insights needed.

It bears mentioning that, as with any metric, a periodic review of metrics is an important aspect of measuring workload.

_**[ Guest post from Mojtaba Hosseini ]**_