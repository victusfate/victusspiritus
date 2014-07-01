---
layout: post
status: publish
published: true
title: Rails 3.1beta deployed to Heroku from your iPhone
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8927
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/05/17/rails-3-1beta-deployed-to-heroku-from-your-iphone/
date: '2011-05-17 06:24:12 -0400'
date_gmt: '2011-05-17 13:24:12 -0400'
categories:
- Uncategorized
tags:
- web/tech
- coding
- ruby
comments:
- id: 9985
  author: Imagebrowser Rails app ported from 2.3.4 to 3.1beta &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/05/18/imagebrowser-rails-app-ported-from-2-3-4-to-3-1beta/
  date: '2011-05-18 06:57:32 -0400'
  date_gmt: '2011-05-18 13:57:32 -0400'
  content: "[...] and rails 2.3.4 to MRI 1.9.2 and rails 3.1beta. I&#8217;ve discussed
    some of the changes to rails here in the past [...]"
- id: 9997
  author: neXter
  author_email: ''
  author_url: http://twitter.com/neXter
  date: '2011-05-20 08:56:00 -0400'
  date_gmt: '2011-05-20 08:56:00 -0400'
  content: Try using Prompt by Panic as SSH App for iOS (http://www.panic.com/blog/2011/04/introducing-prompt-ssh-for-ios/)
    nice and smooth
- id: 9998
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-20 09:16:00 -0400'
  date_gmt: '2011-05-20 09:16:00 -0400'
  content: Thanks, grabbed it.
---
<h1>The tools:</h1>
<ol>
<li>Local shell, LogMeIn or an ssh shell to a terminal system on your phone/tablet</li>
<li>a system with git and heroku <strong>(I haven't tried installing these on my phone)</strong></li>
<li>Internet</li>
<li>DropBox and DropText for easy mobile editing. Alternatively you could use github as a web editing/auto-commiting platform</li>
</ol>
<h1>The commands</h1>
<p>Begin in your DropBox project hidey hole directory.</p>
<h2>Part 1</h2>
<p><script src="https://gist.github.com/976382.js"> </script></p>
<h2>Intermission, theRubyRacer</h2>
<p>For Heroku we'll need to add pg and theRubyRacer gem. We only need them for production (can use conditional requires), but this  will work. </p>
<p><script src="https://gist.github.com/976408.js"> </script></p>
<h2>Part 2</h2>
<p><script src="https://gist.github.com/976391.js"> </script></p>
<p>That's it, the app is live at. You can see it here: <a href="http://phoneHome.heroku.com/links">http://phoneHome.heroku.com/links</a>.</p>
<p><b>Lessons learned:</b></p>
<ul>
<li>LogMeIn over Simons mall wifi is painful. Stopping at the Apple store helped figure out some issues (I forgot rubyracer initially).</li>
<li>DropText helped edit files. Remember to add editable file types with no extension like Gemfile.</li>
<li>iPhones can deploy web servers. But it's still far from ideal. I could use a wonderful shell app for ssh terminaling home. I should be able to find one without too much trouble.</li>
</ul>
<p><script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.5.1/jquery.min.js"></script><br />
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.10/jquery-ui.min.js"></script><br />
<script type="text/javascript"<br />
src="https://gist.github.com/raw/949945/1468755b2659aa0206ef4b0060100b152f44a8d3/growingdivs.js"></script></p>
