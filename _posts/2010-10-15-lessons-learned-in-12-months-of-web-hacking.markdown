---
layout: post
status: publish
published: true
title: Lessons learned in 12 months of web hacking
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5473
wordpress_url: http://www.victusspiritus.com/?p=5473
date: '2010-10-15 01:52:41 -0400'
date_gmt: '2010-10-15 08:52:41 -0400'
categories:
- Uncategorized
tags:
- coding
- ebook
comments: []
---
<h2>Quick list of some lessons I learned in the last year</h2>
<p><I>Never make a client wait</I></p>
<p>I've made and continue to make mistakes while experimenting. My earliest design faux pas was forcing clients to wait on long page loads while applications daisy chain remote APIs (big no no). A better way to connect remote APIs is through asynchronous calls or background processes. </p>
<p><I>Syntax</I></p>
<p>I'll slip up on syntax with a botched regular expression in Ruby or misplace a colon or brace in JavaScript, yielding pages which are dead on arrival. This drives me to Chromium's inspect or Firebug (I prefer Rails' error messages). Since most of my hacks are freehand sketches without a clear end point, strict testing based development makes little sense. I need to see and feel an interface as feedback. For larger, task oriented projects careful testing reduces complexity errors from slipping to live servers. </p>
<p><I>JavaScript Scope</I></p>
<p>If you've spent any serious time coding with other languages you'll probably freak out about JavaScripts funky scoping rules. It's my own fault for developing in c++ for so many years, I expect functions to follow a sequential pattern and for local variables to end with the scope. Javascript function calls are asynchronous and any state information you want at the time of the call needs to be explicitly passed to the function. As long as you do that, JavaScript behaves quite nicely. There are globals but counting on them for complex programs is a recipe for disaster, not to mention mucking up the namespace. JavaScript has some mighty cool features that <a href="http://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742">JavaScript the Good Parts</a> covers in great detail, and yeah there's an <a href="itunes.apple.com/br/app/javascript-the-good-parts/id312652400?mt=8">app for that</a>. As an additional reference David Semeria put together a sharp <a href="http://lmframework.com/blog/2010/02/closures-in-javascript/">slide deck</a> on closures. </p>
<p>After reviewing posts from the last year or so on lesson's learned, I've decided to write my second ebook on the subject. There are many topics that would be much better served by a long format. I've wanted to stress test Anthologize with a few hundred posts, and it's been over a year since my first mini-ebook. </p>
