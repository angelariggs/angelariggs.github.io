---
layout: post
title:  "Hierarchy of Metrics"
date:   2022-07-18
permalink: /articles/hierarchy-of-metrics
comments: true
tags: guest-post metrics
---

In a previous post, Mojtaba introduced us to the [5 categories of *engineering* metrics]({% post_url 2022-05-10-categories-metrics %}). These are appropriate for engineering teams. When combined with product and design, and looking at the organization and business as a whole, it’s important to distinguish between various levels of metrics. 

## Levels of Metrics

It’s important to distinguish between various levels of metrics, especially when looking at metrics at the highest level. The diagram below attempts to provide a hierarchy of metrics from the highest level of business metrics to the lowest level of engineering service metrics. It’s drawn as a pyramid to show the dependency (lagging-leading relationship), as well as the total number of metrics. 

<br>

<div id="blog-photo">
	<img src="/images/hierarchy-of-metrics.png" alt="A pyramid breaking down the metrics levels described in the sections below">
</div>

<br>

### CxO Level (accountable to the board)

At the CxO level, a handful of financial metrics indicate the performance of the company as a function of input and outcomes. These have direct business implications but are lagging indicators and given that they are the result of aggregation and confluence of many factors, they are difficult to attribute directly to singular causes. 

*Examples of metrics at the CxO level:*

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Open Sans, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Open Sans, sans-serif;font-size:14px;
  font-weight:bold;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
@media screen and (max-width: 767px) {.tg {width: auto !important;}.tg col {width: auto !important;}.tg-wrap {overflow-x: auto;-webkit-overflow-scrolling: touch;}}</style>
<div class="tg-wrap"><table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Input metrics</th>
    <th class="tg-0pky">Outcome metrics</th>
    <th class="tg-0pky">Performance metrics</th>
    <th class="tg-0pky">Health metrics</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">OpEx and CapEx</td>
    <td class="tg-0pky">ARR, revenue, profit</td>
    <td class="tg-0pky">EBITDA, revenue per employee</td>
    <td class="tg-0pky">Overall company engagement score, overall company retention</td>
  </tr>
</tbody>
</table></div>

At times, some high-level customer metrics are also used here since they are leading indicators of financial performance.

### VP Level (accountable to CxO)

Typically, leading indicators of financial performance are customer metrics such as MAU, activation rates, churn, etc. Though these are leading indicators to financial metrics, they are themselves lagging indicators in relation to lower level metrics. Often some measures of financial metrics such as cost breakdown and budgeting are also relevant at this level. For Engineering (and Build), the input (cost) and output (customer value delivery cadence, significance and possibly quality) are also relevant metrics. 

*Examples of metrics at the VP level (for build and engineering):*

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Open Sans, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Open Sans, sans-serif;font-size:14px;
  font-weight:bold;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
@media screen and (max-width: 767px) {.tg {width: auto !important;}.tg col {width: auto !important;}.tg-wrap {overflow-x: auto;-webkit-overflow-scrolling: touch;}}</style>
<div class="tg-wrap"><table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Input metrics</th>
    <th class="tg-0pky">Outcome metrics</th>
    <th class="tg-0pky">Performance metrics</th>
    <th class="tg-0pky">Health metrics</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Functional OpEx and CapEx; f</span>unctional workload metrics</td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">MAU, churn, activation rate</span></td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Overall cadence, significance and quality of delivery to customer (aggregated from programs/departments)</span></td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Functional engagement score, functional retention</span></td>
  </tr>
</tbody>
</table></div>
<br>

### Director Level (accountable to VP)

At this level, specific programs or departments have their metrics that would impact customer metrics. These could be the cost of the program/department as well as value, cadence, and possibly quality of delivery to the customer (as a result of the program or as part of the department). 

*Examples of metrics at the Director level:*

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Open Sans, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Open Sans, sans-serif;font-size:14px;
  font-weight:bold;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
@media screen and (max-width: 767px) {.tg {width: auto !important;}.tg col {width: auto !important;}.tg-wrap {overflow-x: auto;-webkit-overflow-scrolling: touch;}}</style>
<div class="tg-wrap"><table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Input metrics</th>
    <th class="tg-0pky">Outcome metrics</th>
    <th class="tg-0pky">Performance metrics</th>
    <th class="tg-0pky">Health metrics</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Department or Program OpEx and CapEx; d</span>epartment workload metrics</td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Program success metrics (which may be set at customer level, or even financial)</span></td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Cadence, significance, and quality of delivery to customer from program/department (aggregated from teams)</span></td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Department engagement score, department retention</span></td>
  </tr>
</tbody>
</table></div>

The cadence, significance and quality of delivery are leading indicators of higher level customer metrics, but are themselves lagging indicators of lower level metrics. 

### Manager Level (accountable to director)

At this level, metrics pertain to individual projects and teams.

*Examples of metrics at the Manager level:*

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Open Sans, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Open Sans, sans-serif;font-size:14px;
  font-weight:bold;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
@media screen and (max-width: 767px) {.tg {width: auto !important;}.tg col {width: auto !important;}.tg-wrap {overflow-x: auto;-webkit-overflow-scrolling: touch;}}</style>
<div class="tg-wrap"><table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Input metrics</th>
    <th class="tg-0pky">Outcome metrics</th>
    <th class="tg-0pky">Performance metrics</th>
    <th class="tg-0pky">Health metrics</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Team OpEx and CapEx; </span>Team Workload metrics (% of effort per category of work)</td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Product Success Metrics (HEART metrics)</span></td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Team Performance metrics (DORA metrics, Velocity, Cycle Time)</span></td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Team engagement metrics (engagement, happiness)</span></td>
  </tr>
</tbody>
</table></div>


These metrics are often leading indicators to higher level program/department metrics but may be lagging indicators to lower level metrics (e.g. service metrics)

### Team Level (accountable to manager)

The team uses a myriad of metrics to assess the services and systems it runs. 

*Examples of metrics at the Team level:*

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Open Sans, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Open Sans, sans-serif;font-size:14px;
  font-weight:bold;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
@media screen and (max-width: 767px) {.tg {width: auto !important;}.tg col {width: auto !important;}.tg-wrap {overflow-x: auto;-webkit-overflow-scrolling: touch;}}</style>
<div class="tg-wrap"><table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Input metrics</th>
    <th class="tg-0pky">Outcome metrics</th>
    <th class="tg-0pky">Performance metrics</th>
    <th class="tg-0pky">Health metrics</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Service (and feature) costs (development and running); s</span>ervice load (traffic)</td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Service and feature delivery metrics: uptime, latency</span></td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Service metrics in relation to load and cost</span></td>
    <td class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">Number of false alarms, true alarms</span></td>
  </tr>
</tbody>
</table></div>
