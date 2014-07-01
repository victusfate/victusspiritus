---
layout: post
status: publish
published: true
title: First Steps Sorting out Python
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8713
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/05/02/first-steps-sorting-out-python/
date: '2011-05-02 06:29:24 -0400'
date_gmt: '2011-05-02 13:29:24 -0400'
categories:
- Uncategorized
tags:
- coding
- python
comments:
- id: 9882
  author: Greg Johnson
  author_email: gregfjohnson@yahoo.com
  author_url: ''
  date: '2011-05-02 15:36:00 -0400'
  date_gmt: '2011-05-02 15:36:00 -0400'
  content: |
    Here was my newb attempt at a python qsort.  It uses list comprehensions.  I really
    like how clean it is.

    def qsort(a):

        # a really short list is already sorted.  this is the (non-recursive)
        # base case.

        if len(a) &lt;= 1:
            return a

        # this is the inductive step, which recursively calls the routine
        # on lists that are known to be shorter than the input list.

        # pick an arbitrary element of list &#039;a&#039; (we choose a[0] but it
        # could have been anything).

        pivot = a[0]

        # grab the elements smaller than pivot, the elements equal to
        # pivot, and the elements bigger than pivot.

        smaller   = [value for value in a if value   pivot]

        # recursively sort the lists of smaller and bigger elements,
        # and glue the result together.

        result = qsort(smaller)

        result.extend(equal)

        result.extend(qsort(bigger))

        return result
