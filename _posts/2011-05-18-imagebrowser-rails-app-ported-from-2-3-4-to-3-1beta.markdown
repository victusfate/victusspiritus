---
layout: post
status: publish
published: true
title: Imagebrowser Rails app ported from 2.3.4 to 3.1beta
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8928
wordpress_url: http://www.victusspiritus.com/?p=8928
date: '2011-05-18 06:56:27 -0400'
date_gmt: '2011-05-18 13:56:27 -0400'
categories:
- Uncategorized
tags:
- coding
- ruby
- rails
comments:
- id: 10036
  author: Leland
  author_email: leland@pickple.com
  author_url: ''
  date: '2011-05-24 04:58:00 -0400'
  date_gmt: '2011-05-24 04:58:00 -0400'
  content: |-
    Man you weren't kidding about taking long to pass/receive that data! I spent about 2 minutes waiting for everything to come in (though that might be on my end). :)

    The idea is pretty cool though. Not something I would use, but perhaps someone who has to process a lot of messages and skim through things quickly would get a lot of use out of it.
- id: 10037
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-05-24 08:48:00 -0400'
  date_gmt: '2011-05-24 08:48:00 -0400'
  content: ":)\r\n\r\nUgh, it should load in 3-4 seconds. I'll need to parse language
    locally to speed it up. Twitter's API is usually pretty fast, and so is Google
    images (&lt; 500msec). The time killer is text blob to semantic entity api&#039;s
    and process time."
---
<p><a href="http://imagebrowser.heroku.com/"><img src="http://www.victusspiritus.com/wp-content/uploads/2011/05/imagebrowser_rails3-1024x797.png" alt="" title="imagebrowser_rails3" width="630" height="490" class="aligncenter size-large wp-image-8929" /></a></p>
<p>The Intelligent Media Manager is once again live at <a href="http://imagebrowser.heroku.com">imagebrowser.heroku.com</a>! It still takes a little too long to pass and receive data from remote semantic APIs. One change I'd like to make is a local entity (people, place, thing) identifier in text streams.</p>
<p>I found some time last night and this morning to finish migrating an app Tyler and I worked on 2009, and that I spent time on refining in 2010. I moved the application from ruby 1.8.7 and rails 2.3.4 to MRI 1.9.2 and rails 3.1beta. I've discussed some of the changes to rails <a href="http://www.victusspiritus.com/2011/05/17/rails-3-1beta-deployed-to-heroku-from-your-iphone/">here</a> in the past <a href="http://www.victusspiritus.com/2011/05/11/the-four-horsemen-of-rails-3-1beta-coffee-script-jquery-scss-and-assets/">week</a>. </p>
<p>Heroku makes it fairly straight forward to migrate stacks for deployment, but be careful not to migrate to the same stack. I did that and had to destroy the app and recreate it (not a big deal) as it was no longer receiving git pushes.</p>
<p>The final error I was having was in CSS. Simply put I didn't have valid style sheets and Sprockets was choking on it. In the past forgiving browsers would conceal the errors. Luckily a quick CSS validation call from TextMate pointed out the mistakes and it's been smooth sailing ever since.</p>
