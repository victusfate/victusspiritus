---
layout: post
status: publish
published: true
title: The joy of function chaining and callbacks with jQuery and underscore.js
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 6986
wordpress_url: http://www.victusspiritus.com/?p=6986
date: '2011-01-29 14:56:59 -0500'
date_gmt: '2011-01-29 21:56:59 -0500'
categories:
- Uncategorized
tags:
- coding
- javascript
- jquery
- underscore.js
comments:
- id: 8218
  author: Tweets that mention The joy of function chaining and callbacks with jQuery
    and underscore.js » Victus Spiritus -- Topsy.com
  author_email: ''
  author_url: http://topsy.com/www.victusspiritus.com/2011/01/29/the-joy-of-function-chaining-and-callbacks-with-jquery-and-underscore-js/?utm_source=pingback&amp;utm_campaign=L2
  date: '2011-01-29 15:45:16 -0500'
  date_gmt: '2011-01-29 22:45:16 -0500'
  content: "[...] This post was mentioned on Twitter by Mark Essel and Mark Essel,
    HN Firehose. HN Firehose said: The joy of function chaining and callbacks with
    jQuery and underscore.js: http://bit.ly/dRxuHq [...]"
- id: 8417
  author: bscopes
  author_email: bradandsteve@bscopes.com
  author_url: http://blog.bscopes.com
  date: '2011-01-31 15:08:00 -0500'
  date_gmt: '2011-01-31 15:08:00 -0500'
  content: 'Mark: Thanks for the details. I''ve been using jQuery for a while now,
    but still found some useful new tips on both chaining and callbacks. Could you
    go into a bit more detail on why directly passing the function with 2 params is
    bad but passing an anonymous function definition with 0 params that only calls
    the other function is good? You lost me on that part.'
- id: 8440
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-01-31 18:23:00 -0500'
  date_gmt: '2011-01-31 18:23:00 -0500'
  content: "Your very welcome.\n\nThe version of the function that passes in arguments
    in the call will actually call the function first and pass in whatever it returns.
    From the source I linked to:\nWrong\n\nThe Wrong Way (will not work!)\n\n $.get('myhtmlpage.html',
    myCallBack(param1, param2));\n\n\nThis will not work because it calls\n\nmyCallBack(param1,
    param2)\n\nand then passes the return value as the second parameter to $.get() "
- id: 8444
  author: bscopes
  author_email: bradandsteve@bscopes.com
  author_url: http://blog.bscopes.com
  date: '2011-01-31 18:32:00 -0500'
  date_gmt: '2011-01-31 18:32:00 -0500'
  content: 'Mark: that explains it. Thanks!'
- id: 8560
  author: FAKE GRIMLOCK
  author_email: FAKEGRIMLOCK@FAKEGRIMLOCK.COM
  author_url: ''
  date: '2011-02-01 06:46:00 -0500'
  date_gmt: '2011-02-01 06:46:00 -0500'
  content: ME, GRIMLOCK, SOMEHOW NOT KNOW ABOUT UNDERSCORE.JS. LOVE IT! WILL USE IMMEDIATELY
    IN NEXT PROJECT.
