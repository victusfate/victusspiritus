---
layout: post
status: publish
published: true
title: Each Time I Get My Hands Dirty, I Learn
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2975
wordpress_url: http://www.victusspiritus.com/?p=2975
date: '2010-02-08 06:18:37 -0500'
date_gmt: '2010-02-08 13:18:37 -0500'
categories:
- Uncategorized
tags:
- web/tech
- semantic
- victus media
- coding
- ruby
comments:
- id: 2917
  author: Gotta Grock Git &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/02/09/gotta-grock-git/
  date: '2010-02-09 05:37:04 -0500'
  date_gmt: '2010-02-09 12:37:04 -0500'
  content: "[...] friendfeed        Each Time I Get My Hands Dirty, I Learn [...]"
- id: 2930
  author: Mind =&gt; Tools, dynamic and static typing &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/02/11/mind-tools-dynamic-and-static-typing/
  date: '2010-02-11 07:43:07 -0500'
  date_gmt: '2010-02-11 14:43:07 -0500'
  content: "[...] an earlier post I mentioned I&#8217;d come back to the advantages
    of dynamic typing. My primary reference for all [...]"
- id: 6227
  author: Exploring speculative execution and evaluation &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/10/02/exploring-speculative-execution-and-evaluation/
  date: '2010-10-02 14:55:40 -0400'
  date_gmt: '2010-10-02 21:55:40 -0400'
  content: "[...] encountering these terms, I&#8217;ve become more comfortable with
    their meaning, transcending the spooky animal phase. Lazy evaluation is simply
    delayed computation until a result is required. Pure functional programs [...]"
- id: 8206
  author: Dynamic scripting with static speed, the best of both worlds &raquo; Victus
    Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/01/28/dynamic-scripting-with-static-speed-the-best-of-both-worlds/
  date: '2011-01-28 13:14:43 -0500'
  date_gmt: '2011-01-28 20:14:43 -0500'
  content: "[...] Each time I get my hands dirty I learn [...]"
- id: 9595
  author: Pattern CLiPS &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/03/21/pattern-clips/
  date: '2011-03-21 04:47:14 -0400'
  date_gmt: '2011-03-21 11:47:14 -0400'
  content: "[...] if you want to process individual messages. I described the API
    costs and free levels in an earlier post.  The past few days I’ve been digging
    into Open Calais’ API. They have another great semantic [...]"
- id: 9698
  author: One line installs, One button deploys &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/03/28/one-line-installs-one-button-deploys/
  date: '2011-03-28 06:16:01 -0400'
  date_gmt: '2011-03-28 13:16:01 -0400'
  content: "[...] and partner materialized out of crossing real time updates, and
    showed me that I need to get my hands dirty. When I wanted to better understand
    distributed social networks, I was introduced to open social [...]"
---
<p>As long as I'm unwilling to face an obstacle, my mind invents clever schemes to prevent me from having to deal with undesirable tasks. That results in me treating the obstacle as a <a href="http://www.youtube.com/watch?v=O4MlIOCNIW4">spooky animal</a>. It also means I will miss out on any advantages of understanding the taboo subject.</p>
<p>My biggest hurdle over the past dozen years has been learning a new programming language. After getting comfortable with C++ (and c) I couldn't imagine starting out all over. Learning how to translate thoughts into data structures, objects, and methods took me a good two years to understand, and five to get very comfortable with. But last year that barrier finally got worn away by a potent force, my enthusiasm to build <a href="http://victusmedia.com">a highly capable web information tool</a>.</p>
<p>At that point I began to familiarize myself with php and common web programming languages. I had never consciously written code to access a web API before writing a script to access Twitter late last summer. The documentation was rich, but I kept looking for something like an include to dig into source code. That's how I used to figure interfaces out, often my own source code written years earlier. But APIs only reveal the interface, they are the block box of the web world.</p>
<p>In the fall of last year I toyed with Scala on Lift, and Python with Django. Setting up Scala in Netbeans and Eclipse IDEs was nontrivial for a first timer. To clarify, getting the right compilers/Jre/sdk and mixing this concept with the Google App Engine took some time to straighten out (poor Benjamin Golub was kind enough to put up with my ignorance at the time the friendfeed API v2 was released).  </p>
<p>My reliance on IDEs is another hurdle, but I far prefer rich IDEs for code navigation to editors and makefiles (I started coding on SGI unix, VI and emacs are not the ideal coding tools for me). I was clueless how to tweak the sample code frameworks besides obvious logical hints in the code structure. I judge a language by how much sense it makes to me when looking at sample code. If I have to pour over documentation to clarify dense arcane syntax, it's a bad sign, although I'm becoming acclimated to hitting web docs for help.</p>
<p>Last November <a href="http://www.Twitter.com/tylergillies">Tyler</a> kicked me into learning the basics of Ruby through Rails our current framework for the <a href="http://imm.victusmedia.com/">IMM (Intelligent Media Manager)</a>. As a long time engineer who primarily did numerical/algorithm development in C++ I was a little shocked at how slow run times for interpreted languages can be. Why would anyone choose to develop in a language that was an order of magnitude or two slower? Some simple facts I was missing: </p>
<ul>
<li>for the type of web processing I do now, the wait time of remote API calls is much greater than local processing time</li>
<li>abstraction for high level languages allows for rapid construction of functioning prototypes</li>
<li>Static vs Dynamic typing: (somewhat related to interpreted and compiled languages) I prefer static typing to dynamic, as that's how I first learned. Declaring types is good practice (its built in documentation) and saves a fair amount of testing. Dynamic typing has it's own merits but I'm not the right guy to argue this topic. Someone like <a HREF="http://www.twitter.com/dpp">Dave Pollack</a> can discuss the comparison of each much better. I'll come back to it in a future post when I have more time to research trade offs (spooky animal)</li>
</ul>
<p>In contrast to the lack of need for speed with some web development languages, there are fundamental interfaces that we all want to be as responsive as possible. For these (our database and public API) we'll want things to be hypertuned. In fact if we had to, I'm confident Tyler and I could write the entire site/service over again in a natively faster language now that we've gone through it once *ducks the rock Tyler will throw at me for this comment*. </p>
<p>Ruby on Rails is a great tool for learning, developing and understating the process, data, and user flow. There's still a great deal I can learn about the language (they didn't choose dynamic typing on a whim). While working with Rails I have even learned a little JavaScript to enable users to do remote hits to the Twitter search API (we use jquery as a support lib). This was the last step for the rudimentary twitter client we now have, Social Gravity.  Our tools excel at identifying the important topics of status updates (metadata) and  puts us in a position to better invent useful search and interaction tools. </p>
<h2>Unlimited API hits aren't free</h2>
<p>The past few days I've been digging into Open Calais' API. They have another great semantic tool which we can leverage. The big plus for Calais is there 100k hits per day limit. While debugging our list processing, I've already gone beyond the Zemanta API limit of 10k. Alchemy's Orchestr8 is our goto semantic API, and it gives us 30k hit per day to work with. If necessary we can explore hitting DBPedia directly to identify our own entities from text. Relying on external tools could be more expensive than our limited revenue can practically support. It all depends on how many affiliate sales we can get per API hit. Zemanta's pricing architecture is $1200/month for 50k hits per day at the time of writing this post. Calais may be our most viable option. Even better than that, in house semantic lookups could be the best long term solution. Lower software and maintenance cost versus API hits, and in theory we could have a massive local database to minimize response time. </p>
