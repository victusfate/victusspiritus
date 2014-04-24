---
layout: post
status: publish
published: true
title: Exploring speculative execution and evaluation
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5333
wordpress_url: http://www.victusspiritus.com/?p=5333
date: '2010-10-02 14:55:29 -0400'
date_gmt: '2010-10-02 21:55:29 -0400'
categories:
- Uncategorized
tags:
- coding
- ruby
- llvm
comments: []
---
<p>Consider a simple search problem with multiple paths. The main processing path can be computed in series as required functionality is identified. Completion occurs whenever an adequate solution is found. Alternatively, potential paths can be searched in batches or all simultaneously ahead of time**. This diminishes the wait for required functionality at the cost of additional processing, some of which may never be necessary. We trade computation power for statistically lower execution time.</p>
<p>Speculative execution is a time saving technique used in code execution. The method extrapolates what may be required, executes those branches, and generates intermediate results which are used for required computation paths as needed. Resources are risked on branches that may never be needed so their judicious use is required to maintain efficiency (power concerns, etc). Let's hit the ground running with an example of how <a href="http://en.m.wikipedia.org/wiki/Speculative_execution">speculative execution</a> is used in practice. </p>
<blockquote><p>
Modern pipelined microprocessors use speculative execution to reduce the cost of conditional branch instructions. When a conditional branch instruction is encountered, the processor guesses which way the branch is most likely to go (this is called branch prediction), and immediately starts executing instructions from that point. If the guess later proves to be incorrect, all computation past the branch point is discarded
</p></blockquote>
<p><i>Conditions for Compiler Optimization</i></p>
<p>As an eternal sophomore of software^, I've encountered quite a few technical presentations on compiler optimization which leave me baffled. I've become familiar with many design motivations, but docs regularly refer to vocabulary which I don't understand. This leads to never ending web reading sessions. In the beginning my confusion began with references to <a href="http://en.wikipedia.org/wiki/Functional_programming">functional programming</a> and <a href="http://en.wikipedia.org/wiki/Lazy_evaluation">lazy evaluation</a>. Since first encountering these terms, I've become more comfortable with their meaning, transcending the <a href="http://www.victusspiritus.com/2010/02/08/each-time-i-get-my-hands-dirty-i-learn/">spooky animal phase</a>. Lazy evaluation is simply delayed computation until a result is required. Pure functional programs eliminate all intermediary variables by limiting the syntax to describing operations. In practice functions which don't have side affects are <em>dazy chained</em> together to result in values*.</p>
<p>Functional programming enable compilers to optimize calculations using techniques like <a href="http://en.wikipedia.org/wiki/Deforestation_(computer_science)">deforestation</a>. Having context for these terms is necessary to achieve introductory comprehension of compiler design.<br />
[caption id="attachment_5335" align="aligncenter" width="425" caption="no, not this kind of deforestation"]<a href="http://www.victusspiritus.com/wp-content/uploads/2010/10/deforestation-tree-removal.jpg"><img class="size-full wp-image-5335" title="deforestation-tree-removal" src="http://www.victusspiritus.com/wp-content/uploads/2010/10/deforestation-tree-removal.jpg" alt="" width="425" height="282" /></a>[/caption]</p>
<p>Another regularly used term is JIT or just in time compilation. This architecture blends compilation and continuous interpretation for maximum efficiency. I touched briefly on <a href="http://www.victusspiritus.com/2010/04/03/ideal-coding-easy-to-pickup-yet-abundant-in-function/">just in time compiling</a> when predicting changes to programming in the coming years. </p>
<p><i>LLVM</i></p>
<p>One large project I can't help but cross paths with while researching compiler optimization is the <a href="http://llvm.org/docs/">LLVM</a> or low level virtual machine. Here's a <a href="http://llvm.org/pubs/2008-10-04-ACAT-LLVM-Intro.html">great introduction by Chris Lattner</a>, the primary author of the project. It's an ambitious project to provide compile time, link time, run time, and idle time optimization of programs from arbitrary programming languages.</p>
<p>To see the LLVM in action I've included a presentation on leveraging the LLVM to execute Ruby (Rubinius) by Evan Phoenix:</p>
<div id="__ss_2148169" style="width: 425px;"><strong><a title="Accelerating Ruby with LLVM" href="http://www.slideshare.net/evanphx/accelerating-ruby-with-llvm">Accelerating Ruby with LLVM</a></strong><object id="__sse2148169" classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="425" height="355" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="allowFullScreen" value="true" /><param name="allowScriptAccess" value="always" /><param name="src" value="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=llvmdevmeeting2-091006203334-phpapp01&amp;stripped_title=accelerating-ruby-with-llvm&amp;userName=evanphx" /><param name="name" value="__sse2148169" /><param name="allowfullscreen" value="true" /><embed id="__sse2148169" type="application/x-shockwave-flash" width="425" height="355" src="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=llvmdevmeeting2-091006203334-phpapp01&amp;stripped_title=accelerating-ruby-with-llvm&amp;userName=evanphx" name="__sse2148169" allowscriptaccess="always" allowfullscreen="true"></embed></object>
</div>
<p>I'll leave off with a more recent <a href="http://www.engineyard.com/blog/2010/making-ruby-fast-the-rubinius-jit/">post by Evan</a> on how Ruby is designed to run fast with Rubinius and take advantage of the LLVM.</p>
<p>Notes:<br />
** = are quantum computers a flavor of speculative execution? The search analogy could use some work, as I reread it, I've comparing series versus parallel execution not quite required versus potentially required processing.</p>
<p>^ = It's posts like these where I wish I had a fraction of the low level compiler understanding of master engineer, <a href="http://codingrelic.geekhold.com/">Denton Gentry</a> who's fluent with the <a href="http://codingrelic.geekhold.com/2010/07/virtual-instruction-sets-opcode.html">topic of virtual machines</a>.</p>
<p>* = The web definition supplement to my laymen understanding:</p>
<blockquote>
<ul>
<li>A method of writing programs that describes only the operations to be performed on the inputs to the programs, without the use of temporary variables to store intermediate results</li>
<li>In computer science, functional programming is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids state and mutable data.</li>
</ul>
</blockquote>
