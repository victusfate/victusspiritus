---
layout: post
status: publish
published: true
title: Visualization layered like music tracks
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9352
wordpress_url: http://www.victusspiritus.com/?p=9352
date: '2011-06-25 06:49:35 -0400'
date_gmt: '2011-06-25 13:49:35 -0400'
categories:
- Uncategorized
tags:
- coding
- html5
- coffeescript
comments:
- id: 10226
  author: The secret art of the tutorial &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/07/05/the-secret-art-of-the-tutorial/
  date: '2011-07-05 20:57:21 -0400'
  date_gmt: '2011-07-06 03:57:21 -0400'
  content: "[...] with CoffeeScript. I&#8217;ve found it much easier to dive in with
    client side CoffeeScript examples which require only a browser and Jeremy Ashkenas&#8217;
    JavaScript interpreter, than to work [...]"
- id: 10243
  author: Songify delights as a mobile app &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/07/11/songify-delights-as-a-mobile-app/
  date: '2011-07-11 04:57:59 -0400'
  date_gmt: '2011-07-11 11:57:59 -0400'
  content: "[...] was inspired by otomata not long back as well as the broader field
    of cellular automata, and see another opportunity for it&#8217;s simplistic music
    synthesis. That web app provided a [...]"
---
<p>The past couple weeks I've been fascinated by the html5 canvas element. My interest in graphics goes decades back, yet only recent experimentation with CoffeeScript showed me how fun and addicting the peanut butter and jelly combination of client side scripting and html5 canvas are to work with.</p>
<p>Implementing translations and adaptions of graphical JavaScript snippets has proven to be an easy transition into the basics of 2D web graphics. In fact the process has been so much fun that I defy you to devise a more entertaining method of learning CoffeeScript<sup><a href="#notes">1</a></sup>.</p>
<p>After mimicking a few intriguing examples, I contemplated how to combine the effects without overburdening the browser. Each small script pushes even Chromium's JavaScript interpreter to its limits. The analogy of each canvas layer to a separate music track lead me to consider pre-rendered gifs, but that implementation would lose any interactive features. Alternatively I could write all the image updates to the same canvas element, and render it to the browser once.</p>
<p>I can't imagine smoothly rendering multiple canvas elements simultaneously without a form of parallelism, lower level code, or dramatically shrinking each canvas. It turns out there are quite a few tricks I can try to speed up both individual and parallel rendering<sup><a href="#notes">2</a></sup>.</p>
<h2>Life in 2D</h2>
<p>The world of 2D pixel graphics unerringly shot my attention like an arrow to <a href="http://en.wikipedia.org/wiki/Conway%27s_Game_of_Life">Conway's game of life</a>. Conway's game set the stage for <a href="http://en.m.wikipedia.org/wiki/Cellular_automaton">cellular automata</a>, a broader field of self replicating patterns (see <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/04/17/otomata-is-beautifully-simple-and-incredibly-addictive/">otomata</a> for a music variant). A simple set of rules and initial state gives rise to complex self perpetuating patterns.</p>
<blockquote><p>
The universe of the Game of Life is an infinite two-dimensional orthogonal grid of square cells, each of which is in one of two possible states, live or dead. Every cell interacts with its eight neighbours, which are the cells that are horizontally, vertically, or diagonally adjacent. At each step in time, the following transitions occur:</p>
<ol>
<li>Any live cell with fewer than two live neighbours dies, as if caused by under-population.</li>
<li>Any live cell with two or three live neighbours lives on to the next generation.</li>
<li>Any live cell with more than three live neighbours dies, as if by overcrowding.</li>
<li>Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.</li>
</ol>
</blockquote>
<p>http://www.youtube.com/watch?v=FdMzngWchDk</p>
<h2>Life with CoffeeScript</h2>
<p>My latest conversion from JavaScript is a non-canvas table based <a href="http://victusfate.github.com/life/">implementation of life</a> from <a href="http://cafaq.cafaq.com/lifefaq/index.php">Conway's Game of Life FAQ</a>. When time allows I'll add an interactive canvas version. Click the image below to see it:<br />
<a href="http://victusfate.github.com/life/"><img src="{{ site.url }}/assets/2011/06/life_table.png" alt="" title="life_table" width="825" height="848" class="aligncenter size-full wp-image-9356" /></a></p>
<p>The relevant coffeescript source:<br />
<script src="https://gist.github.com/1046449.js"> </script></p>
<p><a href="#notes" id="notes">Notes:</a></p>
<ol>
<li>Server side CoffeeScript in <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/05/30/clientside-coffeescript-with-jquery/">Henri Bergius' gist (bottom of post)</a> on the Falsy Values node.js tutorials is a strong contender, but requires a couple of additional steps to dive in (installing node/npm)</li>
<li><a href="https://developer.mozilla.org/en/Using_web_workers">Web Workers</a> are one way to perform calculations leveraging multiple cpus. Each completed canvas would need to be handled by a separate thread, and the initial worker API limited their ability to modify DOM elements. The good news is the browser vendors have augmented the API to allow imagedata to be manipulated by workers, but it'll take some tuning to leverage efficiently (limit data copying, distribute processing to workers)<br />
Pixel manipulation <a href="http://www.forestpath.org/notes/html/html5">source</a><br />
<script src="https://gist.github.com/1046362.js"></script><br />
Additional references: <a href="http://stackoverflow.com/questions/1864756/web-workers-and-canvas/3229118#3229118">stack question</a>, <a href="http://nooshu.com/mandelbrot-renderer-update">mandlebrot renderer</a> and this <a href="http://nooshu.com/mandelbrot-renderer-update#comment-295">comment</a> </li>
</ol>
