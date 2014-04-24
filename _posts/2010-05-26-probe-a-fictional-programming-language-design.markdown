---
layout: post
status: publish
published: true
title: 'Probe: A fictional programming language'
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3967
wordpress_url: http://www.victusspiritus.com/2010/05/26/probe-a-fictional-programming-language-design/
date: '2010-05-26 08:06:05 -0400'
date_gmt: '2010-05-26 15:06:05 -0400'
categories:
- Uncategorized
tags:
- leadership
- coding
- probe
- design
comments:
- id: 4412
  author: iamronen
  author_email: iamronen@iamronen.com
  author_url: http://www.iamronen.com
  date: '2010-05-26 16:10:37 -0400'
  date_gmt: '2010-05-26 21:10:37 -0400'
  content: 'This isn&#39;t "my kind of post" to relate to ... but I think it&#39;s
    imperative you watch this inspiring video: <br><a href="http://video.google.com/videoplay?docid=-533537336174204822#"
    rel="nofollow">http://video.google.com/videoplay?docid=-533537...</a><br><br>Inside
    you will find, amongst other things, an animation that a young girl with no official
    training programmed!!! in the early days of computers ... I think Alan Kay was
    trying to suggest heading in the direction you want to go ... I am sure this will
    open up to you pas experiences and new avenues to explore!'
- id: 4421
  author: Sri
  author_email: sri.panyam@gmail.com
  author_url: http://panyam.wordpress.com
  date: '2010-05-27 01:21:54 -0400'
  date_gmt: '2010-05-27 06:21:54 -0400'
  content: Hi<br><br>    Very interesting.  Have you seen the chuck programming language
    that came out of Princeton university?  What you describe is very similar to what
    Ge Wang (the author of Chuck) has implemented.<br><br><a href="http://chuck.cs.princeton.edu/"
    rel="nofollow">http://chuck.cs.princeton.edu/</a><br><br>cheers<br>Sri
- id: 4427
  author: Transient Technology, how probe may handle interface mapping - Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/05/28/transient-technology-how-probe-may-handle-interface-mapping/
  date: '2010-05-28 06:29:57 -0400'
  date_gmt: '2010-05-28 13:29:57 -0400'
  content: "[...] couple of days ago I described the beginning of a top down designed
    programming language, probe. This design effort is defined by what I want as an
    application builder first, with only a hint of [...]"
- id: 4451
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-06-03 22:06:18 -0400'
  date_gmt: '2010-06-04 03:06:18 -0400'
  content: Thanks Ronen.
- id: 4452
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-06-03 23:03:26 -0400'
  date_gmt: '2010-06-04 04:03:26 -0400'
  content: Thanks Sri, I&#39;ll certainly take a look. Appreciate the related share.  <br>Could
    be helpful to see what choices they made.
---
<p>This morning's riff is a beginning for a new programming language which may end up being a dialect or library of an existing language after I take a look at what I've written. I'll begin with an example of how I'd like code to look and function, and then wrap up with some design priorities and benefits. I would like a language that makes the process of learning easier and more streamlined. Probe stands for anything you want. At the moment for me probe stands for PROgram By Essel, PROgram BE, Produce Relational Ontologies By Example, and/or Pattern Refined Organization Born Easily :).</p>
<p>The following program will access an array of numerical signals (images, sound clips, etc) and identify an array of signal parameters. The specific example will be a list of images from the web.</p>
<pre>

[url1, url2, url3] => Stats</pre>
<p>The brackets suggest a collection of things to be handled by the Stats object. The => isn't quite a passing operator. What it means is map what's on the left into the inputs of what's needed on the right. I like to think of it as the handshake, I hold out my hand and you figure out a way to shake it. A default flow will take priority if there are multiple mappings possible (with a warning?) and if no mappings are possible an error is raised and a doomsday countdown is initiated*.</p>
<h2>Implicit Loops</h2>
<p>Lets keep inventing as we go by looking into the Stats code.</p>
<pre>

Stats
     init( sig, proc )
         sig => proc > xout
     end
 end

