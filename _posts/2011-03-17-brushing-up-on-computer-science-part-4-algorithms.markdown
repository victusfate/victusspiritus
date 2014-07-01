---
layout: post
status: publish
published: true
title: Brushing Up on Computer Science Part 4, Algorithms
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7779
wordpress_url: http://www.victusspiritus.com/?p=7779
date: '2011-03-17 06:33:23 -0400'
date_gmt: '2011-03-17 13:33:23 -0400'
categories:
- Uncategorized
tags:
- career counseling
- math
- coding
- computer science
comments:
- id: 9562
  author: Brushing Up on Computer Science Part 3, Data Structures &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/
  date: '2011-03-19 15:48:36 -0400'
  date_gmt: '2011-03-19 22:48:36 -0400'
  content: "[...] Algorithms (searches, sorts, maths!) [...]"
- id: 10059
  author: Brushing up on Computer Science Part 5, Graphs, Networks, and Operating
    Systems &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/
  date: '2011-05-29 09:18:42 -0400'
  date_gmt: '2011-05-29 16:18:42 -0400'
  content: "[...] Algorithms (searches, sorts, maths!) [...]"
---
<p>"An algorithm must be seen to be believed."<br />
<a href="http://www-cs-faculty.stanford.edu/~uno/">Donald Knuth</a></p>
<p><em>How we ended up here</em><br />
It all began a few days ago with an email from a friend (thanks Denny). I was inspired to dust off my software engineering cap, and review a few choice topics in computer science. What better way to study than to write up a blog post sampling the materials of interest. I accept that in the limited span of blog posts I won't do proper justice to any topic of sufficient depth, that's what books are for. Each post in the series begins with an anchor quote and takes off through the fundamentals of software design theory and practical implementation details with an emphasis on the latter. Much of my sophomoric understanding of computer science comes from iterative practice, reading, and communicating with folks much smarter than myself.</p>
<p>The <i>table of contents</i> for this blog series:</p>
<ol>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/14/brushing-up-on-computer-science-part-1-big-o/">Intro and Big O</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/15/brushing-up-on-computer-science-part-2-object-oriented-programming-oop/">Object Oriented Programming</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/">Data Structures</a>: arrays, lists, trees, hash tables</li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-4-algorithms/">Algorithms</a> (searches, sorts, maths!)</li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/">Graphs, Networks, and Operating Systems</a></li>
</ol>
<h2>Algorithms</h2>
<p><a href="http://www.webopedia.com/TERM/A/algorithm.html"><img src="{{ site.url }}/assets/2011/03/ALGOR.gif" alt="" title="ALGOR" width="413" height="284" class="aligncenter size-full wp-image-7784" /></a><br />
In short, an algorithm is a recipe.</p>
<blockquote><p>
A formula or set of steps for solving a particular problem. To be an algorithm, a set of rules must be unambiguous and have a clear stopping point. Algorithms can be expressed in any language, from natural languages like English or French to programming languages like FORTRAN<br />
(<a href="http://www.webopedia.com/TERM/A/algorithm.html">source</a>)</p>
<p>In mathematics and computer science, an algorithm (pronounced /ˈælɡəɹɪðm/ ( listen)) is an effective method expressed as a finite list[1] of well-defined instructions[2] for calculating a function[3]. Algorithms are used for calculation, data processing, and automated reasoning.<br />
(<a href="http://en.wikipedia.org/wiki/Algorithms">source</a>)
</p></blockquote>
<p><b>Understanding Strategies beats Memorizing Tactics</b></p>
<p>Algorithms are well specified techniques for performing an unbounded variety of tasks (good luck learning all algorithms). They are the tactics employed by computer scientists day in and day out, many times without even conscious awareness until further optimization is needed. When working on application specific problems at a high level, it's a distraction to constantly dive into deep operating system and compiler details. </p>
<p>There are broad patterns common to vastly separated problem spaces. These strategies serve as motivations for both design and implementation of algorithms.  Divide and conquer and greedy techniques are deployed time and time again within algorithms. </p>
<p>A couple of the most famous divide and conquer techniques are the <a href="http://en.wikipedia.org/wiki/Fast_Fourier_transform">FFT</a> and <a href="http://labs.google.com/papers/mapreduce-osdi04.pdf">MapReduce</a> (<a href="http://labs.google.com/papers/mapreduce-osdi04-slides/index.html">slides</a>, <a href="http://cacm.acm.org/magazines/2010/1/55744-mapreduce-a-flexible-data-processing-tool/fulltext">web article</a>). The FFT iteratively breaks down the Discrete Fourier Transform into a series of odd and even components until it get's down to a single multiply and add. </p>
<p>I first came across map reduce while reading a set of slides by Jeff Dean, <a href="iepg.org/iepg/2009-11-ietf76/dean-keynote-ladis2009.pdf">Designs, Lessons and Advice from Building Large Distributed Systems</a>.<br />
<a href="http://iepg.org/iepg/2009-11-ietf76/dean-keynote-ladis2009.pdf"><img src="{{ site.url }}/assets/2011/03/MapReduce_DeanKeynoteLadis.png" alt="" title="MapReduce_DeanKeynoteLadis" width="446" height="315" class="aligncenter size-full wp-image-7813" /></a><br />
I didn't give it much thought at the time, as it appeared to be a good framework for implementing a divide and conquer strategy. A few months later I hit upon MR again while reading through CouchDB's architecture for retrieving documents. It's no surprise sharp folks utilize similar strategies for very different types of problems.</p>
<p>Greedy algorithms make locally optimally decisions, often keeping several potential solutions, and generate a final decision when a forcing function requires an estimate in finite time. One example of a greedy algorithm is an implementation of the Multiple Hypothesis Tracker or MHT. The MHT associates combinations of measurements (factorial growth), calculates likelihood scores, and retains a set number of associations per iteration. At each phase there is always a set of best tracks that it can report out, yet there is a possibility that the global best solution will be pruned during an iteration (heuristics make no guarantees). For understanding the nuances of greedy strategies I defer to the expert, Boss Hog.<br />
<a href="{{ site.url }}/assets/2011/03/boss_hog_eating_wings.jpeg"><img src="{{ site.url }}/assets/2011/03/boss_hog_eating_wings.jpeg" alt="" title="boss_hog_eating_wings" width="255" height="191" class="aligncenter size-full wp-image-7816" /></a></p>
<h2>Sorting Algorithms</h2>
<p>I blame the cruel mistress entropy for the heroic efforts needed to repeatedly sort unorganized data, such is nature. The methods to sort data are as varied as there are ways to visualize it, each algorithm and its implementation is crafted with an artistic touch. If you're looking for a sort to fit your problem's constraints, an excellent starting point is the <a href="http://en.wikipedia.org/wiki/Sorting_algorithm">Wikipedia page</a> which I quote shamelessly below. The gifs from Wikipedia display an animation of each algorithm in action. The gifs cycle through visualizations after a brief pause.<br />
<a href="{{ site.url }}/assets/2011/03/sorting_shootout.png"><img src="{{ site.url }}/assets/2011/03/sorting_shootout.png" alt="" title="sorting_shootout" width="440" height="410" class="aligncenter size-full wp-image-7795" /></a></p>
<p><em>Quicksort</em><br />
<a href="http://en.wikipedia.org/wiki/Algorithms#Examples"><img src="{{ site.url }}/assets/2011/03/220px-Sorting_quicksort_anim.gif" alt="" title="220px-Sorting_quicksort_anim" width="220" height="168" class="aligncenter size-full wp-image-7791" /></a></p>
<blockquote><p>
Quicksort sorts by employing a divide and conquer strategy to divide a list into two sub-lists.<br />
The steps are:</p>
<p>1)Pick an element, called a pivot, from the list.</p>
<p>2) Reorder the list so that all elements with values less than the pivot come before the pivot, while all elements with values greater than the pivot come after it (equal values can go either way). After this partitioning, the pivot is in its final position. This is called the partition operation. Recursively sort the sub-list of lesser elements and the sub-list of greater elements. The base case of the recursion are lists of size zero or one, which never need to be sorted.</p>
<p>Simple version</p>
<pre>
In simple pseudocode, the algorithm might be expressed as this:
 function quicksort(array)
     var list less, greater
     if length(array) ≤ 1
         return array  // an array of zero or one elements is already sorted
     select and remove a pivot value pivot from array
     for each x in array
         if x ≤ pivot then append x to less
         else append x to greater
     return concatenate(quicksort(less), pivot, quicksort(greater))
