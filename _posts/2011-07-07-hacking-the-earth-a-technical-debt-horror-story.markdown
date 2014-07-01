---
layout: post
status: publish
published: true
title: Hacking the Earth, a Technical Debt Horror Story
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9632
wordpress_url: http://www.victusspiritus.com/?p=9632
date: '2011-07-07 07:32:31 -0400'
date_gmt: '2011-07-07 14:32:31 -0400'
categories:
- Uncategorized
tags:
- coding
- decision making
comments: []
---
<p>Bloggers are notorious over exaggerators and I shamelessly confess that I'm cut from the same cloth. My tale of technical debt is no more horrific than a Gorilla in a prom dress, yet I hope it will serve as a friendly reminder that some shortcuts are better left for Jacque Cousteau's jungle crawlers.</p>
<p>For the past few days I've been supporting a software delivery out in Arizona<sup><a href="#notes">1</a></sup>, and to set the atmosphere I'll emphasize that it gets <b>warm</b> here in the summer. The team I've worked with has provided fantastic support and kicked it up into high gear over the past month. They've gone the extra distance by extending the initial delivery date (first date was too optimistic), freed up local top notch developer and analyst time to support integration (sharp team), and minimized meetings (have I told you lately that I love you?).</p>
<p>While cutting corners on a rapidly approaching cut off date, I performed all manners of unsavory software hacks. Most of those were forgivable faux paus, but one in particular I feared would come back to haunt me. You can safely guess the outcome based on the post title.</p>
<h2>Hacking the Earth</h2>
<p>An Earth model that we developed in my shop back east is driven by a keyed input file, and is composed of an assortment of tables and polymorphic transformations. These structures support line of sight modeling differences for spherical or WGS84 Earth geometries, as well as varied atmospheric conditions.</p>
<p>The host service that this class lives within has a specified copy constructor and as I looked through the nested pointers in the class, I opted for file based reconstruction.  And that served just fine and dandy until yesterday.</p>
<p>It turns out the host simulation is normally run on all manner of dynamic mounted drives and, all input files require specification in the main configuration files. Uh oh! This is done to allow relative paths to function with user set paths and run from any location. As we bumped into the issue around 6pm local time yesterday evening, I volunteered (prompted by the disapproving glares of my team) to correct my wrong doings and fix the code before we left last night.</p>
<p>I was desperately seeking any shortcut to avoid having to write copy constructors and clone functions for the Earth model and all its members, but didn't see any way around it. My refactoring began with a wordpad editor and a browser download of a few svn accessible files. I was pretty foggy by this point as it'd been a long and busy day which began ages ago when I woke up 3am local time. My poor choice of editing environments lead to a quick failure, and a swap to the tech integration lead's <sup><a href="#notes">2</a></sup> sweet Mac and Win VM setup, with Visual Studio loaded and ready.</p>
<blockquote><p>
Pro Tip: Well designed IDEs are a life saver when you're bleary eyed and the alternative is Wordpad.
</p></blockquote>
<p>The top level of recoding revealed another layer of polymorphic composed object pointers. Like a Russian doll, each pointer referred to a contained base class which in turn required clone and copy constructors to satisfy the parent objects copy. The clock ticked by for a few hours while I hacked my way downward, adding clone methods as I went to all base and inherited classes. We finally left off last night at the bottom of the stack, with just a single class left, with each of it's children having no further contained classes. At that point I felt guilty for holding up my colleagues Eric and Mikhail who deserved a healthy break and had long since completed their own tasks, so we called it quits for the night.</p>
<h2>Lesson Learned</h2>
<p>A Sucker Punch quote comes to mind:</p>
<blockquote><p>
"Don't write a check with your mouth you can't cash with your ass."
</p></blockquote>
<p>Technical debt has a way of demanding compensation at inopportune moments, and while it's not inevitable, it is mostly avoidable. In this case if more care was taken with specifying polymorphic base classes with clone and copy constructors, my refactor work would have been trivial. This morning I'll review last night's dicey hacks and ensure that checks for self assignment are done in the copy constructors, while validating the new code.</p>
<p><a href="#notes" id="notes">Notes:</a></p>
<ol>
<li>For background see <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/05/12/a-tale-of-two-simulations/">A Tale of Two Sims</a>, and it's <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/06/15/crazy-east-coast-weather-wild-work-tale-of-two-sims-part-duo/">sequel</a>. </li>
<li>Eric has been doing a killer job pulling the code all together with meeting "point defense" by Greg (epic tech management). The entire team has been a pleasure to work with: Mikhail my partner in modeling, as well as Dan and Cort for c++ wizardry. We've had some rough spots the past couple of days, but it's all coming together.</li>
</ol>