</pre>
<p>Note that sig and proc can both be collections. The interpreter/compiler will determine if sig or proc are collections and expand code as needed. When doing automated tasks with programs, we tend to work with sets of things and run them all. We also want it to be trivial to process subsets when desired. My motto: <em>Get our hands dirty now with a little upfront work to provide elegant readability to ourselves time and again later on.</em> Can reading code be fun? I think so!</p>
<p>So<br />
sig => proc > xout<br />
Is equivalent to:</p>
<pre> 

sig.each x
     proc.each y
         x => y >> xout
     end
 end

</pre>
<p>Let's spend some time looking at collections of collections. xout should have easy single index or multiple index access. The trick is that the output collection structure is determined by the looping on the fly.<br />
So both xout.flat[0] and xout[0][0] are the result of<br />
sig[0] => proc[0]<br />
and xout.flat[1] and xout[0][1] are the result of<br />
sig[0] => proc[1] assuming there are at least two processes</p>
<h2>a * is born</h2>
<p>Finding all the results in x that are processed sig[0] is easy, it's just xout[0]<br />
Want to find all results in x that are processed by proc[0]?<br />
xout[*][0]<br />
It's incredibly liberating writing a programming language based on how I want it to be used without any concern for the hell I'll have to go through later to implement it. In a moment of need, a wild card is brought into the probe language. And of course xout[0][*] is the same as xout[0] in this simple 2D example. For higher dimensions this is not the case.</p>
<h2>Process Subsets</h2>
<p>Only want to process a subset?<br />
Try<br />
sig[0] => proc > xout<br />
Or<br />
sig[0] => proc[0]<br />
there's also .first and .last access methods for collections so<br />
sig[0] is sig.first and<br />
sig.last is sig[sig.dim-1]</p>
<p>I like the idea of allowing symmetry in the data/processing flow if it's not too tricky to parse. So that:<br />
x => proc > xout<br />
is equivalent to<br />
xout < proc <= x<br />
The assignment operator = is the equivalent of a <, but not > (equals only works by assigning left).<br />
So:<br />
xout = proc <= x<br />
and:<br />
xout < proc <= x<br />
are equivalent.</p>
<p>Let's dig a layer deeper with the process object</p>
<pre>

Norm : Process
     init sig
         sig => go > xout
     end
     operator <= sig          
         sig.vector      
     end      
     go sig          
         sig => Std > xout
         sig => Sub(xout.mean) > temp
         temp => Div(xout.sigma) >> xout
     end
 end
</pre>
<p><strong>init</strong> is a standard constructor name.<br />
Add, Sub, Mult, Div, Std (Standard Deviation), and Norm (Sigma Normalization) are all standard library operators which can be overloaded and customized (all derive from Process, single inheritance as in Ruby is groovy with modules/mixins)</p>
<h2>Benefits of the Language</h2>
<p>There are many existent languages which share some or all of the aspects I'll outline below (i.e. Lisp is close), but there is a level of intimacy that comes from writing your own language that I wish to explore. The path forward is to imagine how it would look and work, and then back fill in the details as needed. Some high level language design priorities:</p>
<ul>
<li>dynamic language to encourage meta programming. I desire a very flexible language</li>
<li>dynamically typed objects, where just about everything is an object (like Ruby)</li>
<li>syntactical brevity and clarity. It will be a pleasure to develop with and read later</li>
<li>easy to begin using, but flexible and complex enough for experience hackers</li>
<li>high level functionality and a rich default utility library</li>
<li>has competitive implementation benchmarks with other "fast" programming languages (c, c++, java)</li>
<li>asynchronous flexibility with optional high priority blocking synchronous code sections. Ideally the language can identify the optimal allocated level of concurrency  and use threaded resources</li>
</ul>
<p>This is a top down approach to programming language design. None of the backend or implementation has been written nor have I have spent much time thinking over the advantages of JVM implementations, a C/Assembly backend, vs a dialect of Lisp.</p>
<p>Notes:<br />
*= Not enough severe negative reinforcement is used in programming. Probe seeks to rapidly enhance best coding practices ;).</p>