- id: 9883
  author: Nobody
  author_email: nobody@yopmail.com
  author_url: ''
  date: '2011-05-02 15:57:00 -0400'
  date_gmt: '2011-05-02 15:57:00 -0400'
  content: |-
    Your merge_sort doesn't sort the values (nor does it merge them either).
    In fact your merge_sort function split your list into 3 parts (left, right and a middle value), and creates a new list by appending the values in the same order they were to begin with.
    For instance if you send [5, 4, 2, 8, 3] as an input, your function will return [5, 4] + [2] + [8, 3].

    You can look at the pseudocode from wikipedia (http://en.wikipedia.org/wiki/Merge_sort) to see how the merge sort works, the translation to python is pretty straightforward :

    def merge_sort(lst):
        if len(lst) &lt;= 1:
            return lst
        else:
            l = len(lst)
            mid = len(lst)/2
            left, right = [], []
            for x in lst[:mid]:
                left.append(x)
            for x in lst[mid:]:
                right.append(x)
            left = merge_sort(left)
            right = merge_sort(right)
        return merge(left, right)

    def merge(left, right):
        result = []
        while len(left) or len(right):
            if len(left) and len(right):
                if left[0] &lt;= right[0]:
                    result.append(left[0])
                    left = left[1:]
                else:
                    result.append(right[0])
                    right = right[1:]
            elif len(left):
                result.append(left[0])
                left = left[1:]
            elif len(right):
                result.append(right[0])
                right = right[1:]
        return result

    As a side note, it is not recommended to use &#039;sorted&#039; or &#039;list&#039; as variable names, as they are builtin functions in Python.
- id: 9885
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-02 18:15:00 -0400'
  date_gmt: '2011-05-02 18:15:00 -0400'
  content: crap I forgot the ordered merge and it's the most important step! Good
    catch, I didn't verify the outputs.
---
<p>After wrapping up a little c++ code and a fantastic walk yesterday morning, I settled down in front of my iMac without an immediate looming task and it felt grand. Twitter's an unmatched wide band serendipity delivery engine, and in a few minutes I found myself reading about <a href="http://morepypy.blogspot.com/2011/04/pypy-15-released-catching-up.html">pypy's 1.5</a> alpha release. Even if you're far removed from code, you've likely at least heard of Python but...</p>
<blockquote><p>
<bold>What is PyPy?</bold></p>
<p>PyPy is a very compliant Python interpreter, almost a drop-in replacement for CPython 2.7.1. It's fast (pypy 1.5 and cpython 2.6.2 performance comparison) due to its integrated tracing JIT compiler.</p>
<p>This release includes the features of CPython 2.6 and 2.7. It also includes a large number of small improvements to the tracing JIT compiler. It supports Intel machines running Linux 32/64 or Mac OS X. Windows is beta (it roughly works but a lot of small issues have not been fixed so far). Windows 64 is not yet supported.
</p></blockquote>
<p>I've been wanting to <a href="http://diveintopython3.org/your-first-python-program.html">dive into python</a> for a while now and even setup pythonbrew (which regretfully doesn't play nicely with pypy), but the opportunity never presented itself. I pounced on the momentary lapse of my many time eating overlords, and decided to explore how the sorting code I'd recently written in c++ might take shape in Python.</p>
<p>Low and behold, StackOverflow revealed breadcrumbs of another developer new to Python who shared an example of qsort, thanks <a href="http://stackoverflow.com/questions/4322823/how-to-make-this-naive-python-implement-of-quicksort-more-pythonic">Frankie</a>. I eased into this example which was more readable (for a python newb) than the one liner scripts I came across elsewhere. I'm not against one liners, but I'll work that style after I get the fundamentals. Frankie's quicksort's form was similar to the qsort with temporary lists impl I coded Saturday morning, versus the slightly more tricky in place variant (yeah, I screwed that up the first time).</p>
<p>The brand spanking new <a href="https://github.com/victusfate/py-util">py-util repo</a> includes only a single short python script which contains a merge sort in addition to a qsort. Without further delay here come...</p>
<h1>the Sorts</h1>
<p><b>Update</b> I left out a critical step in mergesort, the MERGE! There was an error with merge sort and I haven't tested the fix yet. See the comment below for a good example how to mergesort (thanks, appreciate the correction). I'll test out the fix I edited on github tonight. The good news I got to learn some more python syntax with extend. I coded the merge how I would in c/c++, there may be some tricks in python I'm missing.<br />
<script src="https://gist.github.com/951479.js?file=sorts.py"></script></p>
<h1>Readme & Run Example</h1>
<p>The tweaks to Frankie's version and merge sort took only a few delightful moments with the aid of just two helpful interpreter error messages. The big surprise was in the execution times. PyPy ran ~8x faster than my Mac's default cpython (7.1) and it's comparable to my c++ qsort (in place is still faster). I've embedded the readme and results file below:<br />
<script src="https://gist.github.com/951494.js?file=py-util-readme.md"></script></p>
<p>That wraps up my first steps in Python. Future py-posts may include web frameworks Flask and Django, datamining examples, number crunching with numpy (we'll see if/how this jives with pypy) with an outside chance of opencv python bindings and image processing. </p>
<p>The latter is unlikely because each man or woman is apportioned only so many years of image manipulation per lifetime, and I've far exceeded my lot. One of the few forces outside of a paying gig that could coerce me into image processing would be a mobile app. But for that I'd use objective c or java bindings(?) to opencv or roll my own image processing lib.</p>
<p>Gratuitous Notes:</p>
<ol>
<li>Excellent python references:
<ul>
<li><a href="http://diveintopython3.org/your-first-python-program.html">Dive into Python</a> thanks Mr. Pilgrim, I've grown to cherish well written docs</li>
<li><a href="http://docs.python.org">Docs.python.org</a> aren't too shabby either, actually they're outstanding</li>
<li>An endless stream of docs from my <a href="http://www.instapaper.com/folder/952699/rss/419835/4zvNFfgw07bdO7xB3CN7QidITk">Instapaper pythonic feed</a></li>
</ul>
</li>
<li>Related post: <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/04/30/folding-in-c">Folding in c++</a> (the repo referenced includes array splitting and in place qsorts)</li>
</ol>
<p><script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.5.1/jquery.min.js"></script><br />
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.10/jquery-ui.min.js"></script><br />
<script type="text/javascript"<br />
src="https://gist.github.com/raw/949945/1468755b2659aa0206ef4b0060100b152f44a8d3/growingdivs.js"></script></p>
