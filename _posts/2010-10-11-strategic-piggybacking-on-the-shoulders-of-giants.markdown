---
layout: post
status: publish
published: true
title: Strategic piggybacking on the shoulders of giants
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5444
wordpress_url: http://www.victusspiritus.com/?p=5444
date: '2010-10-11 06:39:12 -0400'
date_gmt: '2010-10-11 13:39:12 -0400'
categories:
- Uncategorized
tags:
- web/tech
- coding
- decision making
comments: []
---
<p><a href="http://en.wikipedia.org/wiki/Time_Bandits"><img class="aligncenter size-full wp-image-5445" title="time_bandits_giant" src="{{ site.url }}/assets/2010/10/time_bandits_giant.jpg" alt="" width="200" height="150" /></a></p>
<p>The largest gradient to improving the value of your time as a founder is aligning specific project goals with a well matched open source community. Leveraging enormous man hours of technical design powered primarily by enthusiasm makes perfect sense. Many of the contributors aren't just amateurs like myself with only a dozen months of web development experience notched on their belt. They're leaders and professionals with many years of hands on expertise.</p>
<p>There's a legion of brilliant hacker types that are sharp and dedicated to pure web development. I've had the good fortune to bump into <a href="http://twitter.com/#!/victusfate/hackers">many of them</a> in my technical document searches, github browsing, and blog readings. While I'm cutting my teeth, these folks have been crafting web apps in their sleep, often times for over a decade. They think in HTTP with their favorite scripting languages and are fluent in RESTful protocols. App design and back ends are second nature to them. The hard part as a guy on the fringes, is figuring out which code tools to use and where to dive in. In order to make an informed decision on where to dedicate limited resources it's imperative that we know of what's out there, understand the benefits/limitations of given choices, and have a system for identifying a good enough solution.</p>
<p>Let's look at few options for dynamic web applications. By no means is this list complete. Yet there are enough different choices here to get a feel for how broad web application technologies are. Here's a cross sample of the most popular choices available to today's budding web developer:</p>
<ul>
<li><a href="http://en.wikipedia.org/wiki/LAMP_%28software_bundle%29">LAMP</a>
<ul>
<li>linux, apache http server, mysql, and php/perl/python</li>
</ul>
</li>
<li><a href="http://rubyonrails.org/">Ruby on Rails </a>
<ul>
<li>full featured ActiveRecord based web framework</li>
</ul>
</li>
<li><a href="http://www.sinatrarb.com/">Ruby with Sinatra</a>
<ul>
<li>choice of data layer leaner/lighter than Rails</li>
</ul>
</li>
<li><a href="http://nodejs.org/">node.js</a>
<ul>
<li>javascript interface to low level c asynchronous web server</li>
</ul>
</li>
<li><a href="http://expressjs.com/">express</a>
<ul>
<li>web framework built on node.js</li>
</ul>
</li>
<li><a href="http://code.quirkey.com/sammy/">Sammy</a>
<ul>
<li>tiny javascript framework built on jQuery</li>
</ul>
</li>
<li><a href="http://couchapp.org/page/index">CouchApp</a>
<ul>
<li>couchdb application framework</li>
</ul>
</li>
<li><a href="http://www.djangoproject.com/">Django</a>
<ul>
<li>Python web framework</li>
</ul>
</li>
<li><a href="http://www.tornadoweb.org/">Tornado</a>
<ul>
<li>the power behind Friendfeed's webserver</li>
</ul>
</li>
<li><a href="http://github.com/blog/308-compojure-clojure-web-framework">Compojure</a>
<ul>
<li>clojure framework</li>
</ul>
</li>
<li><a href="http://liftweb.net/">Lift</a>
<ul>
<li>scala framework</li>
</ul>
</li>
<li><a href="http://www.asp.net/">Asp.net</a>
<ul>
<li>for Microsoft junkies</li>
</ul>
</li>
</ul>
<p>All of these choices are founded on core technology that's the result of hard work and practical technical design. Some options are newer than others, but newer doesn't always translate to better. The more likely correlation is that less popular alternatives have had less opportunity for practitioners to shake out potential bugs. A fairly new framework can support millions of applications which rapidly refine it's source. The advantage of some of the younger frameworks is that they're easier to hit the ground running. There's no need to configure server details out of the gate and lower levels are abstracted away for easy availability to the application layer.</p>
