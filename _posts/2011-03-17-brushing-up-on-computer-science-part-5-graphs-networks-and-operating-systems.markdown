---
layout: post
status: publish
published: true
title: Brushing up on Computer Science Part 5, Graphs, Networks, and Operating Systems
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7844
wordpress_url: http://www.victusspiritus.com/?p=7844
date: '2011-03-17 15:57:22 -0400'
date_gmt: '2011-03-17 22:57:22 -0400'
categories:
- Uncategorized
tags:
- career counseling
- math
- coding
- computer science
comments:
- id: 9543
  author: Brushing Up on Computer Science Part 2, Object Oriented Programming (OOP)
    &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/15/brushing-up-on-computer-science-part-2-object-oriented-programming-oop/
  date: '2011-03-18 09:16:28 -0400'
  date_gmt: '2011-03-18 16:16:28 -0400'
  content: "[...] Graphs, Networks, and Operating Systems [...]"
- id: 9544
  author: Brushing Up on Computer Science Part 4, Algorithms &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-4-algorithms/
  date: '2011-03-18 09:16:46 -0400'
  date_gmt: '2011-03-18 16:16:46 -0400'
  content: "[...] Graphs, Networks, and Operating Systems [...]"
- id: 9545
  author: Brushing up on Computer Science Part 1, Big O &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/14/brushing-up-on-computer-science-part-1-big-o/
  date: '2011-03-18 11:10:18 -0400'
  date_gmt: '2011-03-18 18:10:18 -0400'
  content: "[...] Graphs, Networks, and Operating Systems [...]"
- id: 10061
  author: Lifelong Evolution of Concurrent Programming Patterns &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/05/29/lifelong-evolution-of-concurrent-programming-patterns/
  date: '2011-05-29 10:21:42 -0400'
  date_gmt: '2011-05-29 17:21:42 -0400'
  content: "[...] of concurrency that maintains shared memory space and initial state,
    but with individual stacks. Multithreading ameliorates the need to wait on bottlenecks
    from disk to memory for multi process programs. Program [...]"
- id: 11364
  author: Brushing Up on Computer Science Part 3, Data Structures &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/
  date: '2014-04-10 00:44:27 -0400'
  date_gmt: '2014-04-10 07:44:27 -0400'
  content: "[&#8230;] Graphs, Networks, and Operating Systems [&#8230;]"
