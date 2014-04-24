---
layout: post
status: publish
published: true
title: Unraveling the Knots of Implementation Benchmarks
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7288
wordpress_url: http://www.victusspiritus.com/?p=7288
date: '2011-02-18 11:04:27 -0500'
date_gmt: '2011-02-18 18:04:27 -0500'
categories:
- Uncategorized
tags:
- coding
comments:
- id: 8981
  author: igouy
  author_email: igouy2@yahoo.com
  author_url: ''
  date: '2011-02-18 20:31:00 -0500'
  date_gmt: '2011-02-18 20:31:00 -0500'
  content: |-
    &gt;&gt;Alioth’s shootouts (debian linux)&lt;&lt;

    That&#039;s like saying Sourceforge&#039;s MySQL - Alioth provides free project hosting, Alioth isn&#039;t responsible for what the projects do.

    The project name changed nearly 4 years ago - http://shootout.alioth.debian.org/help.php#namegame

    The measurements are not made on debian linux - http://shootout.alioth.debian.org/help.php#os
- id: 8982
  author: igouy
  author_email: igouy2@yahoo.com
  author_url: ''
  date: '2011-02-18 20:39:00 -0500'
  date_gmt: '2011-02-18 20:39:00 -0500'
  content: |+
    &gt;&gt;A processing benchmark is more meaningful when coupled with a memory comparison.&lt;&lt;

    Do you know that memory use is shown on the benchmarks game?

    http://shootout.alioth.debian.org/u64/which-language-is-best.php?calc=chart&amp;yarv=on&amp;tracemonkey=on&amp;v8=on&amp;luajit=on&amp;xfullcpu=0&amp;xmem=1&amp;xloc=0&amp;nbody=1&amp;fannkuchredux=1&amp;meteor=0&amp;fasta=1&amp;spectralnorm=1&amp;revcomp=1&amp;mandelbrot=1&amp;knucleotide=1&amp;regexdna=1&amp;pidigits=1&amp;chameneosredux=0&amp;threadring=0&amp;binarytrees=1


    http://shootout.alioth.debian.org/u64/performance.php?test=mandelbrot&amp;sort=kb



- id: 8983
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-02-18 21:56:00 -0500'
  date_gmt: '2011-02-18 21:56:00 -0500'
  content: |-
    Thanks for the reality mangling correction and pointing out how to easily pull out memory utilization from the Computer Language Benchmarks Game. Updated the post w/ corrects. Being wrong on the net is so much better than living in a delusional reality :)

    ps you'd think seeing Ubuntu on every page would have been a subtle hint I could have recognized.
- id: 8984
  author: igouy
  author_email: igouy2@yahoo.com
  author_url: ''
  date: '2011-02-19 02:08:00 -0500'
  date_gmt: '2011-02-19 02:08:00 -0500'
  content: "Thanks for making the update.  \n\nIt isn't unusual not to notice banner
    text - every page says Computer Language Benchmarks Game but many don't notice.\n\nIt
    isn't unusual to misread web page text - we don't really read them, we just glance
    at them for a few seconds.\n\n"
