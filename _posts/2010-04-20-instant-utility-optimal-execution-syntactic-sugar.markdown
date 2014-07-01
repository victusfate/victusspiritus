---
layout: post
status: publish
published: true
title: Instant Utility, Optimal Execution, & Syntactic Sugar
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3642
wordpress_url: http://www.victusspiritus.com/?p=3642
date: '2010-04-20 05:05:15 -0400'
date_gmt: '2010-04-20 12:05:15 -0400'
categories:
- Uncategorized
tags:
- coding
- design
comments:
- id: 4086
  author: Dave Pinsen
  author_email: impossibledistances@yahoo.com
  author_url: http://steamcatapult.com/
  date: '2010-04-21 09:03:11 -0400'
  date_gmt: '2010-04-21 14:03:11 -0400'
  content: I contacted Engine Yard before having my developers use their host. I didn&#39;t
    like how the Engine Yard saleswoman wouldn&#39;t give me a clear price quote on
    their hosting services up front. I assume they were more straightforward with
    you guys, since you decided to go with them.
- id: 4087
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-04-21 10:40:42 -0400'
  date_gmt: '2010-04-21 15:40:42 -0400'
  content: 'I found the website, then Tyler checked it out and signed up. I don&#39;t  <br>think
    we&#39;ve ever talked to anyone there yet. We end up paying ~$70/ <br>month, and
    paid the same at Rackspace but EngineYard is even easier to  <br>use: no need
    to run Phusion Passenger as a web server, leaner memory  <br>usage, easy environment
    setup.<br><br>If Google App Engine was a little rails friendlier we would have  <br>swapped
    but there are all kinds of limitations/delays. Tyler is  <br>messing with some
    super efficent Erland server configurations now.'
- id: 4104
  author: Dave Pinsen
  author_email: impossibledistances@yahoo.com
  author_url: http://steamcatapult.com/
  date: '2010-04-21 23:39:57 -0400'
  date_gmt: '2010-04-22 04:39:57 -0400'
  content: That&#39;s not a bad deal. If they quoted me that, I would have had a decision
    to make. But they didn&#39;t quote me any numbers.
- id: 4615
  author: Welcome to Ruby, Javascript and Ubuntu Linux Ben | Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/06/26/welcome-to-ruby-javascript-and-ubuntu-linux-ben/
  date: '2010-06-26 04:28:11 -0400'
  date_gmt: '2010-06-26 11:28:11 -0400'
  content: "[...] Instant Utility, Optimal Execution, &amp; Syntactic Sugar (victusspiritus.com)
    [...]"
- id: 4664
  author: Is there a Moore&#8217;s Law for Machine Intelligence? | Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/07/03/is-there-a-moores-law-for-machine-intelligence/
  date: '2010-07-03 03:34:57 -0400'
  date_gmt: '2010-07-03 10:34:57 -0400'
  content: "[...] and just in time (or ahead of time) compiling, sharp developers
    are converging on a balance between optimal performance and ease of use along
    with [...]"
---
<p>As I have done all too regularly over the  past few weeks, I awoke at 4am with run time and code style anxiety. Some might label this a case of <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/04/03/ideal-coding-easy-to-pickup-yet-abundant-in-function/">premature optimization</a>, because I'm worried about execution time and readability of code I haven't written yet. Heedless of that concern, I grabbed my phone and lowered the brightness to avoid waking Michelle. I then desparately scowered the web for a Ruby interpreter or compiler that runs as fast or faster than native C (on x86 or 64bit architectures) or speedy Java byte code. As you can imagine, I've had limited success for heavy numeric applications, but there is hope.</p>
<p>My explorations have lead me to learn more about the background of both Scala and Duby (more of a Java syntax translator) to see how they've leveraged the JVM with static languages that are expressive and fast. Scala has many attractive features while Duby is a lean and mean Ruby looking front end to Java. My design inclination is to lean heavily in favor of dynamic typing and languages, which are natural fits to interpreted solutions. Unfortunately interpreters tend to be slower than compiled counterparts for heavy computations (there are exceptions).</p>
<p>Recent readings introduced me to Lisp, particularly Paul Graham's dialect Arc, and the community variant Anarki. There is much to learn about the structure and flow of code, and language tools built into the language. I could do without the heavy parentheses (YMMV) but the language appears to include much of what I'm looking for:</p>
<ul>
<li>dynamic</li>
<li>speedy</li>
<li>easy to read, but not anywhere near Ruby readability</li>
</ul>
<h2>Dynamic Ruby Approaches</h2>
<p>I've read sufficient details about JRuby and Rubinius (both supported by our company <a href="http://victusmedia.com">Victus Media</a>'s host <a href="http://www.engineyard.com/">EngineYard</a>) to be impressed by the creativity of their project leads and supporters, but dismayed at the complexity of just in time and/or ahead of time compilers in parallel threads. The trends indicate initial work for Ruby compilers, interpreters, or translation efforts result in dramatic speed ups, then slows as more of the rich default structures are implemented. Based on <a href="http://blog.headius.com/2010/03/jruby-startup-time-tips.html">performance of JRuby with options turned off</a>, I smell a hidden knee in that compatibility curve. Or in English, there may be a good enough implementation of the Ruby language to run something Rails-like in production, be ultra fast, and have 80-90% of the utility. For many products cutting out 20% utility dramatically slashes resource costs, and makes it an irresistable value offer.  I suspect the same goes with open source languges. We must carefully weigh the impact of each feature implemented on the overall performance of the language.</p>
<h2>Tradeoffs between speed, setup, and updating</h2>
<p>The JavaScript translations of Ruby (<a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/04/08/a-dynamic-programming-language-defined-by-urls/">Red &amp; RubyJS</a>) bring ruby to every machine with a JavaScript enabled web browser. These translations are able to leverage JavaScript optimizations as well as cross server dynamic code inclusion. Execution speed may be exchanged to obviate the requirement of installing local gems. Remote code can be referenced/checked for updates or default to local cached versions, enabling as required or dynamic updates.</p>
