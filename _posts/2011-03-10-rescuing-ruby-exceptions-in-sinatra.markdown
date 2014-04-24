---
layout: post
status: publish
published: true
title: Rescuing Ruby Exceptions in Sinatra
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7613
wordpress_url: http://www.victusspiritus.com/?p=7613
date: '2011-03-10 09:48:42 -0500'
date_gmt: '2011-03-10 16:48:42 -0500'
categories:
- Uncategorized
tags:
- web/tech
- coding
- ruby
comments: []
---
<p>This morning granted me 25 minutes to debug an Oauth callback in AutoSub, my latest list subscription juggling tool. While an older spawn of Victus Media <a href="http://imagebrowser.heroku.com">ImageBrowser</a> does a fine job of doing the Oauth handshake in Rails, there were a couple of subtle differences in the implementation.</p>
<p>If memory serves the exception handling in our Rails callback is:</p>
<pre>
def callback
 begin
   *magic code*
 rescue
   render_to :text => !1
 end
end
</pre>
<p>If an exception is raised it's rendered as text and sent to the browser.</p>
<p>Here's the Sinatra variant I'm working with:</p>
<pre>
def callback
 begin
   *magic code*
 rescue
   #do something depending on env['sinatra.error']
 end
end
</pre>
<p>Here I'm passing the environment variable from Rack back to the browser.</p>
<p>Not much of a difference right? But getting a meaningful error message is priceless when trying to understand what's going wrong. Although I'm handling the callback route in AutoSub.rb, and the params are loaded properly from the callback url, there's an issue with one of the method calls I'm making. I should have a few moments this afternoon to clear it up.</p>
<p><b>update</b> I removed the rescue and allowed the app to raise an error and render the results automatically.</p>
<pre>
def callback
   *magic code*
end
</pre>
<p>Looks like I'm running into a token usage error.</p>
