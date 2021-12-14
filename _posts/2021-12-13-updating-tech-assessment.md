---
layout: post
title:  "Improving Our Technical Assessment"
date:   2021-12-13
permalink: /articles/improving-technical-assessment
comments: true
tags: hiring interviewing series-interview-updates
---

Hiring is a constant part of any manager’s job, but I think it can be one of the hardest parts to do well. Thinking about hiring practices usually isn’t a priority until you’re actively hiring. And by the time you’re actively hiring, you’re more likely to use the system in place rather than think about whether that system could be improved.

Even if you do make time to proactively think about your hiring processes, you may not be able to make changes - you might not have the option to try out a one-off process, or it would require approvals from HR or senior leadership, or you’d need agreement from other managers.

But if you are able to prioritize reviewing your hiring practices, and you are empowered to try out some changes to see how they land - what would you do? 

As it happens, I recently had this opportunity! I had the buy-in from my peers to update our technical assessment, and approval from senior leadership to try a different process for panel interviews. For this article I’ll focus on the technical assessment, and follow up with the panel interview changes in a Part 2.

## Previous assessment

Our technical assessment for Quality Engineers was a take-home assignment (I know there are pros and cons to take-homes, but that’s a topic for a different article 😄). The assessment overview that we sent to candidates was pretty straightforward:

<div class="emphasis-block"><p>You will be writing a sample test for $WEBSITE. Your suite can be written in whatever language or tool you want, but it should be deliverable to us in an easily runnable way. Spend about 2-3 hours on this assignment, and work on the following tests and see how much you can accomplish in that timeframe.</p>

<p>Please get it back to us within 3 days. We know you have a life outside of interviewing so if that timeline does not work, let us know & we can adjust.</p>

<p>Verifications: Write some tests that will verify that relevant and important elements and text are present on the page.</p>

<p>User Flow: Write a test that will go through the user flow.  With this test, you will need to fill out $FIELDS.</p>

<p>Please provide any information on your decisions made, and any improvements you would make if you had more time to work on the project.</p></div>

A decent overview, and here are the things I think we did well:
- Setting expectations for timeboxing
- Specific prompts around what we want the candidate to do
- Offering space for candidates to explain their process and where they’d go further if they weren’t timeboxed

But it’s still missing some things that could make this a better experience for candidates, as well as for the folks evaluating these assessments. 

From the evaluation side, candidates were submitting their test suites in a variety of frameworks and languages. When the evaluator wasn’t familiar with the candidate’s choices, it was often difficult to set up their environments so they could run the candidate’s tests. In one case it took the evaluator two hours to get set up properly because of various dependencies! Hiring already tends to take a big time commitment - adding this additional churn to someone’s schedule felt like a good opportunity for tweaking our process.

The rubric we used for evaluation also needed updating - some criteria were too similar and could be regrouped under a single topic; some criteria weren’t specific enough; and one criteria conflicted with how we introduced the assessment to candidates.

## Updated assessment

From the candidate side, we could be much more specific about our expectations for the assessment. These are the areas I focused on improving:
- Instead of leaving the language/framework choice wide open, we included information about what frameworks we use on the job so they could make an informed decision
- Adding an overview of our evaluation criteria so they would know what our priorities were, which could help them decide what to focus on in a limited timeframe
- We told them how the evaluators would be running the tests, which should help candidates set up their tests to be easily runnable and reduce the amount of time it takes to run and evaluate the assessment.

Based on that, here’s what our updated assessment looks like:

<div class="emphasis-block"><p>You will be writing a proof of concept automation test for $WEBSITE. Here we use Javascript/Selenium, so that is our preference for how you complete the automation. However, the purpose of this assessment is to give us an accurate understanding of your automation experience. If there is a different language or framework that you are more proficient in, please use that to complete the assessment. Whichever framework you choose, it should be deliverable to us in an easily runnable way.</p>

<p>This assessment is designed to take about 2-3 hours to complete, and we suggest a target of completing this within 3 days of receiving the assignment. That being said, we recognize that you have a life and responsibilities outside of this interview process. Please let us know if that timeline won’t work for you and we can adjust.</p>

<p>We would like you to write automation that tests the UI. The starting URL for this is $URL. Please make sure your tests cover the following:
Verifications: Write some tests that will verify that relevant and important elements and text are present on the page.
User Flow: Write a test that will go through the user flow. With this test, you will need to fill out $FIELDS.</p>

<p>We will be running your tests on Chrome browsers + macOS, so please make sure your tests are runnable within that environment. When evaluating your assignment, we’ll be focusing on architecture, documentation, and effectiveness.</p>

<p>Please provide any information on your decisions made, and any improvements you would make if you had more time to work on the project.</p></div>

That updated assessment gives candidates better information to work from, and does a better job at setting them up for success. I didn’t make any huge, sweeping changes to our technical assessment, and in fact the assessment itself didn’t change at all. The difference was in adding more context when we introduce the assessment so that our expectations for the candidates are clearer. Now we have a higher likelihood of getting technical submissions that help us evaluate the candidate on the things that we care about.

Hopefully, we’re also offering candidates a better introduction to interviewing at our company - more inclusive, more collaborative, less stressful. Interviewing is, ideally, a collaborative process. Not “us versus them”, but something that interviewers and candidates are navigating together.

In Part 2, I'll show you the changes I've made to the process for panel interviews - again toward that goal of having our hiring process be inclusive and collaborative.

**I’d love to hear from you all! What are some inclusive practices you’ve seen or experienced in hiring? Have you had the opportunity to improve your hiring practices? If so, what did you change and how did it go?**
