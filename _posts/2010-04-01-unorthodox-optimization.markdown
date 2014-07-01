---
layout: post
status: publish
published: true
title: Unorthodox Optimization
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3419
wordpress_url: http://www.victusspiritus.com/?p=3419
date: '2010-04-01 06:31:27 -0400'
date_gmt: '2010-04-01 13:31:27 -0400'
categories:
- Uncategorized
tags:
- web/tech
- coding
- design
comments:
- id: 3735
  author: 'Victus Spiritus &raquo; Blog Archive &raquo; Ideal Coding: Easy to Pickup
    Yet Abundant in Function'
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/04/03/ideal-coding-easy-to-pickup-yet-abundant-in-function/
  date: '2010-04-03 05:50:39 -0400'
  date_gmt: '2010-04-03 12:50:39 -0400'
  content: "[...] I took away from my morning readings is that unorthodox optimization
    is already happening. People are selecting languages where they can quickly express
    themselves, and [...]"
- id: 4665
  author: Is there a Moore&#8217;s Law for Machine Intelligence? | Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/07/03/is-there-a-moores-law-for-machine-intelligence/
  date: '2010-07-03 03:35:14 -0400'
  date_gmt: '2010-07-03 10:35:14 -0400'
  content: "[...] Unorthodox Optimization (victusspiritus.com) [...]"
---
<p><a href="http://aakin.com/"><img src="{{ site.url }}/assets/2010/04/l_1024_670_587FFFED-184F-48DC-B4F9-F1FC03077E1A.jpeg" alt="" width="500" height="380" /></a></p>
<p><I>Prompted by recent reads over <a href="http://blog.headius.com/2009/04/how-jruby-makes-ruby-fast.html">JRuby tweaks</a> and <a HREF="http://ihumanable.com/blog/2010/03/micro-optimization/">micro optimizations</a> today's riff will be about a different design route.</I></p>
<h2>The Grand Daddy of Unorthodox Optimization: The Lisp Machine</h2>
<p>For a quick background on <a HREF="http://en.m.wikipedia.org/wiki/Lisp_machine?wasRedirected=true">Lisp Machines here's the wikipedia page</a>. Here's a relevant portion:</p>
<blockquote><p>
The power requirements of AI research were exacerbated by the Lisp symbolic programming language, when commercial hardware was designed and optimized for assembly- and Fortran-like programming languages. At first, the cost of such computer hardware meant that it had to be shared among many users. But as integrated circuit technology shrank the size and cost of computers in the 1960s and early 1970s, and the memory requirements of AI programs started to exceed the address space of the most common research computer, the DEC PDP-10, researchers considered a new approach: a computer designed specifically to develop and run large artificial intelligence programs, and tailored to the semantics of the Lisp programming language. To keep the operating system (relatively) simple, these machines would not be shared, but would be dedicated to a single user
</p></blockquote>
<p>After reading up on Lisp machines the idea of optimized hardware for our favorite software or development language doesn't sound so crazy. Sure, in the end assembly and Fortran/C architectures won out due to in fighting, delays, cost, speed and <i>consumer funded development</I> (my favorite flavor of R&D). But with the dawn of hardware like programmable logic arrays and their ancestors, the idea of hardware optimized to your personal preference of design language is not just possible, but inevitable. A convergence of optimization will occur "under the hood" while hackers and designers continue to create marvels that capture our attention. </p>
<p>Tyler (CHW* of <a href="http://victusmedia.com">Victus Media</a>) mentioned yesterday that he sticks with what works for his build utlities. It's unlikely he'll adopt a replacement unless it's superior on many counts. His description related to <a HREF="http://en.m.wikipedia.org/wiki/Turing_completeness?wasRedirected=true">Turing Complete</a> so various alternatives all yield analagous results, so why waste time switching? Now take the idea of Turing Complete and apply it to optimization. If a language is capable of performing any calculation, all executions share an optimal form specific to the data and architecture it is executed on. Our current interpreters, languages, and instructions aren't quite sharp enough to find that optimal run time, but I can imagine more potent translators converging on identical execution speed regardless of our language choice. Maybe I'm overestimating the intelligence of future compilers/interpreters, I humbly request that experts pipe in with your perspective and correct me.</p>
<h2>So What?</h2>
<p>In the long run it doesn't matter what form you choose to express your ideas and algorithms. Find an architecture that resonates with your most creative energy and go crazy with it.</p>
<p><I>Optimize for the quality of your creations</I></p>
<p>There's a sharp rocket scientist at my work that swears by Matlab. He has literally Gigabytes of libraries floating around the office. Even though Matlab is painfully slow for certain implementations now (don't do nested for loops, vectorize!), if it survives long enough as a language folks use and love, it could run as fast as any other solution. In the short term if you're like myself and like seeing results fast as an iterative design tool, c++ works pretty well, but it can be a heavy syntactical language.</p>
<p>Note* CHW = chief hacknical wizard </p>