</pre>
</blockquote>
<p>The quicksort on average requires O(n log n) comparisons and worse case O(n^2).</p>
<p><em>Merge sort</em><br />
<a href="{{ site.url }}/assets/2011/03/Merge_sort_animation2.gif"><img src="{{ site.url }}/assets/2011/03/Merge_sort_animation2.gif" alt="" title="Merge_sort_animation2" width="280" height="237" class="aligncenter size-full wp-image-7801" /></a><br />
The <a href="http://en.wikipedia.org/wiki/Merge_sort">merge sort</a> implements a divide and conquer strategy. If the size of a sublist is 0 or 1 it's sorted. The merge sort breaks up a list into two sublists of equivalent size. Each sublist is then merged.</p>
<p>The following is a pseudo code example of the algorithm's implementation (<a href="http://en.wikipedia.org/wiki/Merge_sort#Algorithm">source</a>)</p>
<pre>
function merge_sort(m)
    if length(m) ≤ 1
        return m
    var list left, right, result
    var integer middle = length(m) / 2
    for each x in m up to middle
         add x to left
    for each x in m after middle
         add x to right
    left = merge_sort(left)
    right = merge_sort(right)
    result = merge(left, right)
    return result

function merge(left,right)
    var list result
    while length(left) > 0 or length(right) > 0
        if length(left) > 0 and length(right) > 0
            if first(left) ≤ first(right)
                append first(left) to result
                left = rest(left)
            else
                append first(right) to result
                right = rest(right)
        else if length(left) > 0
            append first(left) to result
            left = rest(left)
        else if length(right) > 0
            append first(right) to result
            right = rest(right)
    end while
    return result
