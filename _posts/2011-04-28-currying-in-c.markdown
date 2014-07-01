---
layout: post
status: publish
published: true
title: Currying in c++
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8662
wordpress_url: http://www.victusspiritus.com/?p=8662
date: '2011-04-28 15:31:20 -0400'
date_gmt: '2011-04-28 22:31:20 -0400'
categories:
- Uncategorized
tags:
- coding
- c++
comments:
- id: 9870
  author: Folding in c++ &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/04/30/folding-in-c/
  date: '2011-04-30 06:54:20 -0400'
  date_gmt: '2011-04-30 13:54:20 -0400'
  content: "[...] Currying in c++  //   Share and Enjoy: [...]"
- id: 10023
  author: kiki
  author_email: deimos13710@gmail.com
  author_url: ''
  date: '2011-05-23 08:00:00 -0400'
  date_gmt: '2011-05-23 08:00:00 -0400'
  content: 'WTF, sir. You use variadic argument ?? You could have used  variadic template
    instead. available in GCC 4.6 '
- id: 10025
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-23 13:00:00 -0400'
  date_gmt: '2011-05-23 13:00:00 -0400'
  content: "Oh my, what have I done.\r\nI'll look into variadic templates asap."
---
<h2>Variable argument parameter lists</h2>
<p>While brushing up on some coding samples I came across va_args which is included within the stdargs header file. Here's an example of how it's used:<br />
<script src="https://gist.github.com/946781.js"> </script></p>
<pre>
To compile:
g++ va_args_test.cpp -o va_args 

it outputs:
>>Ten (doubles)10 twelve 12
>>Ten (longs)10 twelve 12

</pre>
<p>This triggered a mad idea and became part one of my many tiered master plan to mold c++ into my unwilling modern feeling, syntactically sugar coated servant (<a href="http://rubini.us/">fallback</a>). We'll see how far I get. Next up, currying! I leaned heavily on void* to make it work, and leveraged typedef to aid readability. Bear with me, the source is a little longer:<br />
<script src="https://gist.github.com/947474.js?file=curry.cpp"></script></p>
<p>The code takes sCurry<double>(nargs,function_pointer1,function_pointer2...,val) and computes it. Yeah I know boost has functors, good for that 80 trillion byte library ;).</p>
<p>Here's an example of it run:</p>
<pre>
Mark-Essels-iMac:misc messel$ g++ curry.cpp -o curry
Mark-Essels-iMac:misc messel$ ./curry 2
Address to base numeric 0x7fff5fbfdbc8 base val 2
extracting val from curry 2
temp 2 val 1
temp 2 val 1
addOne-> 3 curried addOne 3
start curry val 3
extracting val from curry 3
temp 3 val 1
temp 4 val 2
temp 8 val 7
temp 1 val 10
curried output f10(f7(f2(f1(val)))) or ((val+1)*2-7)/10 = 0.1
</pre>
<p>Next up, dynamic typing without boost::any...maybe.</p>
<p>Notes:</p>
<ul>
<li><a href="http://en.wikipedia.org/wiki/Currying">Currying</a></li>
<li><a href="http://en.wikipedia.org/wiki/Higher_order_function">Higher order functions</a></li>
<li><a href="http://en.wikipedia.org/wiki/Fold_(higher-order_function)">Fold</a></li>
<li><a href="http://en.wikipedia.org/wiki/Function_composition_(computer_science)">Function composition</a></li>
</ul>
<p><script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.5.1/jquery.min.js"></script><br />
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.10/jquery-ui.min.js"></script><br />
<script type="text/javascript"<br />
src="https://gist.github.com/raw/949945/1468755b2659aa0206ef4b0060100b152f44a8d3/growingdivs.js"></script></p>
