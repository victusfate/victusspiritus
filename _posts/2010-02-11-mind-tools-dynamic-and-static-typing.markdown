---
layout: post
status: publish
published: true
title: 'Mind => Tools, dynamic and static typing '
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3006
wordpress_url: http://www.victusspiritus.com/?p=3006
date: '2010-02-11 05:22:56 -0500'
date_gmt: '2010-02-11 12:22:56 -0500'
categories:
- Uncategorized
tags:
- far out
- coding
- design
comments:
- id: 2934
  author: Jim Dwulit
  author_email: None
  author_url: http://twitter.com/jimocz
  date: '2010-02-12 12:10:11 -0500'
  date_gmt: '2010-02-12 17:10:11 -0500'
  content: I do not agree with all the points you have made above especially the fact
    that you say dynamic typing encourages unit testing?  Why?  Is it because you
    make more errors in coding with dynamic programming?  Unit testing is a technique
    to ensure your code is as correct as possible -- I would venture that quality
    programming encourages unit testing.<br>Also I question the statement that CPU&#39;s
    view data as only binary bits.  From a programming point of view (and hardware
    design) CPUs can do integer arithmetic and floating point arithmetic -- it is
    more than bits.  Bits are to data as letters are to words, would you say that
    all words are a bunch of letters? True but you miss the forest for the trees.
- id: 2936
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-02-12 17:12:53 -0500'
  date_gmt: '2010-02-12 22:12:53 -0500'
  content: It&#39;s harder to get away without unit testing in dynamic typed languages
    (although we haven&#39;t done unit testing with <a href="http://imm.victusmedia.com"
    rel="nofollow">IMM</a>).<br><br>The CPU can&#39;t infer data types (as far as
    I know). It doesn&#39;t know what a memory location is unless it&#39;s described
    in the machine&#39;s language. Heck even we have problems understanding binary
    formats unless we have some clues.
- id: 8208
  author: Fuse
  author_email: spidermario@free.fr
  author_url: ''
  date: '2011-01-28 23:05:00 -0500'
  date_gmt: '2011-01-28 23:05:00 -0500'
  content: |-
    &gt; as long as an object has the methods used it can function within any other range of interfaces without a complex inheritance tree

    Ever heard of structural typing?
- id: 8211
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-01-29 02:45:00 -0500'
  date_gmt: '2011-01-29 02:45:00 -0500'
  content: |-
    I haven't before today. Will look into how it's done, and with what languages.
    Thanks.
---
<p><a href="http://www.victusspiritus.com/wp-content/uploads/2010/02/l_2048_1536_99CF4B03-550C-4F45-9374-8BB162C5F611.jpeg"><img src="http://www.victusspiritus.com/wp-content/uploads/2010/02/l_2048_1536_99CF4B03-550C-4F45-9374-8BB162C5F611.jpeg" alt="" width="300" height="225" class="alignnone size-full wp-image-364" /></a></p>
<p>In an earlier <a href="http://www.victusspiritus.com/2010/02/08/each-time-i-get-my-hands-dirty-i-learn/">post</a> I mentioned I'd come back to the advantages of dynamic typing. My primary reference for all the quotes and information is the <a HREF="http://en.m.wikipedia.org/wiki/Dynamic_type">dynamic type wikipedia page</a>. But if you're not very familiar with programming it can read like a spooky animal. I'll try to translate by pointing out a couple of advantages of each that relate to my personal experience.</p>
<h2>Definition of a Type System</h2>
<p>A type system describes what each block of memory is and can be thought of as metadata or descriptive information. Type information aids the interpreter or compiler to translate your brilliant code* into assembly and binaries to run on a specified platform.</p>
<p>So the essence of typing is to prevent or catch errors where data or operations are misclassified and misused. Basically, don't put the square peg in the round hole. This can happen before run time with static typed languages which are compiled. Or it can happen at run time with dynamic typed languages. <i>Maybe we'd be better off with type agnostic compilers and interpreters.</i> More on this later. </p>
<p>Why do we need run time typing at all?</p>
<blockquote><p>
Because any value simply consists of a sequence of bits in a computer, hardware makes no intrinsic distinction even between memory addresses, instruction code, characters, integers and floating-point numbers, being unable to discriminate between them based on bit pattern alone. Associating a sequence of bits and a type informs programs and programmers how that sequence of bits should be understood.
</p></blockquote>
<h2>Static typing defined</h2>
<blockquote><p>
A programming language is said to use static typing when type checking is performed during compile-time as opposed to run-time. In static typing, types are associated with variables not values. Statically typed languages include Ada, AS3, C, C++, C#, F#, JADE, Java, Fortran, Haskell, ML, Pascal, Perl (with respect to distinguishing scalars, arrays, hashes and subroutines) and Scala. Static typing is a limited form of program verification (see type safety): accordingly, it allows many type errors to be caught early in the development cycle.
</p></blockquote>
<p> The features of static typed languages are:</p>
<ul>
<li>compile time checking of correct types. But static type checks are more restrictive as they can dissallow completey acceptable code. Static type languages usually have methods around this by allowing type casting</li>
<li>built in documentation, knowing data or function type aids others in understanding code flow</li>
<li>no need to do extensive type checking in unity tests</li>
<li>specific optimizations: This allows optimization by knowing how to align memory of a certain type</li>
</ul>
<h2>Dynamic typing in a nutshell</h2>
<p>The type of nut or even that an object IS a nut isn't checked until run time.</p>
<blockquote><p>
In dynamic typing, types are associated with values not variables. Dynamically typed languages include Erlang, Groovy, JavaScript, Lisp, Lua, Objective-C, Perl (with respect to user-defined types but not built-in types), PHP, Prolog, Python, Ruby, Smalltalk and Tcl. Compared to static typing, dynamic typing can be more flexible (e.g. by allowing programs to generate types and functionality based on run-time data), though at the expense of fewer a priori guarantees
</p></blockquote>
<p>The features of dynamic typed languages are:</p>
<ul>
<li>dynamic typing gives a coder more flexibility by allowing type generation on the fly during code execution</li>
<li>as long as an object has the methods used it can function within any other range of interfaces without a complex inheritance tree (thank David Pollack's Scala post below for this point)</li>
<li>dynamic languages encourage unit testing, which can capture a wide range of errors beyond type safety (behaviorial feature?)</li>
</ul>
<h2>Conclusions</h2>
<p>Static and dynamic typing can coexist in a programming language. Coding behavior or the <i>human pattern</i> may be more important than whether a language is static or dynamically typed. Although opinions can sway strongly to one side or the other, this post on the <a href="http://www.scala-blogs.org/2007/12/scala-statically-typed-dynamic-language.html">Scala blog</a> covers the topic well.</p>
<p>Earlier I mentioned the possibility for type agnostic compilers or interpreters. A language with this feature would require a machine architecture that is capable of using handlers to process data without ever having to know what the data was or how the handlers work. Even the knowledge of whether a memory block was a handler or data would be unknown. There'd need to be a way to connect memory locations, to change other memory locations. Agnostic memory structures would create a completely <a HREF="http://en.m.wikipedia.org/wiki/Dynamic_programming_language?wasRedirected=true">dynamic language</a>.  </p>
<p>Notes:<br />
*  If you're reading this post I'm giving you the benefit of the doubt </p>
