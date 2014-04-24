---
layout: post
status: publish
published: true
title: Lifelong Evolution of Concurrent Programming Patterns
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9096
wordpress_url: http://www.victusspiritus.com/?p=9096
date: '2011-05-29 09:19:22 -0400'
date_gmt: '2011-05-29 16:19:22 -0400'
categories:
- Uncategorized
tags:
- coding
- computer science
comments: []
---
<h3>Serial Processing</h3>
<p>The type of development I grew up learning in the 80's was serial. Data entered into a program through files or standard input. Functions then transformed data through a series of discrete intermediate steps, generating outputs as they ran, or directly funneling generated data into other functions. Final outputs were stored in human readable files, formats for other programs, or a combination of both. </p>
<p>The advantages of this pattern include simplicity of state, ease of tracking down bugs, and the ability to reroute functional flow at any stage of processing. Unfortunately serial programming is limited by bottlenecking I/O, and fails to utilize multicore or large network resources.</p>
<h3>Multi Process</h3>
<p>When I began working as an engineer in the mid 90's I suddenly had access to more computational power. An easy way to scale programs is to run the code across several processors. This is commonly referred to as horizontal scaling, and is a straightforward way to scale serial programs. </p>
<p>Care must be taken to duplicate intermediate data to separate systems over networks. Local multiprocess implementation is limited by bus bandwidth to and from disks to memory, memory to and from processors, as well as computational complexity.</p>
<h3>Multi Threaded</h3>
<p>In the last decade I was introduced to a form of concurrency that maintains shared memory space and initial state, but with individual stacks. <a href="http://www.victusspiritus.com/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/#concurrency">Multithreading</a> ameliorates the need to wait on bottlenecks from disk to memory for multi process programs. Program state is managed for multiple threads by a series of semaphores which broker conditional access to limited resources, the simplest being a Mutex or lock. Atomic operations are a simple form of synchronization and safe to be called by threads at any time.</p>
<h3>Asynchronous</h3>
<p>Web programming and large network development delivers access to dedicated systems. Each call yields advanced processing by leveraging remote resources. With a growing reliance on networks of systems, asynchronous callbacks or non-blocking I/O enables processors to avoid waiting and continually reacts, much like graphical user interfaces. The <a href="http://en.wikipedia.org/wiki/Reactor_pattern">reactor pattern</a> is an extremely popular implementation of asynchronous processing for web design. Events can be processed without requiring event handlers to block program flow.</p>
<p>The above concurrent patterns may be combined, bringing serial, multi threaded, multi process and asynchronous modules together into a single application. Each concurrent pattern resolves a class of execution needs. Practical experience serves as the basis for selecting the proper pattern to meet a given processing requirement.</p>