---
<p><a href="http://brownsharpie.courtneygibbons.org/?p=21"><img src="{{ site.url }}/assets/2011/03/2006-10-18-regarding-henry.jpg" alt="" title="2006-10-18-regarding-henry" width="500" height="359" class="aligncenter size-full wp-image-7873" /></a></p>
<p>“Our graphs are based on starting with chaos — meaning we have a blast of news, and we say to our algorithms, find some order in this. We're creating these from scratch.”<br />
<a href="http://thinkexist.com/quotes/jim_andrus/">Jim Andrus</a></p>
<p>It is with some regret that I must bring to a close this white knuckled thrill ride and comp sci overview (mutually exclusive). All good things must come to an end, and weaving these posts together was certainly a good exercise for me. There is a bastion of material to choose from, limiting my ability to properly delve into all of the interesting bits. Despite this I'm satisfied with the compressed <em>random draw</em> that is the result of this review. Thanks for everyone who stopped in, commented or planted the seeds for this blog series. One last time, the <i>table of contents</i>:</p>
<ol>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/14/brushing-up-on-computer-science-part-1-big-o/">Intro and Big O</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/15/brushing-up-on-computer-science-part-2-object-oriented-programming-oop/">Object Oriented Programming</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/">Data Structures</a>: arrays, lists, trees, hash tables</li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-4-algorithms/">Algorithms</a> (searches, sorts, maths!)</li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/">Graphs, Networks, and Operating Systems</a></li>
</ol>
<p>Let's jump right in with a presentation which Chris Dixon and Matt Gattis of Hunch gave to an eager audience at Google in mid February. In the slideshow the importance of graphs is made clear through several hugely successful applications of graph theory on real world problems. The metaphor from clients and connections to nodes and vertices is the magic of our time.<br />
[scribd id=49061218 key=key-1u8ymkf45zipfepbxx09 mode=slideshow]</p>
<h2>Graph Algorithms</h2>
<p><a href="http://spikedmath.com/384.html"><img src="{{ site.url }}/assets/2011/03/384-the-petersen-giraffe.png" alt="" title="384-the-petersen-giraffe" width="300" height="590" class="aligncenter size-full wp-image-7875" /></a></p>
<p><b>Dijkstra's Algorithm</b><br />
One of the properties of shortest paths through directed graphs is that any shortest path is composed of shortest paths to all nodes along it's route (<a href="http://en.wikipedia.org/wiki/Optimal_substructure">optimal substructure</a>). If there was a shorter path to an intermediary node, you'd select that one instead for the current shortest path.</p>
<p>Dijkstra's algorithm is a search algorithm which finds the shortest path between an origin node and all other connected nodes (isolated nodes miss the party). Begin by setting all path lengths from the origin to all nodes to infinity, and mark them as unvisited. Set the current node to the origin. </p>
<p>Iteration:<br />
Identify the distance to all adjacent nodes, adding their path lengths to the length to get to this node. Store and update any improvements in current path lengths. Mark the current node as visited. Choose a shortest path to an adjacent node as the next node to process. If there are multiple nodes with equal length, selecting any will suffice.  </p>
<p>Each node will be visited only once and once a shortest path is calculated for all reachable nodes you're done.</p>
<p>[scribd id=50977483 key=key-naslhvzhgj81iotm6bd mode=slideshow]<br />
(<a href="http://www.cs.kuleuven.be/~jon/presentations/dijkstra_chr.pdf">source</a>)</p>
<p>It's hard to top the value of free university lectures when it comes to learning. This <a href="http://videolectures.net/mit6046jf05_demaine_lec17/">lecture</a> by <a href="http://videolectures.net/erik_demaine/">Erik Demaine</a> is well developed and easy to follow (thanks Erik and the unknown videographer). I've included Erik's slides below.<br />
[iframe http://videolectures.net/mit6046jf05_demaine_lec17/video/1/slides/ 550 400]<br />
Related implementation details for Dijkstra's algorithm:</p>
<blockquote><p>
The common implementation based on a min-priority queue implemented by a <a href="http://en.wikipedia.org/wiki/Fibonacci_heap">Fibonacci heap</a> and running in O(|E| + |V| log |V|) is due to (Fredman & Tarjan 1984). This is asymptotically the fastest known single-source shortest-path algorithm for arbitrary directed graphs with unbounded nonnegative weights<br />
(<a href="http://en.wikipedia.org/wiki/Dijkstra%27s_algorithm">source</a>)
</p></blockquote>
<p><b>A* algorithm</b><br />
An alternative search or shortest path approach is the <a href="http://en.wikipedia.org/wiki/A*_search_algorithm">A* Algorithm</a>. A* outperforms Dijkstra's algorithm by using heuristics.</p>
<blockquote><p>
As A* traverses the graph, it follows a path of the lowest known cost, keeping a sorted priority queue of alternate path segments along the way. If, at any point, a segment of the path being traversed has a higher cost than another encountered path segment, it abandons the higher-cost path segment and traverses the lower-cost path segment instead. This process continues until the goal is reached.<br />
(<a href="http://en.wikipedia.org/wiki/A*_search_algorithm#Concepts">source</a>)
</p></blockquote>
<p><a href="http://www.policyalmanac.org/games/aStarTutorial.htm">A* for beginners</a> is a good introduction to the algorithm.</p>
<p><a href="#concurrency" id="concurrency"<br />
<h2>Concurrency, Threads & Processes</h2>
<p></a><br />
"Once you start down the path of lock management the non-deterministic character of the system can quickly overwhelm your brain"<br />
<a href="http://compoundthinking.com/blog/index.php/2008/05/14/threads-processes-rails-trubogears-and-scalability/">Mark Ramm</a><br />
(I linked to Mr. Ramm's brief and effective introduction to threads and processes).</p>
<p>One of the simplest ways to scale an algorithm to many processes is horizontally. You batch concurrent and completely isolated runs and then tally their results with post processing. But there are times when running a single process with many threads will yield irresistible optimization returns. Recognizing when to walk the path of concurrent threads versus alternative options is a signal of expertise. I discussed an implementation of green threads in ruby over a couple of posts last year (<a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/12/31/ensure-all-roads-lead-to-your-goal-ruby-threads/">1</a>, <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/01/01/practical-first-rails-threading-example/">2</a>), and it saved us some time waiting on remote api calls. <i>It's worth noting that the Ruby MRI suffers from the same GIL that's mentioned in the slides on Python below.</i></p>
<p>It's beyond the scope of this post to go into great details about how operating systems handle the memory space (swapping, caching) and balance processor load (<a href="{{ site.url }}/assets/2011/03/umpa-lumpa.jpg">tiny red men</a>). What I'm interested in reviewing and learning more about is how multi/thread/process applications can best be designed to take advantage of increasingly concurrent hardware to solve computationally expensive problems. First let's begin by covering definitions, and then wrap up this series with a couple slideshows which <del datetime="2011-03-18T16:10:29+00:00">show all my baby pictures</del> discuss concurrent processing.</p>
<p><b>Defintiions</b></p>
<p><i>What's a process?</i><br />
Processes describe active applications. A process encapsulates the execution code and memory for a given program, and may share state information with other processes through communication channels (sockets).</p>
<p><i>What's a thread?</i><br />
An executable series of code, but that are contained in processes and often share memory and other resources between each other. Threads share a processes instructions and variable states.</p>
<blockquote><p>
In order for data to be correctly manipulated, threads will often need to rendezvous in time in order to process the data in the correct order. Threads may also require mutually-exclusive operations (often implemented using <a href="http://en.wikipedia.org/wiki/Semaphore_(programming)">semaphores</a>) in order to prevent common data from being simultaneously modified, or read while in the process of being modified. Careless use of such primitives can lead to <a href="http://en.wikipedia.org/wiki/Deadlock">deadlocks</a>.<br />
(<a href="http://en.wikipedia.org/wiki/Thread_(computer_science)#Multithreading:_Advantages.2FUses">source</a>)
</p></blockquote>
<p><em>Deadlocks</em><br />
Deadlocks occur when multiple competing actions wait for each other to finish. The gruesome cousin of gridlock.<br />
(<a href="http://en.wikipedia.org/wiki/Deadlock">source</a>)</p>
<p><em>Race conditions</em></p>
<blockquote><p>
Race conditions arise in software when separate processes or threads of execution depend on some shared state. Operations upon shared states are critical sections that must be mutually exclusive in order to avoid harmful collision between processes or threads that share those states.<br />
(<a href="http://en.wikipedia.org/wiki/Race_conditions#Computing">source</a>)
</p></blockquote>
<p><em>Semaphores</em><br />
A semaphore is an abstract data type that brokers access to shared resources. Simple binary semaphores are either locked or unlocked. Counting semaphores keep a tally of available resources and buffer currently unavailable resource access in a queue. Really good managers act as semaphores for their teams, buffering upper management demands :).<br />
(<a href="http://en.wikipedia.org/wiki/Semaphore_(programming)">source</a>)<br />
An analogous structure to counting semaphores are <a href="http://www.boost.org/doc/libs/1_38_0/libs/smart_ptr/smart_ptr.htm">shared pointers</a>. Although they aren't directly responsible for threading, shared pointers keep a tally of active copies, and are able to free the memory of an object when it's last copy goes out of scope.</p>
<p><em>Mutex or Mutually exclusive operations</em></p>
<blockquote><p>
A mutually exclusive (or mutex) lock acts as a protective barrier around a resource. A mutex is a type of semaphore that grants access to only one thread at a time. If a mutex is in use and another thread tries to acquire it, that thread blocks until the mutex is released by its original holder. If multiple threads compete for the same mutex, only one at a time is allowed access to it.<br />
(<a href="http://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/Multithreading/ThreadSafety/ThreadSafety.html">source</a>)
</p></blockquote>
<p><em>Atomic Operations</em></p>
<blockquote><p>
Atomic operations are a simple form of synchronization that work on simple data types. The advantage of atomic operations is that they do not block competing threads. For simple operations, such as incrementing a counter variable, this can lead to much better performance than taking a lock.<br />
(<a href="http://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/Multithreading/ThreadSafety/ThreadSafety.html">source</a>)
</p></blockquote>
<p>Additional references on locks, mutexes, semaphores and monitors:</p>
<ul>
<li><a href="http://www.darkside.co.za/archive/2008/08/08/lock-monitor-mutex-and-semaphores.aspx">Lock monitor mutex and semaphores</a></li>
<li><a href="cseweb.ucsd.edu/classes/fa06/cse120/lectures/120-fa06-l6.pdf">Semaphores and Monitors</a></li>
</ul>
<p><b>Although the following set of slides is Python specific, it reviews many of the core features of multiprocessing and multithreading. </b></p>
<div style="width:425px" id="__ss_855881"> <strong style="display:block;margin:12px 0 4px"><a href="http://www.slideshare.net/pvergain/multiprocessing-with-python-presentation" title="Multiprocessing with python">Multiprocessing with python</a></strong> <object id="__sse855881" width="425" height="355"><param name="movie" value="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=pyworks-1229584486232623-1&stripped_title=multiprocessing-with-python-presentation&userName=pvergain" /><param name="allowFullScreen" value="true"/><param name="allowScriptAccess" value="always"/><embed name="__sse855881" src="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=pyworks-1229584486232623-1&stripped_title=multiprocessing-with-python-presentation&userName=pvergain" type="application/x-shockwave-flash" allowscriptaccess="always" allowfullscreen="true" width="425" height="355"></embed></object>
<div style="padding:5px 0 12px"> View more <a href="http://www.slideshare.net/">presentations</a> from <a href="http://www.slideshare.net/pvergain">Patrick Vergain</a> </div>
</p></div>
<p><b>I'll leave off with a set of slides which goes into further detail about multithreading and the global interpreter lock in Python</b></p>
<div style="width:425px" id="__ss_466970"> <strong style="display:block;margin:12px 0 4px"><a href="http://www.slideshare.net/XEmacs/beating-the-sh-out-of-the-gil-multithreading-vs-multiprocessing" title="Beating the (sh** out of the) GIL - Multithreading vs. Multiprocessing">Beating the (sh** out of the) GIL - Multithreading vs. Multiprocessing</a></strong> <object id="__sse466970" width="425" height="355"><param name="movie" value="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=pyparallelscripting-1213408663113146-8&stripped_title=beating-the-sh-out-of-the-gil-multithreading-vs-multiprocessing&userName=XEmacs" /><param name="allowFullScreen" value="true"/><param name="allowScriptAccess" value="always"/><embed name="__sse466970" src="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=pyparallelscripting-1213408663113146-8&stripped_title=beating-the-sh-out-of-the-gil-multithreading-vs-multiprocessing&userName=XEmacs" type="application/x-shockwave-flash" allowscriptaccess="always" allowfullscreen="true" width="425" height="355"></embed></object>
<div style="padding:5px 0 12px"> View more <a href="http://www.slideshare.net/">presentations</a> from <a href="http://www.slideshare.net/XEmacs">XEmacs Slartibartfast</a> </div>
</p></div>
<p>Uh oh, I forgot Networks. Maybe nobody will notice.</p>
