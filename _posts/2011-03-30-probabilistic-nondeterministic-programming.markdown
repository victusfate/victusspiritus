---
layout: post
status: publish
published: true
title: Probabilistic Nondeterministic Programming
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8151
wordpress_url: http://www.victusspiritus.com/?p=8151
date: '2011-03-30 06:43:01 -0400'
date_gmt: '2011-03-30 13:43:01 -0400'
categories:
- Uncategorized
tags:
- math
- coding
- probe
- design
comments: []
---
<p>This morning I came across an inviting link on Hacker News, <a href="http://www.ccs.neu.edu/home/dorai/t-y-scheme/t-y-scheme-Z-H-16.html#node_chap_14">Nondeterminism</a>, part of the <a href="http://www.ccs.neu.edu/home/dorai/t-y-scheme/t-y-scheme-Z-H-1.html#node_toc_start">Teach Yourself Scheme in Fixnum Days</a>. There are a number of chapters which help new comers to Scheme dig in and get a feel for the language. This chapter discusses McCarthy's <span style="color: #990000;">amb</span> operator, describes a rules based implementation, and offers several example applications.</p>
<blockquote><p>
<span style="color: #990000;">amb</span> takes zero or more expressions, and makes a nondeterministic (or "ambiguous'') choice among them, preferring those choices that cause the program to converge meaningfully.
</p></blockquote>
<p>What drew me to this topic is that a lack of predictability can be an advantage to solving certain types of problems. There are plenty of options for deterministic programming, but not nearly as many which implement fuzzy or unpredictable decision logic. What will a program do with a slightly malformed packet, or a combination of headers that appear to be JSON mixed with a markup language and include binary attachments? If a specific interface isn't detailed, we hope that it gracefully fails with an appropriate error message. </p>
<p>While browsing the post I was reminded of a fictional programming language I touched on briefly last year (<a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/05/26/probe-a-fictional-programming-language-design/">Probe</a>), and one of the goals for the language is an implicit interface selection system. A source of great complication with programming is delineating rules to cover all probable data and performance environments, ie handling the edge cases. Exhaustively going through an infinite library of perfectly matching formats is impractical to say the least. What would be helpful is an automated lookup system for machine readable specifications, a series of educated guesses based on pattern matching, and memory that persists between executions.</p>
<p>Can we better characterize data patterns so that a fast guessing engine could identify novel combinations of formats by recognizing tell tale signatures?</p>
<p>A follow up post to Probe:</p>
<ul>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/05/28/transient-technology-how-probe-may-handle-interface-mapping/">how probe may handle interface mapping</a></li>
</ul>
<p>Wonderful references for me to pour over later:</p>
<ul>
<li><a href="http://www.lfcs.inf.ed.ac.uk/reports/90/ECS-LFCS-90-105/">Probability and Non Determinism thesis</a></li>
<li><a href="http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.5855&rep=rep1&type=pdf">Comparative semantics for a process language with probabilistic choice and non-determinism</a></li>
<li><a href="http://en.wikipedia.org/wiki/Stochastic">Stochastic processes</a></li>
<li><a href="http://en.wikipedia.org/wiki/Probabilistic_automaton">probabilistic automaton</a></li>
<li><a href="http://en.wikipedia.org/wiki/Nondeterministic_finite-state_machine">nondeterministic finite-state machine</a></li>
</ul>
