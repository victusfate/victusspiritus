---
layout: post
status: publish
published: true
title: How to bind class methods to global functions in CoffeeScript
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9376
wordpress_url: http://www.victusspiritus.com/?p=9376
date: '2011-06-27 03:20:40 -0400'
date_gmt: '2011-06-27 10:20:40 -0400'
categories:
- Uncategorized
tags:
- coding
- coffeescript
comments: []
---
<p>This morning's post is about a sticky piece of syntax I came across in CoffeeScript this weekend. I presume the problem arose due to several causes including my weekend laziness, the disconnect of errors from JavaScript to CoffeeScript, and partly because I wasn't compiling the CoffeeScript into JavaScript to iteratively inspect the code.</p>
<p>My goal was to pass a class method to setTimeout, and have it loop. Below I show each step and what was missing along with it's compiled JavaScript.</p>
<h2>First cut:</h2>
<p>The class GameOfLife contains an "update" method which takes in a single argument with a default parameter. The argument is compared with an internal member variable and if equal the time out id is cleared and play is paused.<br />
<script src="https://gist.github.com/1048552.js"> </script><br />
If you're familiar with JavaScript you may notice that the update method passed to setTimeout is inaccessible. I wasn't reviewing the compiled JavaScript at the time, so it took me a little longer to see. Eventually I came to the same conclusion.</p>
<h2>Second take:</h2>
<p>This version of the passed method I enclosed in an anonymous function wrapper and tried slapping the function onto the window object to make it accessible everywhere. This turned out being a bad idea because the window object doesn't have all the other members and methods the update function relies on. But it did bring me closer to working code.<br />
<script src="https://gist.github.com/1048586.js"> </script></p>
<h2>Third time's a charm:</h2>
<p>Finally, after several interweb searches and rereading CoffeeScript docs it struck me. This is the perfect time for the FAT arrow. This time I passed in an anonymous function with the fat arrow
<pre>=></pre>
<p> to bind the method always to the GameOfLife class it was called from, and removed the update function from the window object (whew). Eureka, it worked!<br />
<script src="https://gist.github.com/1048590.js"> </script></p>
<p>You can see the wiggling results at my <a href="http://victusfate.github.com/life/">html5 life</a> page.</p>
