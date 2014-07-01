---
layout: post
status: publish
published: true
title: Ensure All Roads Lead to Your Goal (+ Ruby Threads)
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2649
wordpress_url: http://www.victusspiritus.com/?p=2649
date: '2009-12-31 06:11:09 -0500'
date_gmt: '2009-12-31 13:11:09 -0500'
categories:
- Uncategorized
tags:
- inspiration
- coding
- ruby
- design
comments:
- id: 2403
  author: DaveinHackensack
  author_email: impossibledistances@yahoo.com
  author_url: http://www.thehackensack.blogspot.com/
  date: '2009-12-31 14:13:30 -0500'
  date_gmt: '2009-12-31 19:13:30 -0500'
  content: It&#39;s funny how you focus on the beautiful gardens instead of the impossible
    distances. You&#39;re a true optimist, which is a good thing. Beats the alternative.
    <br><br>I don&#39;t think Crane was much of an optimist, but his poetry is enriched
    by his world-weariness. Here&#39;s a great poem of his to keep in mind next time
    you get drawn into an argument on the Internet:<br><br><I>I saw a man pursuing
    the horizon;<br>Round and round they sped.<br>I was disturbed at this;<br>I accosted
    the man.<br>"It is futile," I said,<br>"You can never -"<br><br>"You lie," he
    cried,<br>And ran on.</I>
- id: 2404
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2009-12-31 14:52:40 -0500'
  date_gmt: '2009-12-31 19:52:40 -0500'
  content: You have me pegged, I had utterly missed the impossible distance as just
    a minor inconvenience. The garden draws out my best so that is what I focus on.
    I&#39;m fully capable of believing the worst of people and situations, but I find
    that myself and the world benefits more from seeing the best in others. It&#39;s
    so easy to forget all that we accomplish, and all the good we do because cognitively
    we hardwired to remember the negative more clearly.
- id: 2412
  author: DaveinHackensack
  author_email: impossibledistances@yahoo.com
  author_url: http://www.thehackensack.blogspot.com/
  date: '2009-12-31 17:41:04 -0500'
  date_gmt: '2009-12-31 22:41:04 -0500'
  content: I&#39;ll leave you with a more positive Stephen Crane poem, which I think
    you might like:<br><br><I>There was a man with tongue of wood<br>Who essayed to
    sing,<br>And in truth it was lamentable.<br>But there was one who heard<br>The
    clip-clapper of this tongue of wood<br>And knew what the man<br>Wished to sing,<br>And
    with that the singer was content.</I>
- id: 2727
  author: Practical First Rails Threading Example &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/01/01/practical-first-rails-threading-example/
  date: '2010-01-24 11:38:47 -0500'
  date_gmt: '2010-01-24 18:38:47 -0500'
  content: "[...]        Ensure All Roads Lead to Your Goal (+ Ruby Threads) Candy
    to the Imagination, a Day Trip to [...]"
- id: 9540
  author: Brushing up on Computer Science Part 5, Graphs, Networks, and Operating
    Systems &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/03/17/brushing-up-on-computer-science-part-5-graphs-networks-and-operating-systems/
  date: '2011-03-18 09:15:17 -0400'
  date_gmt: '2011-03-18 16:15:17 -0400'
  content: "[...] expertise. I discussed an implementation of green threads in ruby
    over a couple of posts last year (1, 2), and it saved us some time waiting on
    remote api calls. It&#8217;s worth noting that the Ruby [...]"
---
<p><a href="http://www.stuckincustoms.com/2009/12/27/the-rainy-forest-in-hakone/"><img class="aligncenter size-large wp-image-2648" title="A Rainy Day in Hakone" src="{{ site.url }}/assets/2009/12/Gateway-682x1024.jpg" alt="" width="682" height="1024" /></a></p>
<h2>The Zen Abstract Design Side</h2>
<p>Our world is a function of pre-existing inertia (environment), uncontrollable events, and my personal favorite the malleable future that we craft together. We are challenged daily to pull our sum experiences together to overcome barriers. The greater our ability to collaborate and scale these walls, the further we can go, and the more wonderous our creations. Take stock of your victories, even if they appear to be the product of luck!</p>
<h2>Design Challenge, Calling And Waiting on APIs is too Slow</h2>
<p>Last night while working with Tyler on improving extracted keywords/entities we discovered a design tradeoff. In this case it was speed versus quality. We focused on the delays of superior quality entity returns and it occurred to me we could spawn many threads to simultaneously call the processing API to relieve sequential user wait time. Neither of us has done multithreaded Ruby coding before so it was new ground. Background processing of information is our main approach but the Twitter streaming API isn't fully open, and since we are focused on growth we expect many new users (for which we won't have preprocessed results).</p>
<p>Ruby just happens to make threading incredibly simple to implement:<br />
threadID = Thread.new {<br />
*threadcode*<br />
}<br />
...<br />
threadID.join()</p>
<p>Literally. in a manner of seconds we had sped up a series of API calls to a single batch call (N x user calls was now the slowest of all the calls, a speedup up of potentially hundreds of seconds for large lists of new users). The only detail is when to rejoin the threads. Naturally collapsing the calls will happen before visualizing their outputs. Additional care must be taken for memory writing and storing their returns in a structure. Threads allow local storage to keep API returns, and we need to ensure that we don't create a thread for the same user more than once (should have that working this afternoon). The coding experience has been phenomenal compared to threading in C++ (a bit trickier), so kudos to Ruby language designers. Many modern languges keep the simplicity of concurrency at the top of their priority list (even C++ is including simpler handling in the new standard).</p>
<h2>Now Back to Zen thanks to Dave</h2>
<p>I'll leave off with a powerful poem passed along by my <a href="http://thehackensack.blogspot.com/">"cynicism guru" Daveinhackensack</a> (Dave believes the scarcity of optimism boosts its value ;)).<br />
"It comes from this poem by the great New Jersey man of letters Stephen Crane"</p>
<blockquote><p>There was set before me a mighty hill,<br />
And long days I climbed<br />
Through regions of snow.<br />
When I had before me the summit-view,<br />
It seemed that my labour<br />
Had been to see gardens<br />
Lying at impossible distances.</p></blockquote>
<p>May all paths lead to beautiful gardens.</p>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/01/01/practical-first-rails-threading-example/">Practical First Rails Threading Example</a> (victusspiritus.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.zemanta.com/blog/2010-a-fresh-new-start-2/">2010: a fresh new start</a> (zemanta.com)</li>
<li class="zemanta-article-ul-li"><a href="http://blog.revolution-computing.com/2010/01/analyzing-a-friendfeed-group-with-ruby-and-r.html">Analyzing a FriendFeed group with Ruby and R</a> (revolution-computing.com)</li>
<li class="zemanta-article-ul-li"><a href="http://nandz.blogspot.com/2008/04/ruby-few-points-about-ruby-threading.html">[Ruby] A few points about Ruby threading...</a> (nandz.blogspot.com)</li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Reblog this post [with Zemanta]" href="http://reblog.zemanta.com/zemified/6266fa4d-0098-47ab-a1cc-fe7e3a98f972/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/reblog_e.png?x-id=6266fa4d-0098-47ab-a1cc-fe7e3a98f972" alt="Reblog this post [with Zemanta]" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