---
<p>What language features do you rely on while coding? In my own work and others' code (while wearing my app developer hat) I look for the following utilities:</p>
<blockquote>
<ol>
<li>readability (minimize line noise and arcane symbols/parens)</li>
<li>mostly working code (see 1)</li>
<li>powerful data and algorithmic manipulation</li>
<li>light interface definitions from <a href="http://en.wikipedia.org/wiki/Structural_type_system">structure</a> or runtime <a href="http://en.wikipedia.org/wiki/Type_system#Dynamic_typing">symbols</a> (boo to static typing/complex inheritance)</li>
<li>efficiency whenever practical (impatient, frugal)</li>
</ol>
</blockquote>
<p>The above priority set leads to trade offs. What I'm learning more about today will help with everything on that list. Function chaining helps with 1-4. The chain leads to readable code that works, enables powerful manipulation of data and processing, and <i>can be</i> a light interface in dynamic scripting languages (like javascript). <a href="http://en.wikipedia.org/wiki/Callback_(computer_programming)">Callbacks</a> aid 4-5 by providing functional flexibility (execute this code block when you're done) and prevent blocking code from slowing event driven software down (gui's, distributed apps, servers). Let's jump right in with specific examples of chaining and callbacks with javascript.</p>
<h2>Chaining Examples</h2>
<p><a href="http://ejohn.org/blog/ultra-chaining-with-jquery/">Ultra-Chaining with jQuery</a> captures John Resig's early thoughts on how jQuery would handle chaining, and those ideas have matured in the latest library releases. Here's a straight forward example of chainable animation effects from the <a href="http://www.webdesignerwall.com/tutorials/jquery-tutorials-for-designers/">web designer wall</a><br />
<script src="https://gist.github.com/802003.js?file=jquery%20chaining%20example"></script></p>
<p>The following is a live example of the above code:<br />
[iframe http://jsfiddle.net/victusfate/GQG4F/1/embedded/result/ 500 400]</p>
<p><i>Process Chaining</i><br />
Thanks to <a href="http://twitter.com/HenrikJoreteg">Henrik Joreteg</a> (a talented web hacker at <a href="http://andyet.net/">andyet.net</a>) for calling <a href="http://documentcloud.github.com/underscore/">underscore.js</a> to my attention yesterday.<br />
[blackbirdpie url="http://twitter.com/HenrikJoreteg/status/30859394296057856"]<br />
 (emphasis mine).</p>
<blockquote>
<h3>Underscore.js</h3>
<p>Underscore is a utility-belt library for JavaScript that provides a lot of the functional programming support that you would expect in Prototype.js (or Ruby), but without extending any of the built-in JavaScript objects. <strong>It's the tie to go along with jQuery's tux</strong>.
</p></blockquote>
<p>For another great example of function chaining see the following:<br />
<script src="https://gist.github.com/802013.js?file=underscore.js%20chaining%20sample"></script></p>
<h2>Callback Examples</h2>
<p>The <a href="http://docs.jquery.com/Tutorials:How_jQuery_Works#Callback_and_Functions">jQuery documentation on callbacks</a> gives a few one line descriptions for callback functions with and without arguments.</p>
<blockquote><p>
CALLBACK AND FUNCTIONS</p>
<p>A callback is a function that is passed as an argument to another function and is executed after its parent function has completed. The special thing about a callback is that functions that appear after the "parent" can execute before the callback executes. Another important thing to know is how to properly pass the callback. This is where I have often forgotten the proper syntax.<br />
</blockquote.<br />
Good, Callback without arguments</p>
<pre>$.get('myhtmlpage.html', myCallBack);
</pre>
<p>Bad, WRONG way to pass callbacks with args</p>
<pre> $.get('myhtmlpage.html', myCallBack(param1, param2));
</pre>
<p>Good, Right way to callback with args</p>
<pre>$.get('myhtmlpage.html', function(){
  myCallBack(param1, param2);
});
</pre>
</blockquote>
<p><a href="http://www.amazon.com/gp/product/B0026OR2ZY?ie=UTF8&tag=dream06-20&linkCode=as2&camp=1789&creative=390957&creativeASIN=B0026OR2ZY">JavaScript: The Good Parts</a><img src="http://www.assoc-amazon.com/e/ir?t=dream06-20&l=as2&o=1&a=B0026OR2ZY" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" /><br />
Javascript: The Good Parts discusses callbacks in detail. </p>
<blockquote>
<h2>Callbacks</h2>
<p>Functions can make it easier to deal with discontinuous events. For example, suppose there is a sequence that begins with a user interaction, making a request of the server, and finally displaying the server's response. The naïve way to write that would be: </p>
<p>request = prepare_the_request(  );<br />
response = send_request_synchronously(request);<br />
display(response); </p>
<p>The problem with this approach is that a synchronous request over the network will leave the client in a frozen state. If either the network or the server is slow, the degradation in responsiveness will be unacceptable. A better approach is to make an asynchronous request, providing a callback function that will be invoked when the server's response is received. An asynchronous function returns immediately, so the client isn't blocked: </p>
<pre>
request = prepare_the_request(  ); 
send_request_asynchronously(request, function (response) {     
  display(response);     
});
</pre>
<p>We pass a function parameter to the send_request_asynchronously function that will be called when the response is available.
</p></blockquote>
<p><i>example of callback, hitting the twitter search api</i><br />
And for kicks I put together a simple code sample that exercises callbacks by hitting the twitter api (the <a href="https://github.com/victusfate/callback_twitter_sample">git repo for callback_twitter_sample</a>):<br />
<script src="https://gist.github.com/802225.js?file=twitter%20callback%20api%20sample"></script><br />
Here's the <a href="http://victusfate.github.com/callback_twitter_sample/">app live</a>, feel free to play with it, fork it etc.<br />
[iframe http://victusfate.github.com/callback_twitter_sample/ 500 500]</p>
<p>Related urls:</p>
<ul>
<li><a href="http://stackoverflow.com/questions/tagged/chaining">function chaining at stackoverflow</a></li>
<li><a href="http://en.wikipedia.org/wiki/Callback_(computer_programming)">Callbacks defined</a></li>
<li><a href="http://docs.jquery.com/How_jQuery_Works">How jQuery Works</a></li>
</ul>
