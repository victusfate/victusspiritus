---
layout: post
status: publish
published: true
title: The Prize, Making Sense Out of Millions of Voices
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2783
wordpress_url: http://www.victusspiritus.com/?p=2783
date: '2010-01-21 08:16:45 -0500'
date_gmt: '2010-01-21 15:16:45 -0500'
categories:
- Uncategorized
tags:
- leadership
- inspiration
- social web
- collaboration
- semantic
- victus media
comments:
- id: 2700
  author: David Semeria
  author_email: david@lmframework.com
  author_url: http://lmframework.com/blog/about
  date: '2010-01-21 21:06:37 -0500'
  date_gmt: '2010-01-22 02:06:37 -0500'
  content: Hi Mark, I&#39;m going to spend some more time on <a href="http://victusmedia.com"
    rel="nofollow">victusmedia.com</a> - and you should check out <a href="http://cascaad.com"
    rel="nofollow">http://cascaad.com</a>
- id: 2702
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-01-21 23:04:44 -0500'
  date_gmt: '2010-01-22 04:04:44 -0500'
  content: It&#39;s needing a push update, coming soon from a Chief Tech to you.  (Tyler
    and I have list lockout syndrome)<br>Next update should be a nice one.<br><br>Thanks,
    looks like a very similar social data mining approach-&gt; and they even pull
    in popular links.
