---
layout: post
title:  "DevOpsDays PDX"
date:   2017-08-10
permalink: /blog/devopsdayspdx
comments: true
---

Last week, I attended my first DevOpsDays PDX! I wasn’t quite sure what to expect, but it seemed like a cool conference - DevOps obviously intersects with QA work, and my interest has been peaked by articles I’ve read from the likes of [New Relic](https://newrelic.com/devops/what-is-devops), [Julia Evans](https://jvns.ca/blog/2016/10/16/whats-devops/), and [Etsy](http://www.networkworld.com/article/2886672/software/how-etsy-makes-devops-work.html). It ended up being an awesome experience, full of interesting talks and conversations, and I came away from it feeling reinvigorated about how I do my job as a QA Engineer.

## Why DevOpsDays?

A while back, I had a conversation with some developers about what DevOps is. For instance, many companies will post an opening for a DevOps Engineer. I see discussions on the interwebs about tooling that is DevOps - Puppet and Jenkins and New Relic. People talk about the tasks of DevOps - deploying code, running tests, monitoring. It was an enlightening conversation, and really interesting to dig down past the misunderstandings around what DevOps is and isn’t.

DevOps is not a title.

DevOps is not a set of tools.

DevOps is not a group of tasks.

DevOps is a mindset and a culture that promotes collaboration between people and departments that are involved in the development lifecycle. It’s about figuring out a (likely iterative) process for creating, deploying, and maintaining quality code within a set of best practices.

As I continue to develop my role as a QA Engineer - and think about how I want to continue growing and learning, and what I want the role to bring to Metal Toad - DevOps is a really interesting topic to dive into. I want to figure out how to bridge the divide between our developers and our Cloud team, and how I can help create that bridge with the QA department.

## The Conference

DevOpsDays PDX was a single-track conference, which is definitely my preferred format. I get serious FOMO when I have to pick and choose, because there are always talks and workshops that overlap and I have to end up missing some that sound really awesome. The program was a mix of keynote and longer talks, some shorter Ignite talks, and [Open Space](https://www.devopsdays.org/open-space-format/) discussions. I really enjoyed the varied formats throughout the day, and the Open Spaces discussions were especially interesting. This was my first experience with them, and I listened more than I talked, but it was great to see these informal chats unfolding and iterating authentically between people.

## Talk Highlights

I always take notes on talks when I go to a conference, and every speaker at DevOpsDays left me with some bit of inspiration - whether it was a single sentence that really hit home, or a new process or concept that I was excited to learn more about.

### On Being Anti-Fragile

Jan de Vries gave an awesome talk on ["Antifragility in DevOps"](https://www.slideshare.net/MeYouSlide/jan-de-vries-antifragility-applied-to-dev-ops-and-to-your-life). Software projects are inherently fragile; with competing concerns, tensions between time, budget, and scope; and the sheer number of tasks that have to be coordinated within the project. Continuous Delivery, therefore, is used to counter this fragility - because the processes that make up Continuous Delivery enable it to be anti-fragile. Some of his main points were:

* Stable systems are fragile - because they don’t change, they also don’t respond to failures and iterate around them. Eventually, those shocks to the system are too much and it fails hard.

* Anti-fragile systems break a little all the time, but they evolve as a result, and are therefore less prone to catastrophic failures

* Tinkering is anti-fragile: a continuous process of small experiments and subsequent learning

* Negative knowledge (what doesn’t work) is more robust and resilient than positive knowledge (what is working)

* Ensure that the people working on the system or project have “skin in the game”. People who aren’t invested don’t care.

### On Whether Our Tests are Valuable

Lucy Wyman and Zach Reichert of Puppet gave a really great talk titled ["Are Our Tests Any Good?"](http://slides.lucywyman.me/qaelk.html#1), about how they figure out whether their tests are actually valuable. They asked themselves a series of questions, each one digging a little deeper into the meaning of the one before it:

* Are our tests providing value?

* What makes a test valuable?

* Which tests tell us that our code is broken?

* Can a test that never fails actually provide value?

* Are our tests worth the cost of running them?

They used CI metrics to try and answer these questions. The tool(s) they used was QAELK, which stands for Quality Assurance ElasticSearch Logstash Kibana(but actually Grafana). The dashboard they created from these tools allowed them to aggregate and visualize data about their acceptance testing, including how long tests took to run, and how often they failed. The data allowed them to refactor their tests, as well as remove tests that ended up proving themselves not to be valuable, according to the questions they were asking.

The question _“What makes a test valuable?”_ was especially interesting to me, as the concept of value has many connotations; and I thought about this question more from the other end - what makes a test valueless? NOTE: I couldn’t really think of the inverse of the word valuable as I was writing this, and my quick search to find the word valueless brought up a lot of words that would apply, which actually highlight some reasons that a test wouldn’t have value: _pointless, ineffective, unproductive_.

A test could be valueless if it takes too long to run, which costs the company money. A test could also be valueless if it’s fast, but doesn’t ever break. This sounds pretty counterintuitive at first, right? Wouldn’t successful tests highlight good code? Maybe, but no code is perfect, and failing tests alert the team where they can improve and iterate their code. If a test truly never fails, it’s either A) not a good test, so it’s not catching the failures; or B) It really is testing code that is good, and doesn’t need to run every time.

### On the Culture and Community of DevOps

In his talk [“Archetype of an SRE Superhero: A DevOps Journey”](http://bit.ly/SRESuperHero), Jason Grimes talked a lot about the culture of DevOps - reaching out on Twitter, understand what topics are important to the community, increase your knowledge base by increasing your community. He put together a Twitter list of DevOps and SRE experts that you can check out [here](http://bit.ly/automators). I’ve [written previously](http://angelariggs.github.io/blog/tweeting-for-community-and-understanding) about Twitter as a community in tech, so this idea of creating your virtual community of experts and colleagues really resonated with me.

One of his lines especially stuck with me as a vital part of growing and learning: “Let go of being right, and meet people where they are.” YES! This is such a great concept, and so important for people in any role or workplace, but it’s so hard to actually implement in your day-to-day.

## Takeaways

The underlying theme of the conference was a conversation around the question “how do we DevOps?”. Some of the answers that I heard were:

* Emphasize a culture of DevOps

* Get buy-in from peers and execs: It’s all about collaboration, so if people aren’t invested in making it happen, then it’s an uphill battle that you’ll eventually lose

* Figure out a process that works

* “Create the process, stick to the process, expect the process to hit blockers, iterate the process”: If you never iterate, you never improve. Worry more about getting started than getting it perfect.

* Communication is KEY

* Commitment > compliance: Change is emotional, not logical. It’s better to have people committed to promoting the culture of DevOps, than to hold them to a rigid standard of process

* “Let go of being right, and meet people where they are”

* Celebrate your wins!

I had a fantastic time at DevOpsDays PDX, and thoroughly enjoyed the conversations, the questions, the opportunities to learn. I will absolutely be attending next year’s conference, and definitely recommend this as a great experience for anyone in tech!
