---
layout: post
status: publish
published: true
title: The Four Horsemen of Rails 3.1beta, Coffee-Script, jQuery, SCSS and Assets
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8772
wordpress_url: http://www.victusspiritus.com/?p=8772
date: '2011-05-11 04:49:42 -0400'
date_gmt: '2011-05-11 11:49:42 -0400'
categories:
- Uncategorized
tags:
- coding
- javascript
- ruby
- jquery
- coffeescript
- rails
comments:
- id: 9954
  author: Twitter&#8217;s List and Search APIs leave much to be desired &mdash; Victus
    Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/05/13/twitters-list-and-search-apis-leave-much-to-be-desired/
  date: '2011-05-13 07:58:21 -0400'
  date_gmt: '2011-05-13 14:58:21 -0400'
  content: "[...] an entity visualization layer on top of Twitter streams. I was able
    to get the 3.1beta Rails app (lots of great changes coming) working locally without
    much trouble. But it&#8217;s the first Heroku app I&#8217;ve migrated from [...]"
- id: 9988
  author: Imagebrowser Rails app ported from 2.3.4 to 3.1beta &mdash; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/05/18/imagebrowser-rails-app-ported-from-2-3-4-to-3-1beta/
  date: '2011-05-18 15:33:40 -0400'
  date_gmt: '2011-05-18 22:33:40 -0400'
  content: "[...] I found some time last night and this morning to finish migrating
    an app Tyler and I worked on 2009, and that I spent time on refining in 2010.
    I moved the application from ruby 1.8.7 and rails 2.3.4 to MRI 1.9.2 and rails
    3.1beta. I&#8217;ve discussed some of the changes to rails here in the past week.
    [...]"
- id: 10033
  author: Jae
  author_email: keolo@dreampointmedia.com
  author_url: ''
  date: '2011-05-23 23:55:00 -0400'
  date_gmt: '2011-05-23 23:55:00 -0400'
  content: |-
    What's the best way to share code between coffeescript files? 

    E.g. if I want to call a function defined in application.js.coffee from anotherfile.js.coffee.

    CoffeeScript wraps code from each file in (function() {}).call(this); to avoid namespacing conflicts.
- id: 10034
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-23 23:59:00 -0400'
  date_gmt: '2011-05-23 23:59:00 -0400'
  content: "I think you can include one file in another. \r\n\r\ninclude \"utils\""
- id: 10035
  author: Jae
  author_email: keolo@dreampointmedia.com
  author_url: ''
  date: '2011-05-24 01:45:00 -0400'
  date_gmt: '2011-05-24 01:45:00 -0400'
  content: |-
    Yeah. The file is included ... I think it's more of a design question. Here's what I found that works:

    https://gist.github.com/988010
- id: 10038
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-24 09:01:00 -0400'
  date_gmt: '2011-05-24 09:01:00 -0400'
  content: |-
    Gotcha. So you order the inclusion of script files in the assets file.

    Does the require only work when using CoffeeScript with node.js/Rhino/ other js servers? I thought that would be a great way to include coffeescript libraries.
---
<h1>A brief description of CoffeeScript, jQuery, SCSS and Assets</h1>
<p><a href="http://www.victusspiritus.com/2011/05/06/wakeup-with-a-fresh-cup-of-coffeescript/">CoffeeScript</a> is a translation and JavaScript with additional features to ease development, code readability, and functionality. It has all the best features of JavaScript as it IS JavaScript, but adds on essential development perks like terse syntax, local variable scoping, and utilities.</p>
<p>jQuery is a wonderful JavaScript development library which works smoothly with or without CoffeeScript. For my personal development usage, jQuery gives me a consistent selector and reliable cross browser interface functionality. It's a great resource for any JavaScript work.</p>
<p>SCSS files, or <a href="http://sass-lang.com/">SASS</a> is a dynamic version of CSS with variables and mixins (blocks or structures). This is one of features that you say, oh yeah why'd it take the web language folks so long to get this right. Although I haven't had a chance to use this feature yet, I look forward to doing so. Say good bye to cut and paste errors cropping up in your style code.<br />
<script src="https://gist.github.com/975057.js"> </script></p>
<p>Assets is the new directory for your projects javascript, css and images. Resource optimization is accomplished with <a href="http://getsprockets.org/">Sprockets</a>. Sprockets merges resources such as javascript and css into a single compressed location for rapid delivery to clients.</p>
<h1>An example</h1>
<p>While converting an older rails 2.3.4 app to 3.0 I crashed and burned while changing one file at a time over within the project. Needless to say that was a flawed strategy, but I did learn a little along the way. I ended up skipping 3.0 and moving to 3.1beta1 with a fresh app, and copied my app and public folders in after getting the migrations right. That move had a couple of outstanding issues, the most important being that I didn't use rails edge for creating the new app (thanks for the tip <a href="http://www.rubyinside.com/how-to-rails-3-1-coffeescript-howto-4695.html">RubyInside</a>). </p>
<p>First snag the latest rails into an easy to reference location:</p>
<pre>
cd ~/goodtimes

git clone https://github.com/rails/rails.git
</pre>
<p>My path includes a ~/Desktop/Dropbox/ so my code is available everywhere.</p>
<p>Then refer to that rails exec for building a new app:</p>
<pre>
~/goodtimes/rails/bin/rails new bacon --edge
</pre>
<p>Assuming your rails repo is in goodtimes and your new app is called bacon.</p>
<p>Then I followed parts of this gist tutorial (thanks <a href="https://github.com/eric1234">@eric1234</a> and <a href="https://github.com/sgruhier">@sgruhier</a> for putting it together), shared pain is shared gain.</p>
<p><script src="https://gist.github.com/965761.js"> </script></p>
<p>Finally this morning I created a git repo and pulled in my old project, then resolved all the merge conflicts. There are likely some sneaky issues left over, as auto merge may have done terrible things with configuration. My last error was a stale cookie, no one eats those.</p>
<p>I'll repeat the process and/or diff one directory at a time if I can't figure it out quickly. So far I've created a few locally functioning rails 3.1beta apps, but ran into problems when deploying the migrated medium complexity app to Heroku, even with theRubyRacer gem. </p>
<p>The likely problem is hosed configuration settings. The database and new change migrations appear ok, along with the moved JavaScript and CSS into assets (auto merge magic) along with a new square root slinging CoffeeScript ;).</p>
<p>More to come...</p>
<p>Related posts:</p>
<ul>
<li>The <a href="http://weblog.rubyonrails.org/2011/5/5/rails-3-1-beta-1-released">official announcement</a> from the Rails team about 3.1 beta.</li>
<li>Great guidance from <a href="http://www.rubyinside.com/how-to-rails-3-1-coffeescript-howto-4695.html">RubyInside</a> on how to get started</li>
</ul>
<p><script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.5.1/jquery.min.js"></script><br />
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.10/jquery-ui.min.js"></script><br />
<script type="text/javascript"<br />
src="https://gist.github.com/raw/949945/1468755b2659aa0206ef4b0060100b152f44a8d3/growingdivs.js"></script></p>
