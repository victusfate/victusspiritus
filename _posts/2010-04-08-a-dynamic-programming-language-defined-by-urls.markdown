---
layout: post
status: publish
published: true
title: A Dynamic Programming Language Defined by URLs
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3522
wordpress_url: http://www.victusspiritus.com/2010/04/08/a-dynamic-programming-language-defined-by-urls/
date: '2010-04-08 04:55:04 -0400'
date_gmt: '2010-04-08 11:55:04 -0400'
categories:
- Uncategorized
tags:
- coding
- javascript
- design
- coffeescript
comments:
- id: 3844
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-04-08 19:11:06 -0400'
  date_gmt: '2010-04-09 00:11:06 -0400'
  content: 'Here&#39;s an interesting find: <a href="http://ukijs.org/" rel="nofollow">Uki</a>
    which looks somewhat like jQuery-UI. I spotted there <a href="http://github.com/voloko/uk"
    rel="nofollow">mail app</a> on HackerNews.<br><br>Here&#39;s <a href="http://github.com/voloko/uk"
    rel="nofollow">Uki</a> on github.'
- id: 3853
  author: James Fuller
  author_email: jimminyfuller@gmail.com
  author_url: http://theinnovationist.com/
  date: '2010-04-09 02:59:05 -0400'
  date_gmt: '2010-04-09 07:59:05 -0400'
  content: Mark, I agree that sometimes a dev environment is a horrible PITA to setup,
    I keep all my dev files together, but I had to reformat a few months ago, and
    gave up after 3 days of no success. Luckily, I went back about a week later, and
    it took about 90 minutes, and everything was ready to go. <br><br>I now compare
    dev/env setup to be just like a problem you might need to sleep on to solve it,
    if you keep trying to work it out, you&#39;re just wasting energy, going in circles.
- id: 3859
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-04-09 09:05:32 -0400'
  date_gmt: '2010-04-09 14:05:32 -0400'
  content: Thanks for empathizing Jim. <br><br>I feel spoiled when I hop onto my desktop
    or phone and start editing JavaScript and it just works. If it was a little more
    compressed (syntax) and easier for non programmers to get into, it could be the
    most popular programming language (maybe it is already?)
- id: 4080
  author: Instant Utility, Optimal Execution, &amp; Syntactic Sugar &laquo; Victus
    Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/04/20/instant-utility-optimal-execution-syntactic-sugar/
  date: '2010-04-20 07:04:54 -0400'
  date_gmt: '2010-04-20 14:04:54 -0400'
  content: "[...] JavaScript translations of Ruby (Red &amp; RubyJS) bring ruby to
    every machine with a JavaScript enabled web browser. These translations are able
    to [...]"
- id: 9907
  author: ''
  author_email: peternakah@gmail.com
  author_url: ''
  date: '2011-05-05 19:22:00 -0400'
  date_gmt: '2011-05-05 19:22:00 -0400'
  content: There are many best advantageous libraries accessible for JavaScript which
    can be referenced by including the URL of the source.
- id: 9908
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-05 19:33:00 -0400'
  date_gmt: '2011-05-05 19:33:00 -0400'
  content: "thanks for commenting. I found out since then, and rely on a few of them
    regularly, including my own in recent posts. see folding in c++, I leverage remote
    javascript to alter the size of embedded gists.\r\n\r\nThis weekend I plan on
    digging into coffeescript and node with tutorials. It's a pleasure to read with
    a rich set of utilities."