</pre>
<p>The merge sort has an average and worst case performance of O(nlogn).</p>
<p><em>Bubble sort</em><br />
<a href="{{ site.url }}/assets/2011/03/Bubble_sort_animation.gif"><img src="{{ site.url }}/assets/2011/03/Bubble_sort_animation.gif" alt="" title="Bubble_sort_animation" width="280" height="237" class="aligncenter size-full wp-image-7804" /></a>(<a href="http://en.wikipedia.org/wiki/Bubble_sort#In_practice">source</a>)<br />
The bubble sort iterates through a collection swapping adjacent elements into a specified order. The process repeats itself until no further elements are swapped. The algorithms average and worst case performance is O(n^2)</p>
<p><em>Heapsort</em><br />
<a href="{{ site.url }}/assets/2011/03/Sorting_heapsort_anim.gif"><img src="{{ site.url }}/assets/2011/03/Sorting_heapsort_anim.gif" alt="" title="Sorting_heapsort_anim" width="280" height="214" class="aligncenter size-full wp-image-7798" /></a><br />
The <a href="http://en.wikipedia.org/wiki/Heapsort">heapsort</a> finds an extreme element (largest or smallest) and places it at one end of the list, continuing until the entire list is sorted. The <a href="http://en.wikipedia.org/wiki/Heap_(data_structure)">heap</a> is a binary tree where the root node is larger than any of it's children, key(A) >= key(B). The heap is also a maximally efficient implementation called a priority queue. The average and worst case performance is O(nlogn).</p>
<blockquote><p>
Heapsort begins by building a heap out of the data set, and then removing the largest item and placing it at the end of the partially sorted array. After removing the largest item, it reconstructs the heap, removes the largest remaining item, and places it in the next open position from the end of the partially sorted array. This is repeated until there are no items left in the heap and the sorted array is full. Elementary implementations require two arrays - one to hold the heap and the other to hold the sorted elements.<br />
(<a href="http://en.wikipedia.org/wiki/Heapsort#Overview">source</a>)
</p></blockquote>
<p>It's worth mentioning another heap, the <a href="http://en.wikipedia.org/wiki/Fibonacci_heap">Fibonacci Heap</a>, which I'll come back to in the tomorrow's post on graphs (Dijkstra's search algorithm).</p>
<h2>Packing Problems</h2>
<p><a href="http://www.astrokettle.com/"><img src="{{ site.url }}/assets/2011/03/box_packing.gif" alt="" title="box_packing" width="490" height="480" class="aligncenter size-full wp-image-7788" /></a><br />
(<a href="http://en.wikipedia.org/wiki/Quicksort#Algorithm">source</a>)<br />
The image says it all about packing problems. Your goal is to fit as many N-dimensional structures as possible into the smallest region possible, and the maximum density algorithm wins. If you're really into this type of problem, <a href="http://www.dropbox.com/jobs">Dropbox</a> is hiring.</p>
<blockquote><p>
Packing problems are a class of optimization problems in recreational mathematics which involve attempting to pack objects together (often inside a container), as densely as possible. Many of these problems can be related to real life storage and transportation issues. Each packing problem has a dual covering problem, which asks how many of the same objects are required to completely cover every region of the container, where objects are allowed to overlap.<br />
In a packing problem, you are given:<br />
'containers' (usually a single two- or three-dimensional convex region, or an infinite space)<br />
'goods' (usually a single type of shape), some or all of which must be packed into this container<br />
Usually the packing must be without overlaps between goods and other goods or the container walls. The aim is to find the configuration with the maximal density. In some variants the overlapping (of goods with each other and/or with the boundary of the container) is allowed but should be minimised.<br />
(<a href="http://en.wikipedia.org/wiki/Packing_problem">source</a>)
</p></blockquote>
<h2>Cryptographic Hash Functions</h2>
<p><del datetime="2011-03-18T17:41:51+00:00">Cryptography and Encryption Algorithms</del> (thanks to <a href="http://www.reddit.com/user/your_perception">your_perception</a> for the correction)</p>
<div style="width:425px" id="__ss_708641"> <strong style="display:block;margin:12px 0 4px"><a href="http://www.slideshare.net/prasenjeetd/cryptography-a-brief-history-presentation" title="Cryptography - A Brief History">Cryptography - A Brief History</a></strong> <object id="__sse708641" width="425" height="355"><param name="movie" value="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=cryptography-a-brief-history-1225451014313292-8&stripped_title=cryptography-a-brief-history-presentation&userName=prasenjeetd" /><param name="allowFullScreen" value="true"/><param name="allowScriptAccess" value="always"/><embed name="__sse708641" src="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=cryptography-a-brief-history-1225451014313292-8&stripped_title=cryptography-a-brief-history-presentation&userName=prasenjeetd" type="application/x-shockwave-flash" allowscriptaccess="always" allowfullscreen="true" width="425" height="355"></embed></object>
<div style="padding:5px 0 12px"> View more <a href="http://www.slideshare.net/">presentations</a> from <a href="http://www.slideshare.net/prasenjeetd">prasenjeetd</a> </div>
</p></div>
<p><a href="http://en.wikipedia.org/wiki/MD5#Algorithm">MD5</a> was considered a popular and fairly secure cryptographic hash function in the late 1990s, but is now known to have several predictable vulnerabilities. It converts a variable length input string into a 128bit output. <a href="http://en.wikipedia.org/wiki/SHA-1#Examples_and_pseudocode">SHA-1</a> is a more recent standard for secure cryptography but is susceptible to other known vulnerabilities (is nothing sacred). </p>
<div style="width:425px" id="__ss_5036453"> <strong style="display:block;margin:12px 0 4px"><a href="http://www.slideshare.net/null0x00/n-ull-presentationcrackingsaltedhashes" title="Salt Cryptography & Cracking Salted Hashes by fb1h2s">Salt Cryptography & Cracking Salted Hashes by fb1h2s</a></strong> <object id="__sse5036453" width="425" height="355"><param name="movie" value="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=nullpresentationcrackingsaltedhashes-100823023438-phpapp02&stripped_title=n-ull-presentationcrackingsaltedhashes&userName=null0x00" /><param name="allowFullScreen" value="true"/><param name="allowScriptAccess" value="always"/><embed name="__sse5036453" src="http://static.slidesharecdn.com/swf/ssplayer2.swf?doc=nullpresentationcrackingsaltedhashes-100823023438-phpapp02&stripped_title=n-ull-presentationcrackingsaltedhashes&userName=null0x00" type="application/x-shockwave-flash" allowscriptaccess="always" allowfullscreen="true" width="425" height="355"></embed></object>
<div style="padding:5px 0 12px"> View more <a href="http://www.slideshare.net/">presentations</a> from <a href="http://www.slideshare.net/null0x00">n|u - The Open Security Community</a> </div>
</p></div>
<h2>Additional Notes:</h2>
<p>There are a few other areas I'd like to include, but I'll have to return and append them to the post at another time (hopefully this weekend time allowing). For now I'll leave these as placeholders as a reminder to myself.</p>
<p><em>Linear and Dynamic Programming</em><br />
<a href="http://en.wikipedia.org/wiki/Linear_programming">Linear Programming</a><br />
<a href="http://en.wikipedia.org/wiki/Dynamic_programming">Dynamic Programming</a> (so named partly because Dynamic sounded cool)</p>
<p><em>Artificial Intelligence and Machine Learning</em><br />
(<a href="http://en.wikipedia.org/wiki/Artificial_neural_network">source</a>)<br />
Supervised and Unsupervised learning...<br />
Estimation algorithms: Detection, Tracking, Prediction, ie what I do for a living Discrimination: Classification (Quadratic, PNN) Natural language processing (NLP): machine learning applied to big data sets <em>There's no shame in brute force</em> When there's no time for more elegant algorithms, there's little shame in <a href="http://en.wikipedia.org/wiki/Brute_force_search">brute forcing</a> your way to a delivery.</p>
