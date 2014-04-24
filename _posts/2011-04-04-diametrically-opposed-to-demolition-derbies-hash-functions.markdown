---
layout: post
status: publish
published: true
title: Diametrically opposed to demolition derbies, Hash Functions
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8239
wordpress_url: http://www.victusspiritus.com/?p=8239
date: '2011-04-04 06:14:00 -0400'
date_gmt: '2011-04-04 13:14:00 -0400'
categories:
- Uncategorized
tags:
- math
- coding
- computer science
comments:
- id: 9769
  author: custom research paper
  author_email: markthesmith76@yahoo.com
  author_url: http://bestresearchpaper.com/
  date: '2011-04-05 08:15:00 -0400'
  date_gmt: '2011-04-05 08:15:00 -0400'
  content: great article. so simple and so informative.  plus..i dont know how could
    it ever happen but i 've just discovered you site and i never saw it before. very
    beautiful and just amazing! thanks!!)
---
<p>With little doubt each and every one of you arose this fine spring morning just as excited about hashing as myself. Like all interesting algorithms, the proud tradition of identifying effective hashing functions requires a mathematician's razor mind and an artist's subtle touch. If you know of anyone who has either of these attributes don't hesitate to hold an image of them in your mind as you scan the rest of this article.</p>
<p><I>Quick Hash Function</i></p>
<p>Within the hallowed pages of the Algorithm Design Manual, Steve Skiena* describes a straightforward Hashing function between strings S of length |S|, with alphabet A, and a length m hash table. </p>
<ul>
<li>First identify a set of integers which contains all possible allowed key values. Let's assume your alphabet is two characters { "a", "b" } and your strings all have length 4. Example keys would be "aaaa", "aaab", "bbbb" or any combination of letters. The total number of possibilities are A^|S|, 2^4 or 16. </li>
<p></p>
<li>Next construct integer values from these strings by applying a base-A numeric conversion. The combinations yield corresponding integer values between 0-15, if we replace the letters with binary values "a"=0, "b"=1 and convert to integers. Note how the keys form a headless binary tree with left and right child nodes taking on the values "a" or "b". This method may be extended to as large an alphabet as is desired, ie "c"=2 (base-3), "d"=3 (base-4),...,"j"=9 (base 10), etc.</li>
<p></p>
<li>
We're restricted to a total number of slots m in our table, so each of these integers must map back into values 0 to m-1. The mod function takes any integer and yields its remainder in the allowed range. The final index is I mod m.
</li>
</ul>
<p><I>Table Collisions</i></p>
<p>The worst hashing function will generate the same index for all keys. Even for the best functions the locations that result from the hash are not guaranteed to avoid collisions. Collisions are common even for uniform distributions, see the Birthday Problem for details. </p>
<p>Recommended solutions to collisions include doubly linked lists, or open addressing where the former is more popular but also consumes more memory for pointers. </p>
<p>For hash buckets with doubly linked lists when writing we append the new value to the list, when reading scan through the list for the desires key. </p>
<p>Open addressing writes to the next available memory location at a hashed index. Reading requires scanning through adjacent memory locations, and deletions require reinserting any broken runs of nodes (ouch). </p>
<p>I haven't read mention of it but busy hash tables could have trees implemented at each bucket. If a hash table becomes congested (<a href="http://stackoverflow.com/questions/371136/binary-trees-vs-linked-lists-vs-hash-tables">which data structure</a>), you're likely better off using a tree implementation. When n is small you're better off with a list.</p>
<p>References:</p>
<ul>
<li><a href="http://www.victusspiritus.com/2011/03/16/brushing-up-on-computer-science-part-3-data-structures/">Brushing Up on Comp Science, Data Structures</a></li>
<p></p>
<li><a href="http://www.amazon.com/gp/product/B0016H523Q/ref=as_li_ss_tl?ie=UTF8&tag=dream06-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B0016H523Q">The Algorithm Design Manual</a>, a valued resource. I highly recommend buying a few thousand digital copies for your university or corporation via this link :)</li>
<p></p>
<li>The <a href="http://en.m.wikipedia.org/wiki/Birthday_problem">Birthday Problem</a></li>
<p></p>
<li>For more complex hashing functions, see the end of <a href="http://www.victusspiritus.com/2011/03/17/brushing-up-on-computer-science-part-4-algorithms/">Brushing up on Computer Science, Algorithms</a> for presentations which discuss MD5 and Sha1 hash functions.</li>
</ul>
<p>Notes:<br />
*= I'm reminded of a conversation between Professor Skiena and a student over a decade ago. I took an algorithm overview course a few years after I graduated when taking additional grad courses was a good excuse to slip out of the office for a couple of hours. Now I recommend reading and working with other peers on the cheap. </p>
<p>Myself and two colleagues who also took the course were waiting outside Steve's office to discuss our final project. A foreign student was ahead of us in a meeting, and we overhead Steve going into detail as he described the Thanksgiving Holiday ritual: "A huge turkey...stuffing...yams..." From the conversation, I could imagine the student salivating over the description of the bountiful meal, and we were inclined to believe Steve may extend an invite to the student to introduce him to the holiday. We were surprised as the meeting wrapped up with Steve mentioning "it's really quite a fun event, you should.. you should get one of your friends to invite you over". Steve's generous with his dynamic programming knowledge and algorithmic mastery, but bring your own Turkey dinner ;).</p>