---
<p>One of the problems with modern programming languages is heavy installation. Last year I tried convincing a friend to learn some modern programming languages with me, and we couldn't get his dev environment to work. He gave up after a couple of days, and I didn't know about the adobe meeting/screen share tool at the time to walk him through setup. </p>
<p>More often than not there's no one click setup. In fact, if you plan on doing any serious work, setup of all required development tools can be quite involved. A recurring question haunts me, why are such great tools hidden behind walls of detailed installation? As a sample point here's a list of some of the development tools I installed over the past few months (at home and at work): </p>
<blockquote><p>
Java Virtual Machine, Java SDK, Ruby MRI 1.8.6-1.9.1, enough gems to be rich 10X over- many which required compilation, JRuby, Rubinius, Duby, Python, Perl, Google App Engine SDK (Python+Java), MongoDB (we moved to sqlite3), Aptana Studio & Aptana Radrails, Eclipse Galaxy + Pluggins, Netbeans + Pluggins, git, Tortoise Git, DiffMerge, Wine, VirtualBox, VMware, and a few browsers with Firebug - Firefox, Chrome, Chromium (work security dissallows Chrome due to some 2008 vulnerability, but allows GPL so Chromium's kosher - long story).
</p></blockquote>
<p>I'm sure there's plenty more that I'm forgetting at the moment. Not all of these tools install smoothly, although most install much faster and with less complaints on Linux (versus Windows). Of course I don't use all these tools every day, but when a need arises I install the tool. In doing so I die the death of a thousand paper cuts. When I choose to setup a new development environment or change language interpreters it can take significant time to shake out all the conflicts. In fact the time cost is large enough that I tend to use inferior utilities in lieu of system wide upgrade time. My favorite feautures are ease of reading, highly functional core installations (rich default lib), and always available.</p>
<h2>Solutions & Ideas</h2>
<p>I have visited a number of sites that have input windows which allow code entry and perform interpretation and execution. But the input source and run time is limited, there's no way to control installed resources, and the output format is highly constrained. Regardless these interfaces are fantastic for learning, and are part of the inspiration for this programming idea.</p>
<h2>A Web & Browser Based Language</h2>
<p>In a short time I've been impressed with Javascript. Although the syntax isn't as pleasing to the eye as Ruby, it wouldn't take much to slap a prettier front end on it^. This dynamic language is readilly available in all browsers, and is currently being optimized by one of the most influential companies on the planet* in unison with the open source community. There are several highly useful libraries available for JavaScript (jQuery, jQuery-UI, Prototype) which can be referenced by including the URL of the source (usually in a compressed format .min). </p>
<p>What value would a derivative language of JavaScript with a rich default library, and syntactical feel/ease of use of Ruby be? I'd lose all the functionality of gems unless there were a translator. I'd still need to identify each libraries URL in a header structure. A way around this would be a distributed lookup system in the interpreter that would search for unknown unique identifers (URLs/subdomain URLs?) and pull in libraries as needed just in time, or just ahead of time inclusion with a quick first pass. It'd save me gratuitous installation time, at the cost of optimal run time. Interpreted dynamic languages can't execute as fast as compiled code unless their flexibility is reduced in bottleneck flow points, using a just in time or predictive compilation model. There's nothing in this proposed language preventing such implementations. </p>
<p>note:<br />
* Google's help with JavaScript interpretation and execution is orders of magnitude faster than several other browsers. I expect to see theirs and the open source Chromium browsers work spread into other browsers<br />
^ CoffeeScript looks somewhat Python or Ruby like</p>
<p>Updates:<br />
<a href="http://wonderfullyflawed.com/2008/10/13/red-40-a-full-ruby-runtime-in-your-browser/">Red 4.0</a> is a full implementation of Ruby in the browser. I have to check it out asap. </p>
<p>Here's an interesting find: <a href="http://ukijs.org/">Uki</a> which looks somewhat like jQuery-UI. I spotted there <a href="http://github.com/voloko/uk">mail app</a> on HackerNews.</p>
<p>Here's <a href="http://github.com/voloko/uk">Uki</a> on github.</p>
<p>Another Update:<br />
The creator and lead developer of jQuery, John Resig wrote a <a HREF="http://ejohn.org/blog/ruby-vm-in-javascript/">blog post</a> about a Ruby implementation using JavaScript: <a href="http://hotruby.yukoba.jp/">HotRuby.js</a>.but the rich default Ruby library wasn't fully developed, and porting over gems will take some collaborative effort. But it looks plausible.</p>
