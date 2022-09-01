---
layout: post
title:  "An Analogy for Product-Engineering Metrics"
date:   2022-08-01
permalink: /articles/analogy-product-engineering-metrics
comments: true
tags: guest-post metrics
---

Mojtaba brings us another great guest post about using real estate investment as an analogy for thinking about product engineering metrics!

I've been thinking about high level build org metrics for some time now. I like analogies and so thinking about it in terms of a real-estate investment helped clarify in my mind the differences between 3 separate things.

I imagined myself as an investor in a house I intend to use for rental income (and for equity growth). I pay $2000/month to have the house both maintained and new additions added (examples: new deck, new garage, new shed, etc.). Starting next year, I want to double my investment and pay $4000/month and so I expect that the rate and significance of the new additions should go up (maybe not twice as much because each addition also brings with it increase in maintenance) but it should go up nonetheless. So then there are 3 separate questions I have:

1. For twice the input investment, how many more (and of what size) additional things do I get added to the house?
1. What % of the total investment is used for maintenance, and what % for additional things?
1. What is the value of the house? (or the value of the monthly return on the house?)


These are 3 **separate** questions, each helping with different types of decisions.

1. Question 1 is about the impact of increased investment on the additions and captures how effective the additional investment is being put to use.
1. Question 2 is the breakdown of how the investment is used and doesn’t cover how effectively (question 1 deals with effectiveness).
1. Question 3 deals with the ultimate goal of increasing value. There is no guarantee that adding an addition (e.g. a pool) adds value, though it’s a lot of work and may take a lot of investment. 

Real-estate market may also change the value of the house independently of the new additions and the maintenance state. 

## Applying To Build Org

Now if I look at this from a company’s founders/board perspective, I can ask the same question about the Build Org of a company (its product-design-engineering):

1. For the additional growth in headcount in build org, how much and how many more additional new things are we building and delivering to customers?
1. What % of the total investment in build org is going to maintenance of the current product vs % used to build new things?
1. What is the actual monetary value this delivers back to Zapier? (and its impact on the overall evaluation of Zapier)

These lead to 3 sets of metrics:

1. New customer-value delivery per time period (e.g. quarter)
1. % of effort for maintenance vs % of effort dedicated for new value delivery (there may be 3rd category: foundational work that is to enable more/better future delivery of value)
1. The actual ARR and revenue coming to Zapier (and the corresponding valuation)

There is an interesting interplay between these 3:

- The actual ARR and revenue and valuation are lagging indicators relative to the new value delivery.
- The ARR and valuation may be impacted by many other internal or external factors (market conditions, marketing, sales).
- New value delivery is more of an [outcome metric]({% post_url 2022-05-10-categories-metrics %}) compared to % of effort.
- % effort is an activity metric (and a [workload metric]({% post_url 2022-06-20-team-workload-metrics %}) from the [5 categories of metrics]({% post_url 2022-05-10-categories-metrics %})).
- The % of effort for maintenance may indirectly help with addition of new value.
