---
layout: post
status: publish
published: true
title: When writing engineering software be like Scotty
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9271
wordpress_url: http://www.victusspiritus.com/?p=9271
date: '2011-06-16 13:11:16 -0400'
date_gmt: '2011-06-16 20:11:16 -0400'
categories:
- Uncategorized
tags:
- career counseling
- coding
- design
comments: []
---
<p><a href="http://memory-alpha.org/wiki/Montgomery_Scott"><img src="{{ site.url }}/assets/2011/06/20110616-041219.jpg" alt="20110616-041219.jpg" class="alignnone size-full" /></a><br />
<blockquote>
"Starship captains are like children. They want everything right now and they want it their way. The secret is to give them what they need, not what they want."- Scotty, offering La Forge advice on handling Starfleet captains</p>
<p>"I cannot change the laws of physics! I've got to have thirty minutes."</p>
<p>Another tip of the hat to one of my favorite <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/01/26/scotty-macgyver-doctor-who-are-hackers/">hacker archetypes</a>.
</p></blockquote>
<p>Almost without exception, writing trustworthy software takes two or three times longer than junior engineers and managers estimate. Seasoned engineers know better. Plug and play is a saying best reserved for Legos.</p>
<p>Tuesday I began coding an image simulation program in c++ which I suspect will weigh in at under 1k lines of new source. I was given 24 hours to complete the task. It's a straight forward optical and digital focal plane sim that takes in a description of sensor parameters and objects, and produces image data (without complex backgrounds). </p>
<p>In addition to the functional requirements, the software should have minimal dependencies for easy porting (it will run under Linux although are libs have been crafted on Windows systems), and it needs to run faster than real time (single process). Those requirements translated into the necessity for a small bundle of new code to do the job.</p>
<p>I got a bit cocky while slapping together the headers and structures. Instead of writing and testing one element at a time, I wrote all the processing steps in one fell swoop. It was great seeing everything compiling so quickly without the mental overhead of a heavy weight code base, in contrast to my current main project which is coming to a close. Everything went smoothly until I began carefully thinking about all the steps that require testing: </p>
<ul>
<li>I/O for common params</li>
<li>I/O for individual fields of view</li>
<li>transformations of input data into common units</li>
<li>initialization of all object state</li>
<li>ensuring sure base classes that are part of stl array structures have clone methods to handle their children pointers copying. I came across auto_ptrs for future tasks, but tracking down that careless error took 20 minutes longer than it had to</li>
<li>identifying a test case that exercises all components</li>
<li>constructing test data including reasonable sensor attitudes, object state, and varied conditions</li>
<li>generating intermediate output data at each step. The visual studio 2010 debugger is inadequate for reviewing object state compared to visual studio 2008</li>
<li>visualization of output data. My old standard cube viewer and it's predecessors work with a specific file format. Matlab provided a rapid plotting tool</li>
<li>and the list goes on...</li>
</ul>
<h2>One bunny trail after another</h2>
<p>Just shaking down the file I/O took an hour to pass muster. While doing so I uncovered a number of required inputs that were left out of the first pass, and moved a few parameters from specific elements to common structures. After that review everything fell into place on the input/control side. </p>
<p>Constructing a fairly robust test case demanded additional geometric transformations. After adding those components I noticed the conversions from radiance to counts looked off. Tomorrow morning I'll do a thorough review of those optical transfer equations, and make sure the results match what I expect. </p>
<h2>Modular testing is a wide angle lens for the mind's eye</h2>
<p>What I reminded myself over the past couple of days is that there's no short cut to writing good software. When you're rushed to deliver functional programs on a tight budget, it's worth putting the breaks on to review each element individually first. </p>
<p>"I'm giving her all she's got captain!"</p>
<p>On rare occasions it's ok to pull out all stops and crank out reckless code like a runaway train. </p>
<p>Just be sure to clean up after yourself when things settle down. If the situation never settles into a sustainable rhythm, odds are you're in a soon to be extinct business.</p>