---
<p><i>Update: The greatest part about being obviously and publicly wrong is that smart folks are generous about pointing out the truth atrocities commited. Thanks to igouy for corrections. My brain mangled the domain into a source and OS, and that's been corrected below.</i></p>
<p>One of the biggest gains that can be achieved with any specific implementation, independent of the language(s) it is written in, is having experts spend time profiling and optimizing system performance (<a href="http://shootout.alioth.debian.org/dont-jump-to-conclusions.php">don't jump to conclusions</a>). That said there are broad language implementation based comparisons that can be made between standard benchmarks.</p>
<p>I spent some time this morning reading over variations in dynamic language implementations (mainly Ruby, Lua, Javascript) by digging into <a href="http://shootout.alioth.debian.org/">shootouts (The Computer Language Benchmarks Game)</a> (<strike>debian</strike> <strong>ubuntu</strong> linux). I wanted to get a feel for execution times between languages overall (vague) and for specific algorithms. You can think of the latest GCC compiler of c/c++ as the gold standard of execution speed for benchmarks, and they help frame other run times (ie just as fast, almost as fast, way freakin' slower).</p>
<p>The single core results show various speeds as a multiple of the fastest run times:</p>
<pre>1 = fastest
63.17 = ruby :(</pre>
<p>Fortunately for my own needs the types of optimization I have to worry about at home are mostly data shuffling and not very sensitive to computation times. At work we have mixed sensitivity to processing speed and memory handling since most of our data is localized. For a handful of specific benchmarks check the end of this post.<br />
<a href="http://shootout.alioth.debian.org/u64/which-programming-languages-are-fastest.php"><img class="aligncenter size-full wp-image-7318" title="singlecore" src="http://www.victusspiritus.com/wp-content/uploads/2011/02/singlecore1.png" alt="" width="535" height="651" /></a></p>
<p>One of the benchmark comparisons that piqued my interest shed further light on the question, <em>who is the fastest Javascript interpreter V8 or TraceMonkey?</em> V8 edges TraceMonkey out in most tests but is twice as slow for the n-body benchmark (<a href="http://www.victusspiritus.com/2010/11/06/the-fall-of-icarus/">gravity is a harsh mistress</a>).<br />
<a href="http://shootout.alioth.debian.org/u64/benchmark.php?test=all&amp;lang=v8&amp;lang2=tracemonkey"><img class="aligncenter size-full wp-image-7300" title="v8_vs_tracemonkey" src="http://www.victusspiritus.com/wp-content/uploads/2011/02/v8_vs_tracemonkey.png" alt="" width="475" height="352" /></a></p>
<p>And a box chart with LuaJIT and Ruby added:<br />
<a href="http://shootout.alioth.debian.org/u64/which-programming-languages-are-fastest.php?calc=chart&amp;luajit=on&amp;v8=on&amp;tracemonkey=on&amp;yarv=on"><img class="aligncenter size-full wp-image-7301" title="luajit_v8_tracemonkey_ruby1.9" src="http://www.victusspiritus.com/wp-content/uploads/2011/02/luajit_v8_tracemonkey_ruby1.9.png" alt="" width="500" height="310" /></a></p>
<p>I moved on to more specific Ruby comparisons next to see how various implementations were coming along with respect to completeness and performance. <a href="http://programmingzen.com/2010/07/19/the-great-ruby-shootout-july-2010/">The Great Ruby Shootout</a> captures a look at execution between 8 Ruby implementations:</p>
<ul>
<li>Ruby 1.8.7 p299</li>
<li>Ruby 1.9.1 p378</li>
<li>Ruby 1.9.2 RC2</li>
<li>IronRuby 1.0 (Mono 2.4.4)</li>
<li>JRuby 1.5.1 (Java HotSpot(TM) 64-Bit Server VM 1.6.0_20)</li>
<li>MagLev (rev 23832)</li>
<li>Ruby Enterprise Edition 2010.02</li>
<li>Rubinius 1.0.1</li>
</ul>
<p style="text-align: center;"><a href="hhttp://programmingzen.com/2010/07/19/the-great-ruby-shootout-july-2010/"><img class="aligncenter size-full wp-image-7296" title="greatrubyshootout" src="http://www.victusspiritus.com/wp-content/uploads/2011/02/greatrubyshootout.png" alt="" width="556" height="520" /></a></p>
<p>A processing benchmark is more meaningful when coupled with a memory comparison*. As you can see from the below chart JRuby is the heaviest hitter when it comes to memory with the interpreters (1.8.7, 1.9.1 &amp; 1.9.2) being rather lean.</p>
<p style="text-align: center;"><a href="http://www.victusspiritus.com/wp-content/uploads/2011/02/greatshootoutruby_memory.png"><img class="aligncenter size-full wp-image-7303" title="greatshootoutruby_memory" src="http://www.victusspiritus.com/wp-content/uploads/2011/02/greatshootoutruby_memory.png" alt="" width="547" height="513" /></a></p>
<pre>
-------------------------------------------------------------------
</pre>
<p>Notes:<br />
* = Thanks to commenter ugouy for pointing out that memory utilization is easily pulled out of the the benchmarks game: ie the <a href="http://shootout.alioth.debian.org/u64/performance.php?test=mandelbrot&sort=kb">mandelbrot benchmark's memory usage</a>. </p>
<p><strong>Additional reference: A handful of specific benchmarks from <a href="http://shootout.alioth.debian.org">http://shootout.alioth.debian.org</a></strong><br />
To get specific times and information about the benchmark click through the image.</p>
<p>n-body<br />
<a href="http://shootout.alioth.debian.org/u64/benchmark.php?test=nbody&amp;lang=all"><img class="aligncenter size-full wp-image-7323" title="nbody" src="http://www.victusspiritus.com/wp-content/uploads/2011/02/nbody.png" alt="" width="496" height="303" /></a><br />
fasta<br />
<a href="http://shootout.alioth.debian.org/u64/benchmark.php?test=fasta&amp;lang=all"><img class="aligncenter size-full wp-image-7322" title="fasta" src="http://www.victusspiritus.com/wp-content/uploads/2011/02/fasta.png" alt="" width="495" height="305" /></a></p>
<p>spectral-norm<br />
<a href="http://shootout.alioth.debian.org/u64/benchmark.php?test=spectralnorm&amp;lang=all"><img class="aligncenter size-full wp-image-7321" title="spectral_norm" src="http://www.victusspiritus.com/wp-content/uploads/2011/02/spectral_norm.png" alt="" width="493" height="303" /></a></p>
<p>mandlebrot fractal<br />
<a href="http://shootout.alioth.debian.org/u64/benchmark.php?test=mandelbrot&amp;lang=all"><img class="aligncenter size-full wp-image-7320" title="mandelbrot_fractal" src="http://www.victusspiritus.com/wp-content/uploads/2011/02/mandelbrot_fractal.png" alt="" width="494" height="306" /></a></p>
<p>binary trees<br />
<a href="http://shootout.alioth.debian.org/u64/benchmark.php?test=binarytrees&amp;lang=all"><img class="aligncenter size-full wp-image-7319" title="binary_trees" src="http://www.victusspiritus.com/wp-content/uploads/2011/02/binary_trees.png" alt="" width="497" height="306" /></a></p>
