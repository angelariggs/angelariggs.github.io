---
layout: post
title:  "Monitorama!"
date:   2017-05-26
permalink: /blog/monitorama
comments: true
---

I just attended Monitorama 2017 in Portland, and I wanted to talk about my experience! I think it’s useful for me as a brain-dump and reflection about what I took away from the talks, but it’s also nice for other people to have some more insight into what the conference is about.

# Why Monitorama

One of our developers takes the time to stub out a yearly conference schedule, and that list was my first knowledge of Monitorama. It seemed like a pretty cool conference, and timely for me — as a QA engineer, my role has some structure to it, but there’s also a lot of room for adding in skills and responsibilities as I go along. Monitorama seemed like a really interesting opportunity to dive into the tools and conversations and goals happening with Ops/SRE people, and to learn more about the intersection of QA and Ops.

At the time, however, the cost of the conference was a bit more than I was able to pay, so I made the decision to check out the livestreams or videos later. But! Two days before the conference, I saw Monitorama re-tweet someone who couldn’t make the conference and was giving away the ticket. I replied with my interest, crossing my fingers but not expecting to get it, and went off on a hike in Leavenworth, WA. A few hours later, I drove back into cell service, and got a very pleasant surprise when I checked my phone — I was going to Monitorama! (Huge kudos, by the way, for making it so simple to reassign a ticket!)

# The Conference

The presenters at Monitorama held a variety of titles and experiences: engineers and engineer managers who work on ops and support teams, performance, infrastructure, cloud, visibility, data science, observability, build and release. The schedule showed talks about new tools, enterprise processes, debugging, and monitoring of all kinds. During the talks, a common thread began to appear even in the morning of Day 1, and continued throughout the conference: an underlying theme of observability versus monitoring. People with more experience in the field may have a better (or different) understanding around the difference between the two, but my take-way was this:

Monitoring is a final, separate step in a project’s development life cycle. The website or product is thrown over a wall to the Ops team, and they use whatever parameters happen to exist for measuring and monitoring.

Observability is baked into the active development cycle, and developers include thoughtful metrics and information for Ops to use. There’s collaboration and communication as developers and ops teams work together to figure out what is useful to be monitored.

Some of the talks went deep into tools and techniques for those tools, which tended to be a bit over my head. But many of the talks were about how the engineer solved a problem with observability or monitoring, and I thoroughly enjoyed those.

One of my favorite talks came from Amy Nguyen, an infrastructure engineer at Pinterest. Her presentation was UX Design and Education for Effective Monitoring Tools. The basis of her talk was the realization that her job wasn’t just to build and maintain the monitoring tools, but also ensuring that those tools were able to be used correctly and effectively by the rest of the engineering organization. She argued that we should all care about user experience: good UX prevents misunderstandings, increases developer velocity, and allows for data democracy. I particularly like that last reason — it means that the infrastructure team, or the tools they implement, don’t limit the data that engineers can discover. I get a kick out of playing around with various tools to see what they do, and what I can do with them; but also sometimes a situation will come up where I want to monitor something weird. Having a good data democracy means that the tools give me the freedom to do that.

A couple of quotes that I took away from Amy:

_“If our tools suck, it’s all people have. And we can do better.”_

_“[Your tools should] make it hard [for users] to do the wrong thing.”_

_“Make it easy to try things without fear.”_

_“The fastest way to become a 10x engineer is to help 10 other engineers do their jobs better.”_

(That last one is just someone on the internet, probably. But maybe Wayne Gretzky. Who can really say for sure?)

# Takeaways

My purpose in wanting to attend Monitorama was to expand my knowledge base, to understand more about what my DevOps team does, and to figure out how our jobs intersect. I came away from Monitorama wanting to scoot into our DevOps desk pod and ask them all of the questions about what they’re doing and how they’re doing it and how can I do those things and what would they change about their tools... It definitely whetted my appetite to know more!

As someone who is fairly unfamiliar with the tools and processes employed by the people who monitor, Monitorama was still a pretty great experience. I really enjoyed hearing about the tools, both purchased and open-sourced, that people use to do their jobs. I loved hearing about how they used monitoring and observability to solve interesting problems, or how they found and solved problems with the monitoring itself. I would definitely recommend Monitorama for anyone wanting to learn and discover about monitoring, observability, infrastructure, etc, regardless of existing knowledge or experience.

# One More Thing

Due to an underground fire, a large chunk of Portland lost power during the evening of the first conference day — including Portland Center Stage, where the conference was being held. (Jokes about uptime and SRE here.) The conference organizers were absolutely amazing — not just communicating news and updates through various channels, but moving an entire conference overnight. Huge kudos to them, as well as everyone from out of town who dealt with all of the inconveniences of losing power, including cold showers and moving hotels. People were offering rides, places to stay, power cords, scouting out which coffee shops still had power. It was pretty amazing to see.
