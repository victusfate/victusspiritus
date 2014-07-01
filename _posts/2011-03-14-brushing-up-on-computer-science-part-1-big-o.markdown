---
layout: post
status: publish
published: true
title: Brushing up on Computer Science Part 1, Big O
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7656
wordpress_url: http://www.victusspiritus.com/?p=7656
date: '2011-03-14 06:24:13 -0400'
date_gmt: '2011-03-14 13:24:13 -0400'
categories:
- Uncategorized
tags:
- career counseling
- math
- coding
- computer science
comments:
- id: 9252
  author: Big O Theory | alebaffa&#039;s
  author_email: ''
  author_url: http://www.alessandrobaffa.it/2011/03/14/big-o-theory/
  date: '2011-03-14 07:37:35 -0400'
  date_gmt: '2011-03-14 14:37:35 -0400'
  content: "[...] Graphs, Operating Systems, Network Communication and other Important
    topic(s) I’m not thinking of right now   via victusspiritus.com [...]"
- id: 9262
  author: Renee
  author_email: reneejustrenee@gmail.com
  author_url: http://noupside.tumblr.com
  date: '2011-03-14 16:44:00 -0400'
  date_gmt: '2011-03-14 16:44:00 -0400'
  content: This is a really useful review...I still have all of my old data structures
    and algorithms textbooks and keep telling myself that one of these days I'll get
    to reviewing them. :) I'm looking forward to reading the rest of the series. Thanks.
- id: 9265
  author: DGentry
  author_email: denny+disqus@geekhold.com
  author_url: http://codingrelic.geekhold.com
  date: '2011-03-14 16:57:00 -0400'
  date_gmt: '2011-03-14 16:57:00 -0400'
  content: Wikipedia's computer science section is quite well done.
- id: 9266
  author: Paul
  author_email: ''
  author_url: http://pulse.yahoo.com/_MIN3JGDXNN7G2TP7UG3XTSNS5I
  date: '2011-03-14 17:09:00 -0400'
  date_gmt: '2011-03-14 17:09:00 -0400'
  content: I think it is easier to understand if you just see it as growth. It is
    how much more time (in the worst case) will be needed for the algorithm if you
    feed in larger inputs. If you double the size of the input, does that double the
    amount of time, square it, or send it into the atmosphere. Or in other words,
    if you tested the code on a very small subset of the data, when it goes into product
    will you be saying "Ohhhhhhhhh" (and thus having a big-Oh day :-)
- id: 9357
  author: Brushing Up on Computer Science Part 2, Object Oriented Programming (OOP)
    &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/15/brushing-up-on-computer-science-part-2-object-oriented-programming-oop/
  date: '2011-03-15 05:34:52 -0400'
  date_gmt: '2011-03-15 12:34:52 -0400'
  content: "[...] Intro and Big O [...]"
- id: 9443
  author: Brushing Up on Computer Science Part 3, Data Structures &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/
  date: '2011-03-16 05:02:13 -0400'
  date_gmt: '2011-03-16 12:02:13 -0400'
  content: "[...] Intro and Big O [...]"
- id: 9457
  author: Jon
  author_email: qweasdf@bobmail.info
  author_url: ''
  date: '2011-03-16 16:35:00 -0400'
  date_gmt: '2011-03-16 16:35:00 -0400'
  content: |-
    "As de Bruijn says, O(x) = O(x2) is true but O(x2) = O(x) is not"

    You're missing a ^ symbol here; O(2*x) = O(x) is true; O(x^2) = O(x) is not.
- id: 9462
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-03-16 18:23:00 -0400'
  date_gmt: '2011-03-16 18:23:00 -0400'
  content: yes indeed, missing a hat, thanks Jon
- id: 9514
  author: Brushing Up on Computer Science Part 4, Algorithms &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-4-algorithms/
  date: '2011-03-17 06:33:52 -0400'
  date_gmt: '2011-03-17 13:33:52 -0400'
  content: "[...] Intro and Big O [...]"
