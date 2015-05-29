---
layout: post
status: publish
published: true
title: 'Practical Programming: Holding the Flow of Code in Mind'
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2320
wordpress_url: http://www.victusspiritus.com/?p=2320
date: '2009-11-22 10:38:47 -0500'
date_gmt: '2009-11-22 17:38:47 -0500'
categories:
- Uncategorized
tags:
- mind
- coding
- decision making
- design
comments: []
---
<p style="text-align: center;"><a href="http://www.stuckincustoms.com/2009/09/20/a-lonely-walk-to-the-ocean/"><img class="aligncenter size-full wp-image-2109" title="A Lonely Walk to the Ocean" src="{{ site.url }}/assets/2009/11/LonelyBeach.jpg" alt="A Lonely Walk to the Ocean" width="480" height="330" /></a></p>
<p>I've been thinking heavily about Internet information flow, and software design for the past few weeks. I took some time this morning to put some of those abstract thoughts into words. Much of my recent effort has been consumed by setting up proper development environments for a Ruby on Rails based project which <a href="http://twitter.com/tylergillies">Tyler Gillies</a> has architected.</p>
<h2>Start With a Simple and Solid Foundation</h2>
<p>A pro move is to begin with a firm understanding of your building blocks, your lower level objects and functions and library utilities. Your confidence in how fundamental objects interact and affect data flow through your system will shorten the often painful process of debugging. It will also provide you with a clearer picture of modular components for higher level design.</p>
<p>Taking the time to unit test (piece wise) your code is also a great way to incrementally approach a more complex problem. Rails framework is complimentary to this method, as component testing is hard wired into the project directory structure. Although unit test writing takes time away from new development, most experts agree the time saved in debugging is well worth the effort. As a guy who's spent TOO MUCH time debugging software, I can respect this outlook.</p>
<h2>Levels of Code Design</h2>
<p>Most desktop applications have various levels of functional flow. Visual user interfaces wait patiently for user interaction to drive some form of processing, analysis, or visualization forward. Command line programs may have a huge hierarchy of input file control mechanisms. Libraries can be static or dynamic and may well depend on a complex and deep set of other libraries and code.</p>
<p>In the case of web programming, <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/11/15/walking-down-the-tracks-of-ruby-on-rails/">Rails implements a MVC (model view control)</a> design. The library functionality of ruby is based on compiled gems. You can zoom into the model handling (data interfaces), the view (visualization), or the algorithm and program flow (control). This helps to isolate the various components into more manageable byte sized concepts.</p>
<h2>Pulling it all together, keep program flow in your conscious mind</h2>
<p>This is where much of the above practical habits pay off.</p>
<p>If you started with:</p>
<ul>
<li><span style="background-color: #ffffff; ">simple reliable structures and libraries</span></li>
<li><span style="background-color: #ffffff; ">and implement unit tests to ensure modular functionality</span></li>
<li><span style="background-color: #ffffff; ">and separated out the highest level program flow into data, visualization and control segments</span></li>
</ul>
<p>You give yourself, and your team the best chance at producing effective and efficient software quickly, and reliably. When it comes to "zooming out" functionally to the highest level program flow, the above practices allow software designers to have a confident image of their entire system. This is  a priceless quality when it comes to planning and implementing changes to a code base, and understanding how those changes will affect the stability of the software.</p>
<p>This is a continuation of practical programming tips from the <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/08/22/optimal-design-performance-under-stress/">design under stress</a> series, with a correlation to <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/07/03/human-condition-flow-is-action-experiencing/">work flow state</a>.</p>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://avdi.org/devblog/2009/11/18/self-confidence-through-assertions/">Assertive Code</a> (avdi.org)</li>
<li class="zemanta-article-ul-li"><a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/11/11/pigs-may-not-have-wings-but-i-can-ride-the-rails-with-a-flu/">Pigs may not have wings, but I can Ride the Rails with a flu</a> (victusspiritus.com)</li>
<li class="zemanta-article-ul-li"><a href="http://avdi.org/devblog/2009/10/29/simplicity-is-complicated/">Simplicity is Complicated</a> (avdi.org)</li>
<li class="zemanta-article-ul-li"><a href="http://techhotspot.com/2009/11/04/codepad/">Codepad</a> (techhotspot.com)</li>
<li class="zemanta-article-ul-li"><a href="http://r.zemanta.com/?u=http%3A//www.infoworld.com/d/developer-world/jetbrains-upgrades-ruby-ide-727%3Fsource%3Drss_infoworld_news&amp;a=9638996&amp;rid=26c19024-a1a7-4a53-88b6-1db105d1c8b5&amp;e=31c60289c570a5c8b54d4f80a7bfb10e">JetBrains upgrades Ruby IDE</a> (infoworld.com)</li>
<li class="zemanta-article-ul-li"><a href="http://joi.ito.com/weblog/2009/08/11/agile-developme.html">Agile development, startups and government policy</a> (joi.ito.com)</li>
</ul>

