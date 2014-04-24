---
layout: post
status: publish
published: true
title: Folding in c++
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8677
wordpress_url: http://www.victusspiritus.com/?p=8677
date: '2011-04-30 06:54:08 -0400'
date_gmt: '2011-04-30 13:54:08 -0400'
categories:
- Uncategorized
tags:
- coding
- c++
comments:
- id: 9881
  author: First Steps Sorting out Python &mdash; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/05/02/first-steps-sorting-out-python/
  date: '2011-05-02 06:30:09 -0400'
  date_gmt: '2011-05-02 13:30:09 -0400'
  content: "[...] post: Folding in c++ (the repo referenced includes array splitting
    and in place [...]"
- id: 9889
  author: John Haugeland
  author_email: johnhaugeland@yahoo.com
  author_url: ''
  date: '2011-05-03 20:43:00 -0400'
  date_gmt: '2011-05-03 20:43:00 -0400'
  content: |-
    This has to be the densest, most garbage-ridden attempt to reinvent std::accumulate() I've ever seen.

    More proof that you need to think really, really hard before listening to a blogger.
- id: 9890
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-03 21:21:00 -0400'
  date_gmt: '2011-05-03 21:21:00 -0400'
  content: "John have you implemented or read through STD::accumulate? I just heard
    of it from another commenter recently and would love to hear some experienced
    insight on it's impl.\r\n\r\nI was experimenting with functions calling functions.
    It works but I made no claims it was the only, best or even good way to do it.
    What didn't you like about the way I did it?"
- id: 9901
  author: Linux Jon
  author_email: linux.jon@gamils.jon
  author_url: ''
  date: '2011-05-05 07:03:00 -0400'
  date_gmt: '2011-05-05 07:03:00 -0400'
  content: |-
    I can see Johns point, even if he is a little harsh. Just look at some  mArray implementation issues:

    Exposing namespace std in a header file.
    Use of long instead of size_t for unsigned quantities.
    Your members should be named like the stl, e.g. nuke() should be clear().
    No STL like typedefs for size_type, iterators, value_type etc.
    Exits the program rather than throwing exceptions, although can still throw exceptions through operator new.
    Bizarre semantics (copy with NULL pointer doesn't do anything?).
    C style variable declarations (put the variable in the for loop).
    Public internal functions.
    Operator= doesn't check for self assignment.
    Protected members but no virtual dtor - make them private if you don't want people to inherit from it.

    I could go on, but as John points out, this code doesn't need to be written at all.

    &gt; But template functions (like my array) are not POD and so aren't supported by this.

    Its a template class, not a function. And accumulate doesn't require POD data.

    Good luck on your travels through c++.
- id: 9905
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-05 09:37:00 -0400'
  date_gmt: '2011-05-05 09:37:00 -0400'
  content: "Great feedback!\r\nI have heard exposing STD namespace in headers was
    poor form, but never practically experienced why. Mind explaining the thinking
    here?\r\n\r\nlong use is admittedly old habit, size_t or unsigned long would be
    a fine choice. Negatives enable circular ques derived from something like this
    structure.\r\n\r\nThrow vs exception, again for my purposes either is acceptable.
    I prefer a full stop when classes are misused or memory allocation fails, as it
    is usually a systemic failure.\r\n\r\nIf I tell you to copy nothing, I should
    hope you'd do nothing :). How's that bizarre?\r\n\r\nI reuse the looping vars
    in larger programs, sometimes breaking ou of loops and keeping knowledge of when,
    again old habit.\r\n\r\nNot checking for self assignment was poor form. I should
    have done that automatically, great catch! I've been wrestling for months at work
    with models far removed from low level data structures.\r\n\r\nNaming- if nuke
    makes no surprises over clear, renaming it isn't an issue. I wasn't looking at
    existing stl formats at the time, just coding from what I wanted out of an array
    structure.  I erred on the side of least surprise with a unique name.\r\n\r\nstl
    typedefs, hmm. I'll have to look in to the value of such.\r\n\r\nAppreciate the
    feedback. \r\n\r\nAlthough the code is written elsewhere, doesn't mean the experience
    of writing it yourself isn't worth doing. Stepping through stl or boost code can
    be an exercise in patience, it has its costs."
- id: 9964
  author: Jon
  author_email: linux.jon@gmail.com
  author_url: ''
  date: '2011-05-15 03:59:00 -0400'
  date_gmt: '2011-05-15 03:59:00 -0400'
  content: |-
    &gt; Mind explaining the thinking here?
    It creates abiguity for users of your header who have clashing types/variables in their own namespace.

    If you are thinking about indexing using negative numbers for indexing you aren't really in the c++ mindset I'd wager. You should be using insert_iterators and reverse iterators to go backwards/add backwards. Indexing is generally poor form compared to using iterators/algorithms (e.g. std::accumulate/std::transform as pointed out above).

    &gt;If I tell you to copy nothing, I should hope you'd do nothing :). How's that bizarre?

    Null is semantically different from an empty collection. Allowing NULL to propigate through your programs is generally a bad idea, particularly in larger apps. You cannot tell an invalid ptr from an empty collection.

    The value of providing stl compatible methods and typedefs is that you don't need to document your classes as heavily, and std algorithms will work on them automatically.
- id: 9965
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-15 10:23:00 -0400'
  date_gmt: '2011-05-15 10:23:00 -0400'
  content: |-
    I can appreciate the commonality of stl iteration over any supporting collections, even if I'm rusty at using stl structures (recently that's changed in the last 2-3 months, maps of key/ptrs come in handy).

    As to corrupting namespaces, I recognize the importance as code bases grow, I just haven't run into naming problems too often. In the past we used names like (Lib)(Utility) to avoid conflicts. Only in my current integration work have I had to really be careful with our older libraries includes. I'll do a full sweep on namespaces in headers, based on your feedback. I don't want to step on other folks vector definitions because I lazily added using namespace std in headers. The one bonus is that it kept us from ever reusing stl reserved class names.

    Thanks again for taking time to explain your rationale.
