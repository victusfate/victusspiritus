---
layout: post
status: publish
published: true
title: Practical First Rails Threading Example
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2654
wordpress_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/01/01/practical-first-rails-threading-example/
date: '2010-01-01 09:59:53 -0500'
date_gmt: '2010-01-01 16:59:53 -0500'
categories:
- Uncategorized
tags:
- ruby
comments:
- id: 2728
  author: Ensure All Roads Lead to Your Goal (+ Ruby Threads) &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2009/12/31/ensure-all-roads-lead-to-your-goal-ruby-threads/
  date: '2010-01-24 11:39:55 -0500'
  date_gmt: '2010-01-24 18:39:55 -0500'
  content: "[...] friendfeed        Stylized Information will be the Sole Survivor
    Practical First Rails Threading Example [...]"
- id: 9542
  author: Brushing up on Computer Science Part 5, Graphs, Networks, and Operating
    Systems &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/
  date: '2011-03-18 09:16:05 -0400'
  date_gmt: '2011-03-18 16:16:05 -0400'
  content: "[...] I discussed an implementation of green threads in ruby over a couple
    of posts last year (1, 2), and it saved us some time waiting on remote api calls.
    It&#8217;s worth noting that the Ruby MRI [...]"
---
<h2>Getting a Handle On Threads</h2>
<p>Yesterday I wrote briefly about <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/12/31/ensure-all-roads-lead-to-your-goal-ruby-threads/">threading in Ruby</a>. Ruby threads don't natively take advantage of multiple processors or cores (this may have changed), but they're a great way to lower wait time on concurrent external delays. This is a non-blocking solution to initiating several API calls simultaneously, and greatly reduces delay, an imperative requirement to web services.</p>
<h2>Threading Mulitple Model Calls</h2>
<p>On initial creation or update, our User model makes API calls to Twitter, as well as several calls to Zemanta markup and Alchemy Orchestr8. We have shifted from a rapid fire status merged keyword extraction using Orchestr8, to a more object specific, rich semantic entity approach per user status. Once the Twitter streaming API fully opens up we can automatically update known user profiles as well as their associated lists and this will diminish the necessity of rapid response. As we grow, we expect many users to be first time visitors, and we are doing our best to make sure load and processing times are minimal.</p>
<h2>Threads in the Controller Were No Go</h2>
<p>The next level of threading was for each user of a list. We didn't want to bottleneck response based on well populated user lists, so it was natural to attempt threading for User construction. The Rails controller gave us some issues, and after some reading we discovered that threading and Rails was discouraged in favor of background processes. I moved the calls into the User update keywords method and forced the collapse of threads after they all had been initiated (loop over creation, then loop over joining). Eureka! It loaded list pages much faster but there may be a more desirable solution. We had to be careful with timing the database writes to avoid concurrent calls (still learning about limitations).</p>
<h2>Threaded User Construction Is Modular, But List API Gets Everything at Once</h2>
<p>An alternative to threaded User creation is to treat lists as a new user. The Twitter API may yield a similar batch data grab, updating all statuses and semantic extraction for them would be identical to single User updates. The tradeoff is that we would lose the connection and history of who an entity came from (something that I'd like to leverage in serendipitous social discovery).</p>
<p>I'd love to hear how others are considering threading with web development and waiting on API calls. Please leave any pro tips in the comment section.</p>
<p>You can email me for code snippets (on my phone at the moment). My email is messel at victusmedia dot com.</p>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://www.killerstartups.com/Web-App-Tools/api-status-com-checking-uptime-downtime-right-away">API-Status.com - Checking Uptime &amp; Downtime Right Away</a> (killerstartups.com)</li>
<li class="zemanta-article-ul-li"><a href="http://techhotspot.com/2009/09/16/a-tiny-thread/">A Tiny Thread</a> (techhotspot.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.slideshare.net/thepropsman/erlounge-sfbay-20100112-christian-westbrook-cotweet">ErLounge SF/Bay: 2010.01.12 Christian Westbrook / CoTweet</a> (slideshare.net)</li>
<li class="zemanta-article-ul-li"><a href="http://avdi.org/devblog/2009/10/27/nulldb-for-datamapper/">NullDB for DataMapper</a> (avdi.org)</li>
</ul>

