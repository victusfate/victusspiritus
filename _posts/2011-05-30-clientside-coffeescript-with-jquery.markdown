---
layout: post
status: publish
published: true
title: Clientside CoffeeScript with jQuery
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9107
wordpress_url: http://www.victusspiritus.com/?p=9107
date: '2011-05-30 09:34:19 -0400'
date_gmt: '2011-05-30 16:34:19 -0400'
categories:
- Uncategorized
tags:
- coding
- javascript
- node.js
- coffeescript
comments:
- id: 10070
  author: Justin Forder
  author_email: justin.forder@gmail.com
  author_url: http://profiles.google.com/justin.forder
  date: '2011-06-01 02:16:00 -0400'
  date_gmt: '2011-06-01 02:16:00 -0400'
  content: |-
    Where you have:

        temp = inv; inv = msg; msg = temp

    you might find it clearer to write:

        [inv, msg] = [msg, inv]

    See the section on "Destructuring Assignment" in the reference at http://jashkenas.github.com/coffee-script/
- id: 10072
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-06-01 09:15:00 -0400'
  date_gmt: '2011-06-01 09:15:00 -0400'
  content: Thanks for the swap tip :). I was going to declare a higher scope tmp but
    didn't get around to it.
- id: 10073
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-06-01 09:15:00 -0400'
  date_gmt: '2011-06-01 09:15:00 -0400'
  content: Thanks for the swap tip :). I was going to declare a higher scope tmp but
    didn't get around to it.
- id: 10176
  author: Fishing for help using Client Side CoffeeScript with .coffee files &mdash;
    Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/06/23/fishing-for-help-using-client-side-coffeescript-with-coffee-files/
  date: '2011-06-23 05:01:45 -0400'
  date_gmt: '2011-06-23 12:01:45 -0400'
  content: "[...] Client side intro [...]"
- id: 10189
  author: Visualization layered like music tracks &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/06/25/visualization-layered-like-music-tracks/
  date: '2011-06-26 01:57:50 -0400'
  date_gmt: '2011-06-26 08:57:50 -0400'
  content: "[...] side CoffeeScript in Henri Bergius&#8217; gist (bottom of post)
    on the Falsy Values node.js tutorials is a strong contender, but requires a couple
    of additional [...]"
- id: 10222
  author: The secret art of the tutorial &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/07/05/the-secret-art-of-the-tutorial/
  date: '2011-07-05 10:19:47 -0400'
  date_gmt: '2011-07-05 17:19:47 -0400'
  content: "[...] is my early experience with CoffeeScript. I&#8217;ve found it much
    easier to dive in with client side CoffeeScript examples which require only a
    browser and Jeremy Ashkenas&#8217; JavaScript [...]"
---
<p>Before digging into node.js servers with CoffeeScript, I branched off by mimicking a <a href="http://geekiriki.blogspot.com/2010/08/jquery-meets-coffeescript.html">simple client example</a> by Arbo von Monkiewitsch.<br />
[iframe http://victusfate.github.com/client_side_coffeescript/ 650 1000]<br />
It attaches a callback function to a click event and updates the page. Note that I haven't passed in an object by reference (return changes), otherwise I could have called a swap function, from within the show message function.</p>
<p>Feel free to browse my <a href="http://www.victusspiritus.com/tag/coffeescript/">coffeescript tag</a> for more clientside hacks. </p>
<p>After this simple client side example I've got a plateful of fun ahead of me thanks to <a href="https://gist.github.com/978411">Henri Bergius' gist</a> capturing node.js exercises from Up and Running with Node.js at the Falsy Values workshop (via the <a href="http://www.tumblr.com/tagged/coffeescript">Tumblr CoffeeScript tag</a> and <a href="http://www.readwriteweb.com/hack/2011/05/coffeescript-nodejs-exercises.php">ReadWriteWeb post</a> by Klint Finley).</p>
<p>[iframe https://gist.github.com/999117 650 2000]</p>