---
<p><a href="http://www.voicesofcivilrights.org/"><img class="aligncenter size-full wp-image-2793" title="lv_photo_project" src="{{ site.url }}/assets/2010/01/lv_photo_project.jpg" alt="" width="690" height="218" /></a></p>
<p>Early last year I experienced <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/03/24/infosaurus-robert-scoble-the-scobleizer-redefines-internet-information-flow/">a major breakthrough, my Twitter AHA! moment</a>. While watching tweets stream by and following way too many people, I couldn't really tune into a single user. I witnessed a chorus of voices all sharing their thoughts, ideas and status. Within the net rattle of information, I was able to discover the tech super fan, Robert Scoble.</p>
<p>He was wildly praising <a class="zem_slink" title="Robert Scoble" rel="homepage" href="http://www.friendfeed.com/scobleizer">friendfeed</a> and why he loved it at the time (powerful aggregation + conversations). What impressed me about my first visit to <a href="http://scobleizer.com">his blog</a> was a video he created. It captured how he processes social web information. My first instinct was that I could help him filter all that info even better, but I wasn't sure of the details, it was a gut reaction. The setup Robert was using was a Matrix like interface of displays. He tracked streams of text flowing down the screens, and split his attention among them. There was certainly some Jujutsu on Robert's behalf, leveraging a distinct lack of focus into an advantage for tech news gathering: <em>Purposeful attention deficit chaos</em></p>
<p>I got an image of the pulse of the world going through twitter, although it's social interface only get's a tiny slice of what people are experiencing. Alas, the ubiquitous state sharing machine will have to wait. Although users get the impression of synchronization, what's really happening is more like phone conversations, with small but acceptable delays. A message is placed which quickly gets posted to the site. If you subscribe to that person's updates you receive it in your input stream after a short delay. Wouldn't it be great if you could filter the history of information for things that are relevant to your interests? It turns out you can! More on that later.</p>
<p>At a coarse level, users of any social service can tune into channels which cover topics that are pertinent or relevant to them. While it's a good start, almost everybody I listen to has diverse interests. Even focused information streams may share more than most folks have time to consume. While users are free to create multiple input and output streams, this manual processing step unnaturally breaks up <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/07/12/super-human-filters/">their creative flow</a>. Despite that cost, several information nexi (super nodes) have sliced their streams. For examples explore <a href="http://blog.louisgray.com/">Louis Gray</a>,  <a href="http://scobleizer.com">Robert Scoble</a>, or <a href="http://www.skepticgeek.com/">Mahendra</a> to see how they split their content and curation.</p>
<p>With respect to streams from a single user, I find value in observing various aspects of their personal interests through diverse shares. You can get a feel for how a person thinks, processes, and values information. But there are times when I want to tune into specific topics, and I want that input stream to flow naturally from my reader lists. It got the wheels spinning in my head about information tools to support that form of filtering. <em>Twitter, a massive relational database waiting to happen</em>.</p>
<p>Their's little relevancy and value in knowing in near real-time if the entire world is eating a bagel. There may be in coordinating a world wide eating event (<a href="http://www.everyonelovestea.com/">tea time Tyler?</a>). But businesses benefit by having up to date approximations for how many folks are talking about a certain brand of bagel. Global Bagel Buzz, you heard it here first. The missing piece to provide this type of meta data is user tags (manual) and semantic processing (automated). Knowledge systems like <a href="http://google.com">Google search</a>, <a href="http://hunch.com/">Hunch</a>, and <a href="http://stackoverflow.com/">Stack Overflow</a> all depend on human tagging (or linking) of data. Successful automated tagging of status messages (we're about ~80% correct with <a href="http://imm.victusmedia.com">Intelligent Media Manager or IMM</a>) is a gold mine of value. As Mr. Miagi might say "If done right, no can defend". When implemented the right way, we create the opportunity for fantastic crowd knowledge applications.</p>
<p>I've witnessed live applications that are already creating enormous value. <a href="http://howardlindzon.com/">Howard Lindzon</a> got the ball rolling with <a href="http://stocktwits.com/">Stocktwits</a> where passionate stock traders share info in the Twitter stream by manually tagging stocks with $ as in $MSFT, and tagging their posts with $$. There is growing crowd knowledge in that stream, and filtering techniques correlated with historic stock values should bring light to trader performance (as well as hot/cold stocks). If you enjoy Howard's blog as I do, please leave him a comment suggesting he try out the <a href="http://imm.victusmedia.com">IMM</a>. More on market effects at the end of the post.</p>
<h2>Additional Structure/Metadata We Can Add to Status Now</h2>
<p>There are plenty of opportunities for meta data assignment algorithms, and accurate user self tagging.  At <a href="http://victusmedia.com">Victus Media</a> we have constructed an opt in system for anyone with a Twitter account. We use semantic algorithms from Zemanta and Alchemy's Orchestr8 to discover high confidence tags (machine identified categories). We do regular expression pre/post filtering but still get false positives, as well as many empty returns. Current semantic tools combined with our own curating yields ~70-80% matching tags to user interests.</p>
<p>Public internet communications systems leave a wake of user shared information. A ghost in the machine, serving as a trail of interests leading back to an individual or community. It's time that users begin taking advantage of information that businesses have been leveraging for years (Google Adsense, Gmail,Financial transaction tracking companies, and now Victus Media). The virtual ghost of one's interests can be a valuable search assistant. <strong>It is vital that users have full control of that information</strong>.  At our site folks can delete or add words they wish associated with their account, and can opt out anytime by disconnecting our service from their Twitter stream. At Victus Media we believe trust is built on open, up front communication and user control.</p>
<h2>How the Intelligent Media Manager Works</h2>
<p>Certain entities come up in your stream more often, naturally reinforcing the weight of that topic. Other topics you mention only once degrade within a week (coincidentally the time window twitter searches reach back to). We chose twitter because it's a natural fit to what we're trying to do (users default to public + straightforward API).</p>
<p>The real magic comes in when these tags empower users to connect on topics that they are passionate about. We look for links and correlations between people and popular trending topics which share categories. While iterating on the software framework , we spent several months brainstorming cool things we could do with the user topics. Tyler recently connected tags to popular trending links from external web sites as a an effective form of social search. My latest contribution is called Social Gravity, and it connects users by topics, creating transient chat rooms based on user chosen topics. I'd like to extend these rooms to a larger index page showing how popular each topic is.</p>
<h2>Segway on Markets, They're on my Mind Today</h2>
<p>What better information sharing system to consider than the market, where <a href="http://findarticles.com/p/articles/mi_m0BPW/is_8_13/ai_n27577326/">real-time is a requirement</a>. The number of financial <a href="http://mondovisione.com/index.cfm?section=articles&amp;action=detail&amp;id=60610">transactions per day</a> is at least in the billions.</p>
<blockquote><p>Currently NYSE and Nasdaq average approximately 2bn shares per day, and the trend is upwards. In terms of shares per trade, the trend in the last four years is sharply downwards, and currently stands at 300 to 400 shares per trade.</p></blockquote>
<p>A cautionary note, I'm familiar with market basics, but have no inside experience (hedge funds, or brokerage houses). But as an avid data miner, it's tough to resist the siren's call of emerging trends in finance. Traders continuiously look at making profit off of market exchanges. I perceive the system as unpredictable, and a lifelike evolving complex adaptive machine. The promise of the market is to provide liquidity, and fairly value just about everything. <em>But how does it self evaluate?</em></p>
<p>The system is far from perfect. Any inadequacies are ripe targets for real-time trades. I suspect that a number of hedge funds make their money on defined systematic effects and predictable micro trends. The secretive trading systems (proprietary in the extreme) are automated and become ineffective in highly volatile markets.</p>
<p>I've spent some time thinking about how much real wealth and value is generated by systematically exploiting the financial system. It's difficult to measure the real social value of short term exploits of our financial system. Ok, enough of my morale wealth generating philosophy.</p>
<p>notes:<br />
<em>I don't enunciate</em> (a comical Dragon speech to text error :)).</p>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/06/21/monetization-for-web2010/">Monetization for Web2010</a> (victusspiritus.com)</li>
<li class="zemanta-article-ul-li"><a href="http://regulargeek.com/2009/08/26/rss-human-filters-and-real-time-streams/">RSS, Human Filters And Real Time Streams</a> (regulargeek.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.centernetworks.com/heres-how-to-fix-the-twitter-suggested-user-advantage">Here's How To Fix The Twitter Suggested User "Advantage"</a> (centernetworks.com)</li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Reblog this post [with Zemanta]" href="http://reblog.zemanta.com/zemified/36c21881-b1ae-4b7c-942c-5f655db4aecc/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/reblog_e.png?x-id=36c21881-b1ae-4b7c-942c-5f655db4aecc" alt="Reblog this post [with Zemanta]" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
