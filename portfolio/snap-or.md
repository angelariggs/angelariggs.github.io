---
layout: page
title: snapOR
permalink: /portfolio/snap-oregon/
comments: true
---

<div class='add-pad'>
	<p><a class='res-link' href='http://snaporegon.herokuapp.com/' target='blank'>Launch snapOR website</a> or <a class='res-link' href='https://github.com/snap-oregon/snapOR' target='blank'>view repo on GitHub.</a></p>

	<h2 class='project-sec-header'>About snapOR</h2>
	<p>snapOR is a site for adventurous photographers, who enjoy exploring and photographing the beauty of Oregon. Use our website to explore state parks in Oregon, and see photos that other hikers have taken there.</p>

	<p>Along with two teammates, I built this website as my capstone project for Portland Code School's Full-Stack JavaScript Immersion course. From July 1-31, we built our website from the ground up, starting with wireframes and ending with a fully-functional website.</p>

	<p>snapOR is built with a combination of Foundation & Backbone for the front-end; JavaScript, Express, AJAX, and Node for back-end; and APIs from Google Maps, Oregon State Parks, and Flickr. We used GitHub for version control, and transitioned between Trello and ZenHub for tasks and tickets.</p>

	<h2 class='project-sec-header'>Responsibilities</h2>
	<p>I knew that I wanted to use my final project to build up my skills across the stack. With this in mind, I took responsibility for the Oregon State Parks API integration, Backbone for account interaction (registering, logging in/out, updating account information), configuring the Express server, and Sass. I also came up with the initial concept of snapOR, and created wireframes for the group.</p>

	<h2 class='project-sec-header'>Reflection</h2>
	<p>Our group's first task was to divide responsibilities, so we wouldn't be stepping on each other's code. In spite of this, there were some mishaps when it came to building out the user interactions (logging in, registering, etc), and the functionality got lost. Currently, snapOR uses jQuery to toggle the nav bar when a user action is performed, but there's no persistence. I think this was a result of too many hands in the same code, and lack of communication between teammates, so it wasn't clear how much progress had been made when the code switched hands.</p>

	<p>We also concentrated too much on form, rather than function, in the beginning stages of our code. We implemented Foundation almost immediately, but this later caused AJAX issues between the Foundation modal windows and our Backbone code. It took a lot of troubleshooting to figure out that our AJAX requests weren't working as designed because of the Foundation modals. The solution seems to be ripping out Foundation, and rebuilding the website with just HTML/Jade and Backbone, then adding Foundation back in if I want to use it for styling. However, I found this solution too late to be useful, and we decided to use the jQuery toggling for the final presentation of our website.</p>

	<p>I learned that I need to focus on the functionality and basic structure of my website, before moving on to the styling of it. I also learned that communication is so important throughout a project, and collaboration - or lack thereof - can be harder to work around than any challenges with code.</p>

	<div class='project-grid'>
		<div class='photo-space'>
			<img class='snap-screenshot left' src='/images/snapor-homepage.png'>
		</div>
		<div class='photo-space'>
			<img class='snap-screenshot right' src='/images/bandon-state-park.png'>
		</div>
	</div>

	<!-- <div class='project-grid'>
		<div class='photo-space'>
			<img class='snap-screenshot' src='/images/oswald-west.png'>
		</div>
	</div> -->
</div>