- id: 9539
  author: Brushing up on Computer Science Part 5, Graphs, Networks, and Operating
    Systems &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/
  date: '2011-03-18 09:14:42 -0400'
  date_gmt: '2011-03-18 16:14:42 -0400'
  content: "[...] Intro and Big O [...]"
- id: 9743
  author: The cold case | Nerdson não vai à escola
  author_email: ''
  author_url: http://nerdson.com/blog/cold-case/
  date: '2011-04-02 16:14:57 -0400'
  date_gmt: '2011-04-02 23:14:57 -0400'
  content: "[...] http://victusfate.github.io/victusspiritus/uncategorized/2011/03/14/brushing-up-on-computer-science-part-1-big-o/
    [...]"
---
<p>"Those who cannot remember the past are condemned to repeat it"<br />
<a href="http://en.wikiquote.org/wiki/George_Santayana">George Santayana</a></p>
<h2>Intro</h2>
<p>Memory is such a fragile construct, yet we are forced to cruelly mold it into submission through extreme repetition and clever tricks of association. And even then, detailed memories fade exponentially in time and are of little use without regular access and utilization.</p>
<p>Early this morning I was <em>inspired</em> to review the basics of computer science, including object oriented programming, data structures, common algorithms and characterization of complexity (Big O) by blogging friend <a href="http://codingrelic.geekhold.com/">Denton Gentry</a>. I leave the source of my inspiration as an exercise in deductive reasoning. </p>
<p>These posts will serve as a study guide for myself, and anyone else who chooses to read or contribute to them. I'll add to each post as I gather more relevant material and a fresher understanding of the types of issues and real world problems that demand readily accessible knowledge. Here are the 5-ish posts I'm planning on writing up:</p>
<ol>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/14/brushing-up-on-computer-science-part-1-big-o/">Intro and Big O</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/15/brushing-up-on-computer-science-part-2-object-oriented-programming-oop/">Object Oriented Programming</a></li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/">Data Structures</a>: arrays, lists, trees, hash tables</li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-4-algorithms/">Algorithms</a> (searches, sorts, maths!)</li>
<li><a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/">Graphs, Networks, and Operating Systems</a></li>
</ol>
<h2>Big O</h2>
<p>Let's begin with a review of Big O or Big Omicron. While you can count on Wikipedia to deliver a well written description of <a href="http://en.wikipedia.org/wiki/Big_O_notation">Big O notation</a>, I found William Shields <a href="http://www.cforcoding.com/2009/07/plain-english-explanation-of-big-o.html">Plain English Explanation of Big O Notation</a> to be a concise and welcome companion for brushing off the cobwebs (thanks William). William shares a down to Earth description of Big O:</p>
<blockquote><p>
Big O notation seeks to describe the relative complexity of an algorithm by reducing the growth rate to the key factors when the key factor tends towards infinity. For this reason, you will often hear the phrase asymptotic complexity. In doing so, all other factors are ignored. It is a  relative representation of complexity.
</p></blockquote>
<p>Before we get into the details, I think it's helpful to get a frame of reference for the Orders of Complexity for several different algorithms, some of which you may be intimately familiar with. Over the years I've come across specific examples of Big O notation for various algorithms and here I list a brief sample (see the references, in particular <a href="http://en.wikipedia.org/wiki/Exponential_time">Time Complexity</a> for more complete lists):</p>
<ul>
<li>lookup at a memory location, simple comparison are constant O(1)</li>
<li>searching an unordered list, basic operations on n members O(n)</li>
<li>binary search of sorted numerical data or a balanced tree, O(log n)</li>
<li>Fast Fourier transform, O(n log n)</li>
<li>Convolutions, Discrete Fourier transform, many types of sorts O (n^2)</li>
<li>General polynomial time O(n^c) (computationally feasible)</li>
<li>solving traveling with dynamic programming exponential O(c^n)</li>
<li>brute force permutations factorial,  O(n!)</li>
</ul>
<p>For Big O notation we usually skip the Best Case and concentrate on the Expected or Worst Case performance. Best Cases are rare and wonderful, unless they happen all the time in which case, they're expected :).</p>
<p><i>Equality and arithmetic operators</i></p>
<p>Unlike many other equality operators you've seen before, <b>this</b> equality operator is not symmetric (<a href="http://en.wikipedia.org/wiki/Big_O_notation#Matters_of_notation">reference</a>).</p>
<blockquote><p>
Equals sign</p>
<p>The statement "f(x) is O(g(x))" as defined above is usually written as f(x) = O(g(x)). Some consider this to be an abuse of notation, since the use of the equals sign could be misleading as it suggests a symmetry that this statement does not have. As de Bruijn says, O(x) = O(x^2) is true but O(x^2) = O(x) is not.[2] Knuth describes such statements as "one-way equalities", since if the sides could be reversed, "we could deduce ridiculous things like n = n2 from the identities n = O(n^2) and n^2 = O(n^2)."[3]</p>
<p>For these reasons, it would be more precise to use set notation and write f(x) ∈ O(g(x)), thinking of O(g(x)) as the class of all functions h(x) such that |h(x)| ≤ C|g(x)| for some constant C.[3] However, the use of the equals sign is customary. Knuth pointed out that "mathematicians customarily use the = sign as they use the word 'is' in English: Aristotle is a man, but a man isn't necessarily Aristotle."[4]
</p></blockquote>
<p>Big O notation can also be used in conjunction with other functions. In particular functions only the most complex or highest order aspect dominates it's Order, i.e. if f(x) = x^2 + x + 3 it's complexity is O(n^2)</p>
<blockquote><p>
Big O notation can also be used in conjunction with other arithmetic operators in more complicated equations. For example, h(x) + O(f(x)) denotes the collection of functions having the growth of h(x) plus a part whose growth is limited to that of f(x). Thus,</p>
<p>    g(x) = h(x) + O(f(x))\,</p>
<p>expresses the same as</p>
<p>    g(x) - h(x) \in O(f(x))\,.
</p></blockquote>
<p>I'll wrap up with an important excerpt from the wikipedia page on the order of complexity for graph theory a vital model for practical programming applications:</p>
<blockquote><p>
Graph theory</p>
<p>It is often useful to bound the running time of graph algorithms. Unlike most other computational problems, for a graph G = (V, E) there are two relevant parameters describing the size of the input: the number |V| of vertices in the graph and the number |E| of edges in the graph. Inside asymptotic notation (and only there), it is common to use the symbols V and E, when someone really means |V| and |E|. We adopt this convention here to simplify asymptotic functions and make them easily readable. The symbols V and E are never used inside asymptotic notation with their literal meaning, so this abuse of notation does not risk ambiguity. For example O(E + VlogV) means O((E,V) \mapsto |E| + |V|\cdot\log|V|) for a suitable metric of graphs. Another common convention—referring to the values |V| and |E| by the names n and m, respectively—sidesteps this ambiguity.
</p></blockquote>
<p>References:<br />
Complexity and Big O notation:</p>
<ul>
<li><a href="http://www.cforcoding.com/2009/07/plain-english-explanation-of-big-o.html">Plain English Explanation of Big O</a></li>
<li><a href="http://en.wikipedia.org/wiki/Big_O_notation">Big O Notation (wikipedia)</a></li>
<li><a href="http://en.wikipedia.org/wiki/Time_complexity">Time Complexity</a></li>
</ul>
<p>The following are not just excellent tips for interviewing, they're practical skills any solid computer scientist should have at their disposal and helped guide this blog series topic coverage.</p>
<ul>
<li><a href="http://sites.google.com/site/steveyegge2/five-essential-phone-screen-questions">Five Essential Phone-Screen Questions</a></li>
<li><a href="http://steve-yegge.blogspot.com/2008/03/get-that-job-at-google.html">Get that job at Google</a></li>
<li><a href="http://www.joelonsoftware.com/articles/GuerrillaInterviewing3.html">Guerilla Interviewing</a> by Joel Spolsky</li>
<li><a href="http://www.joelonsoftware.com/articles/fog0000000043.html">12 Steps to Better Code</a></li>
</ul>