---
<p>Today's post is short and sweet, like a peach. </p>
<p>On the odd chance you're morbidly curious how to fold an array with a function in c++ like myself, you're in for a pleasant surprise (unless you're intimately familiar with <a href="http://www.boost.org/doc/libs/1_46_0/libs/mpl/doc/refmanual/fold.html">boost's lambdas</a>, in which case you will be appalled at how little thought was put into this whimsical hack).</p>
<p>This morning I cleaned up my proj (<a href="https://github.com/victusfate/proj">fork it</a>) utility library and added an Array structure with a foldRight member, and refactored curry to take in either a va_arg parameter list or a mArray of functions.</p>
<p>I make no claims about its stability or memory non-leakiness of the data structure although a hundred million delete and allocation calls had a stable memory footprint.</p>
<p>It all starts with Fptr.h:<br />
<script src="https://gist.github.com/949676.js"> </script></p>
<p>the new hotness of mArray.h (I pronounce it emory as in memory)<br />
<script src="https://gist.github.com/949678.js"> </script></p>
<p>the test program for folding, sort.cpp (<del>naming fail</del> now it sorts too):<br />
<script src="https://gist.github.com/949679.js"> </script></p>
<p>the test program for curry:<br />
<script src="https://gist.github.com/949681.js"> </script></p>
<p>Side note: I had some trouble embedding javascript directly in this post but I hacked together a gist which makes gists wider, and in a metatastic way it makes itself wider:<br />
<script src="https://gist.github.com/949945.js"> </script></p>
<p>Here's the scripts I included below:<br />
<script src="https://gist.github.com/949951.js"> </script></p>
<p>Related posts:</p>
<ul>
<li><a href="http://www.victusspiritus.com/2011/04/28/currying-in-c/">Currying in c++</a></li>
</ul>
<p><script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.5.1/jquery.min.js"></script><br />
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.10/jquery-ui.min.js"></script><br />
<script type="text/javascript"<br />
src="https://gist.github.com/raw/949945/1468755b2659aa0206ef4b0060100b152f44a8d3/growingdivs.js"></script></p>
