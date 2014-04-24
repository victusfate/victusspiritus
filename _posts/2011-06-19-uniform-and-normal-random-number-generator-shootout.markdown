---
layout: post
status: publish
published: true
title: Uniform and Normal Random Number Generator Shootout
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9305
wordpress_url: http://www.victusspiritus.com/?p=9305
date: '2011-06-19 12:04:33 -0400'
date_gmt: '2011-06-19 19:04:33 -0400'
categories:
- Uncategorized
tags:
- coding
comments: []
---
<p>If you have a definitive need for speed like myself, then standard tactics for random number generation simply won't do. In the project I'm working on I don't include or link to Boost (<a href="http://www.boost.org/doc/libs/1_46_1/boost/random/mersenne_twister.hpp">Mersenne Twister</a>) because it's a small delivery, so I went hunting for a fast, reliable, and well packaged random number generator. I remembered reading John D. Cook's blog post sharing precisely what I was looking for. The fastest approach I could generate quickly is a cached version of a large number of normal calls accessed by a uniform call in the loop.</p>
<p>First the source (here's the <a href="https://github.com/victusfate/proj">repo</a> where I keep my c++ utils):<br />
<script src="https://gist.github.com/1034598.js"> </script></p>
<p>And of course the results:</p>
<blockquote>
<h1>Random number generator speed tests</h1>
<p>Thanks to <a href="http://www.johndcook.com/cpp_random_number_generation.html">John D. Cook</a></p>
<p>to build on *nix:</p>
<pre>g++ -O3 -o testRNG testRNG.cpp SimpleRNG.cpp -lm</pre>
<p>Quality test:</p>
<pre>
Mark-Essels-iMac:proj messel$ ./testRNG 1000000
rng get uniform time 0.012 mean 0.499806 stddev 0.2887
rand() get uniform time 0.013 mean 0.50003 stddev 0.288526
generated normal 0.135 mean 0.000684646 stddev 1.00001
rng Normal time 0.085 mean 0.000477835 stddev 0.999851
rng stored normal accessed with uniform 0.006 mean 0.000477835 stddev 0.999851
</pre>
<p>Speed test: note, with optimizations John's uniform was faster so I used it for the cached normal approach</p>
<pre>
Mark-Essels-iMac:proj messel$ ./testRNG 100000000
rng get uniform time 1.030
rand() get uniform time 1.178
generated normal 14.099
rng Normal time 8.393
rng stored normal accessed with uniform 0.486
</pre>
</blockquote>
