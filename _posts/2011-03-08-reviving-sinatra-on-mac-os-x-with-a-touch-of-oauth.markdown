---
layout: post
status: publish
published: true
title: Reviving Sinatra on Mac OS X with a touch of Oauth
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 7571
wordpress_url: http://www.victusspiritus.com/?p=7571
date: '2011-03-08 05:33:51 -0500'
date_gmt: '2011-03-08 12:33:51 -0500'
categories:
- Uncategorized
tags:
- coding
- ruby
comments: []
---
<p style="text-align: center;"><a href="http://www.sinatrarb.com/"><img class="aligncenter size-full wp-image-7577" title="sinatrarb" src="{{ site.url }}/assets/2011/03/sinatrarb.jpg" alt="" width="522" height="340" /></a></p>
<p>I had time this weekend to kick around with a couple of <a href="http://www.sinatrarb.com/">Sinatra</a> apps. First my <a href="http://rvm.beginrescueend.com/">rvm</a> setup conked out so I reinstalled it from scratch, where the implode feature came in handy. After squaring away my ruby versions and a host of basic gems, my dev environment on the Mac required the do_postgres gem to happily bundle the Sinatra app I was working on*. After some doc reading this weekend I discovered how to point gem installs in the right direction for native dependencies.<br />
<code><br />
PATH=$PATH:/Library/PostgresSQL/bin sudo gem install do_postgres<br />
</code><br />
Whala! The gem installed without a hitch and my Sinatra app kicked to life.</p>
<p>The next trick was doing the Oauth dance. It's been many moons since I last looked at oauth but after browsing other functioning code, the cobwebs cleared and more importantly the <a href="http://oauth.rubyforge.org/">oauth gem site</a> reminded me of the handshake process.</p>
<blockquote><p>Create a new consumer instance by passing it a configuration hash:</p>
<pre>@consumer=OAuth::Consumer.new( "key","secret", {
    :site=&gt;"https://agree2"
    })
</pre>
<p>Start the process by requesting a token</p>
<pre>@request_token=@consumer.get_request_token
session[:request_token]=@request_token
redirect_to @request_token.authorize_url
</pre>
<p>When user returns create an access_token</p>
<pre>@access_token=@request_token.get_access_token
@photos=@access_token.get('/photos.xml')
</pre>
</blockquote>
<p>My particular syntax looks a little different, and that could explain why I had an issue early this morning with getting it working. Instead of an instance variable I store the request_token in a session (which has to be enabled in sinatra, ie enable :session), but this is working fine. In the callback I create an access_token by passing in the oauth_verifier to get_access_token</p>
<pre>request_token = session[:request_token]
@access_token= request_token.get_access_token({:oauth_verifier =&gt; params[:oauth_verifier]})
</pre>
<p>I'll have to revisit my implementation later, as the complaint I'm getting is 1 of 2 expected arguments.</p>
<p>On a side note, there's a new <a href="https://github.com/intridea/omniauth">omniauth gem</a> out for grabs (<a href="https://github.com/intridea/omniauth/wiki">wiki</a>), and oauth2 looks well designed for usage on the dev side.</p>
<p>Notes:<br />
* = the app is a spring cleaning list/follow management tool for twitter.</p>
<p>Related links:</p>
<ul>
<li>Perfect implementation example: <a href="https://github.com/mirven/twitter-oauth-sinatra/blob/master/app.rb">twitter-oauth-sinatra</a></li>
<li><a href="http://oauth.rubyforge.org/">Ruby OAuth gem</a></li>
<li><a href="http://wiki.oauth.net/w/page/25236487/OAuth-2">Oauth2</a></li>
<li><a href="https://github.com/intridea/oauth2">Ruby Oauth2</a></li>
</ul>
