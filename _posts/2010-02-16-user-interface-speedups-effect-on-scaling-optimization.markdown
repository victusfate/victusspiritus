---
layout: post
status: publish
published: true
title: User Interface Speedups Effect on Scaling Optimization
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3054
wordpress_url: http://www.victusspiritus.com/?p=3054
date: '2010-02-16 05:56:14 -0500'
date_gmt: '2010-02-16 12:56:14 -0500'
categories:
- Uncategorized
tags:
- web/tech
- coding
- optimization
- design
comments: []
---
<p><i>If you're a coder and in a hurry I included links to a couple of tools and how to use them at the end of the post</I> </p>
<p>Unless your goal is to craft retro techno-art that's defined by its visible blockiness and/or slow response, the aesthetic image you strive for is minimal attention footprint. Designer's endeavor to cultivate a user experience where the technology <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/01/29/the-ideal-computer-converges-on-invisible/">blends into the background</a>. To achieve this, your application must have rapid response, and smooth transitions. The wonderful news, is that designing for rapid user response allows more interactions per second (scale).    </p>
<p>If users can get in and out of your database and processing chain fast enough, you can handle more interactions. The flip side is that user behavior shifts with swift response. Now each user or API hit is more likely to perform repeat tasks with your tool. Just as heavy foot traffic is great for a storefront, heavy user and tool usage of your application is a great sign for growth, but never let them see you <a href="http://www.whatisfailwhale.info/">sweat</a>. </p>
<p>You probably noticed how I slipped in API hits as a use case. We can no longer afford the luxury of thinking only of end users as people, but must include external applications. As developers continue to blur the line between web utilities and destinations, each application has the opportunity of providing database access to downstream services. Many new businesses fear commoditization of their service by sharing important data. This is the wrong way to frame the problem. </p>
<p>Commoditization of a novel service is inevitable (it may take years and there are exceptions but they don't scale as well). Plan for rapid continuous market change, and even self disrupting tech. If you don't explore the next great market, a competitor will invent and own it. Now you either have to acquire (ok), mimick (crappy), or reinvent a new focus in that space (acceptable).</p>
<h2>Data Portability and Remote Access</h2>
<p>One of the methods in designing a fast response is to remove unnecessary nodes from a path. This is precisely what we did with <a HREF="http://imm.victusmedia.com">Social Gravity</a> a search/social interface. Instead of grabbing relevant statuses and pushing them back out to the end user, we leveraged jQuery/JavaScript to create a local interface at each browser, that connects directly to the social status backbone (which is Twitter now, next up Buzz/Facebook).  </p>
<p>As long as users can access their data they don't even need to stop and pay an "attention tax" at Victus Media. We expect users to grant other <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/07/17/layered-internet-apps-real-time-search-as-virtual-assistant/">layers of the Internet stack</a> access to their data, or grab it themselves for local usage. This is the whispered beginnings of a virtual assistant to aid in search, a machine readable list of topics based on your interests. With that alone web services can tailor your experience with smarter defaults. Your interests can project out from natural social sharing (among other behaviorial cues). You'll implicitly shape the virtual environment and interface with your interests and social connections.</p>
<h2>Tools to Help Developers Optimize</h2>
<p>You can roll your own timing tools to keep track of how long each method takes, or you can find tools that already do that. </p>
<p>A potent and fairly universal timing tool is firebug. There's an addon and extension for Firefox and Chrome respectively. There's documentation <a HREF="http://getfirebug.com/">here</a> (see the profiler and network interaction) on how to use Firebug to measure your site load time.</p>
<p>In Ruby on Rails I found the combination of Model <a href="http://www.rubyinside.com/19-rails-tricks-most-rails-coders-dont-know-131.html">benchmark</a> and <a href="http://ruby-prof.rubyforge.org/">ruby-prof</a> to be a great combination for measuring code time. Here's the document I should have been reading yesterday, <a HREF="http://guides.rubyonrails.org/performance_testing.html">Performance Testing</a>.</p>
