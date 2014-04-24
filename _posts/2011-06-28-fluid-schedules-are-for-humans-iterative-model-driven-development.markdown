---
layout: post
status: publish
published: true
title: Fluid Schedules are for humans, Iterative Model Driven Development
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9387
wordpress_url: http://www.victusspiritus.com/?p=9387
date: '2011-06-28 06:29:52 -0400'
date_gmt: '2011-06-28 13:29:52 -0400'
categories:
- Uncategorized
tags:
- leadership
- design
comments: []
---
<blockquote>
"The key to project planning is to embrace the obvious fact that people don't know, what they don't know."
</p></blockquote>
<p>Requirements and deadlines are the methodical drum beats engineers march to. This holds all the way from bridge building, to systems architecture to large network topology design. The more well defined the problem, the more predictable the performance. The machine like efficiency with which grand systematic projects are executed is both beautiful and awful.</p>
<blockquote><p>
"Inflexible project management is best reserved for generating mediocre fast food."
</p></blockquote>
<p>All but the most trivial dynamic systems are unpredictable over an extended period of time. There's nothing that grates my nerves as much as an absolutely rigid plan with an inflexible schedule, carefully orchestrated to execute a "known" solution. Why are people doing that job? Thinking, feeling, creative beings aren't well matched to repetitive mindless tasks<sup><a href="#notes">1</a></sup>. For that job you want robots coordinating other robots. And in all but the poorest areas it's not cost effective to have people performing tasks that machines are capable of doing.<br />
<a href="http://www.victusspiritus.com/wp-content/uploads/2011/06/waterfall_model.jpg"><img src="http://www.victusspiritus.com/wp-content/uploads/2011/06/waterfall_model.jpg" alt="" title="waterfall_model" width="400" height="300" class="aligncenter size-full wp-image-9393" /></a></p>
<h2>Drowning in Waterfalls</h2>
<p>It's unfathomable that project managers continue to rely on fixed overlapping intervals for complex scheduling. Waterfall planning requires all dependent components be complete before follow on integration steps. Each element delay pushes back the entire project delivery. There are a range of popular alternatives to milestone planning, but they share common flawed assumptions. Beyond catchy names and micro milestones, I haven't witnessed an advantage to replacing one orthodox rules based system with another.</p>
<h2>Fluid Schedules and Iterative Model Driven Development </h2>
<blockquote><p>
"Take all your expertise and stuff it... for the moment"
</p></blockquote>
<p>Experts are blinded by barriers assembled brick by brick through years of practice. We are all creatures of habit and favor the tools and solutions we know best over unfamiliar alternatives. And yet the environment is changing around us as fast as we can adapt (or faster).</p>
<p>If the system your team is designing and planning for has even the slightest bit of novelty, then iterative model driven development is a viable option to test initial designs and to better plan and understand development schedules. </p>
<p>The basis for MDD (model driven development) is rooted in stub and complete system tests which validate subtle changes in functional behavior. </p>
<p>The core idea is to fabricate the simplest possible system and element representation which mimics the desired behavior of a system design. You can think of this as model 0, or more specifically zero order system and element models. Immediate knowledge is gained about assumed bottlenecks and system level characteristics. This information feeds back into planning and design, which leads to refined models for the system and elements. Time can be allocated towards incremental improvement of individual element models, or the system backbone.<sup><a href="#notes">2</a></sup></p>
<p>Model enhancements are more predictable, yet less constrained. Incremental development of higher fidelity models allows the overall system to be tolerant of element delays. </p>
<p><a href="#notes" id="notes">Notes:</a></p>
<ol>
<li>When I refer to repetitive tasks, I mean no disrespect to master craftsmen and artisans. Their work is far outside the bounds of mindless, I'd instead describe their work as mindful.</li>
<li>The system backbone is loosely constrained to be on the same order of complexity as an element. The balance between system backbone and elements is analogous to the roles of controllers and models in application design.</li>
</ol>
