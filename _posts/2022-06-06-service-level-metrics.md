---
layout: post
title:  "Service Level Metrics"
date:   2022-06-06
permalink: /articles/service-level-metrics
comments: true
tags: guest-post metrics series-metrics-categories
---

Last week, Mojtaba taught us about [the 5 categories of engineering metrics]({% post_url 2022-05-10-categories-metrics %}). In this post, he dives deeper into one of these categories: [Service Level Metrics](https://angelariggs.github.io/articles/five-categories-engineering-metrics#4-service-level-metrics).

## Two Sub-categories of Service Level Metrics

When setting up service level metrics and dashboards, it is helpful to distinguish between:

**External facing metrics:** these are metrics that the users of the service would potentially care about. Typical examples are:

- Uptime: % of time over a period that the service is up (and is responsive)
- Latency: statistics (average, median, max, min, standard deviation) on the latency experienced by the calls to the service
- Error rate: % of calls to the service that experience an error 

**Internal facing metrics:** these are metrics that the developers and maintainers of the service would monitor. Typical examples are:

- Service Load: the rate at which a service is being called
- Resource Usage: CPU/Memory and I/O calls the service is making
- (Cloud) Costs: the costs of running the service
- Alert rates: how often a service creates alerts for its maintainers
- Incident statistics: frequency and severity and Mean Time To Recover of the service

Note that teams often have to further slice up these metrics by specific parts of the service in order to get better visibility (e.g. which API or endpoint is experiencing load, or returning error or is using resources etc). Note also that some of the internal facing metrics will overlap with team workload metrics (e.g. alert rate) and team performance metrics (e.g. incident rate and MTTR).

## SLI/SLA/SLO

Teams that gain experience with service level metrics begin to have:

- SLI (Service Level Indicator): a subset of metrics for a service to use as key indicators
- SLA (Service Level Agreement): a minimum value for an SLI that the team agrees with its stakeholders/customers to uphold or internally as baseline or normal or expected level
- SLO (Service Level Objective): a value for an SLI that the team aspires to maintain

Note that typically, SLO is better than SLA such that a team is striving to provide a better service than agreed upon in its SLAs. 

## Using Service Level Metrics

So what are some good practices around service level metrics? Here are some suggestions:

- **Periodic review** of service level metrics in order to:
  - Establish a baseline for each metric (this may serve as SLA)
  - Establish SLOs
  - Look for trends that need investigating
  - Fine-tune alerting thresholds
  - Deprecate metrics that don’t bring insights
  - Suggest addition of missing metrics
- Accompanying, easy to find **documentation** of how each metric is collected as well as the established baselines, SLAs, SLOs and insights that can be derived from these. This documentation also serves as a good reference during incident response and training
- **Balancing service level metrics with the other 4 categories of metrics** in order to avoid narrow optimization (e.g. burning out a team but meeting high SLOs)

## Sample Questions While Reviewing Service Level Metrics

Here are some sample questions while reviewing a service’s metrics:

- What do we expect for the baseline of this metric? What is reasonable?
- What can our customers reasonably expect as a minimum?
- What can we set as our goal?
- How often do we get alerted about this metric? Is it too often? Not often enough? 
- How is the cost of the service changing over time? Is it correlated with the load?
- Is the load on the service proportional to the business load? 
- What service level metrics act as counter balance to this metric? (e.g. cost vs performance)
- What other categories of metrics act as counter balance? (e.g. team workload or team performance or team happiness vs cost and performance of a service)
