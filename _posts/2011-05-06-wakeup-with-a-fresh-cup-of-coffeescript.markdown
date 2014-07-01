---
layout: post
status: publish
published: true
title: Wakeup with a fresh cup of CoffeeScript
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8743
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/05/06/wakeup-with-a-fresh-cup-of-coffeescript/
date: '2011-05-06 05:51:55 -0400'
date_gmt: '2011-05-06 12:51:55 -0400'
categories:
- Uncategorized
tags:
- coding
- javascript
- node.js
- coffeescript
comments:
- id: 9933
  author: Essay writing
  author_email: alexstevens78@yahoo.com
  author_url: http://anyessays.com/
  date: '2011-05-07 11:33:00 -0400'
  date_gmt: '2011-05-07 11:33:00 -0400'
  content: |
    I was searching this a long time! Thank you very much for  detail descripton! It's very useful information for me!
- id: 9974
  author: The Four Horsemen of Rails 3.1beta, Coffee-Script, jQuery, SCSS and Assets
    &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/05/11/the-four-horsemen-of-rails-3-1beta-coffee-script-jquery-scss-and-assets/
  date: '2011-05-16 11:53:53 -0400'
  date_gmt: '2011-05-16 18:53:53 -0400'
  content: "[...] CoffeeScript is a translation and JavaScript with additional features
    to ease development, code readability, and functionality. It has all the best
    features of JavaScript as it IS JavaScript, but adds on essential development
    perks like terse syntax, local variable scoping, and utilities. [...]"
---
<p>I like programming languages with rich object models. I <strong>love</strong> dynamic languages. Sure, minimizing execution time and resource optimization may demand speed, and c variants and java (mirah!) are screamers. Yet after having coded heavily in one of these languages for years, it's a breath of fresh air letting go of the training wheels of type safety and discarding the mental overhead of complex inheritance trees. Verbosity be damned!</p>
<blockquote><p>
An object <strong>is</strong> the interface it <strong>defines</strong>.
</p></blockquote>
<p>Ruby, Python and Javascript have all sparked my imagination as incredibly flexible dynamic languages. They've also inspired a generation of delightful framework and tool builders. But while learning their syntax, object models, and functional features, it bugged me that JavaScript missed out on some of the syntactical sugar of its dynamic kin. </p>
<p>It bothered another gentleman far more, and from his frustration was born a language of beauty. <a href="https://github.com/jashkenas">Jeremy Ashkenas</a> crafted and continues to improve <a href="http://jashkenas.github.com/coffee-script/">CoffeeScript</a>, which is actually a transliteration of JavaScript (to which it cleanly compiles) combined with a utility library. I'm having a great time learning the language with <a href="http://pragprog.com/titles/tbcoffee/coffeescript">Trevor Burnham's CoffeeScript</a> book, published by the Pragmatic Bookshelf.</p>
<blockquote><p>
<strong>CoffeeScript</strong></p>
<pre>
square = (x) -> x * x

math =
  root:   Math.sqrt
  square: square
  cube:   (x) -> x * square x

list = [1, 2, 3, 4, 5]

cubes = (math.cube num for num in list)
</pre>
<p>and the equivalent <strong>JavaScript</strong>:</p>
<pre>
var cubes, list, math, num, square;

square = function(x) {
  return x * x;
};
list = [1, 2, 3, 4, 5];
math = {
  root: Math.sqrt,
  square: square,
  cube: function(x) {
    return x * square(x);
  }
};

cubes = (function() {
  var _i, _len, _results;
  _results = [];
  for (_i = 0, _len = list.length; _i < _len; _i++) {
    num = list[_i];
    _results.push(math.cube(num));
  }
  return _results;
})();
</pre>
<p>Another example: (<a href="http://javascriptatoms.com/2011/05/coffeescript-the-other-javascript/">source</a>)</p>
<pre>
restaurants = [‘Fridays’, ‘Applebees’, ‘Chilis’]
for restaurant in restaurants alert restaurant

//compared to JavaScript

var restaurant, restaurants, _i, _len;
restaurants = [‘Fridays’, ‘Applebees’, ‘Chilis’]
for (_i = 0; _len = restaurants.length; _len < _i; _i++) {
  restaurant = restaurants[_i];
  alert(restaurant);
}
</pre>
</blockquote>
<p>One more example, the Y Combinator in JavaScript and coffeescript (thanks <a href="https://github.com/niko">niko</a>)<br />
<script src="https://gist.github.com/958892.js"> </script></p>
<h1>Installation</h1>
<p>Note that with node.js, nodemon and a configuration file you can have coffee files automatically compiled to JavaScript on save for interpretation. <del>I found nvm a great configuration tool for keeping my versions of node straight</del>I opted to manually install and maintain node versions for the time being. I had issues with where nvm was installing files and some conflicts with npm.</p>
<p>The following installation instructions are from Jashkenas github linked above:</p>
<blockquote><p>
Installation and Usage</p>
<p>The CoffeeScript compiler is itself written in CoffeeScript, using the Jison parser generator. The command-line version of coffee is available as a Node.js utility. The core compiler however, does not depend on Node, and can be run in any JavaScript environment, or in the browser (see “Try CoffeeScript”, above).</p>
<p>To install, first make sure you have a working copy of the latest stable version of Node.js, and npm (the Node Package Manager). You can then install CoffeeScript with npm:</p>
<p>npm install -g coffee-script<br />
(Leave off the -g if you don’t wish to install globally.)</p>
<p>If you’d prefer to install the latest master version of CoffeeScript, you can clone the CoffeeScript source repository from GitHub, or download the source directly. To install the CoffeeScript compiler system-wide under /usr/local, open the directory and run:</p>
<p>sudo bin/cake install<br />
If installing on Ubuntu or Debian, be careful not to use the existing out-of-date package. If installing on Windows, your best bet is probably to run Node.js under Cygwin.</p>
<p>Once installed, you should have access to the coffee command, which can execute scripts, compile .coffee files into .js, and provide an interactive REPL.
</p></blockquote>
<p>Notes:</p>
<ul>
<li>For a great example of CoffeeScript in action, check out <a href="http://zombie.labnotes.org/">Zombie.js</a>. There are already far too many wonderful coffeescript examples for me to cite, it's an extraordinarily fast growing language translation.</li>
<li>News at <a href="http://news.ycombinator.com/item?id=2503411">YCombinator conversation about CoffeeScript's latest release</a></li>
</ul>
<p><script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.5.1/jquery.min.js"></script><br />
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.10/jquery-ui.min.js"></script><br />
<script type="text/javascript"<br />
src="https://gist.github.com/raw/949945/1468755b2659aa0206ef4b0060100b152f44a8d3/growingdivs.js"></script></p>
