---
layout: post
status: publish
published: true
title: 'Dynamic Design Patterns: A Hybrid Solution'
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2803
wordpress_url: http://www.victusspiritus.com/?p=2803
date: '2010-01-22 07:08:28 -0500'
date_gmt: '2010-01-22 14:08:28 -0500'
categories:
- Uncategorized
tags:
- coding
- continuous beta
- do no harm
- design
comments:
- id: 2841
  author: Ron W
  author_email: None
  author_url: http://profiles.yahoo.com/u/UODONP72OJHLT5G36EXMFAQ4TE
  date: '2010-02-03 10:18:28 -0500'
  date_gmt: '2010-02-03 15:18:28 -0500'
  content: re. do no harm - i&#39;ll offer up Craigslist as the ultimate example.
    they haven&#39;t improved anything since the start. i, as many others, complain
    about the lack of features, the unrealized potential. but the simplicity and lack
    of change may be the very reasons for its success. a sort of lazy brilliance there.<br><br>anyway,
    regarding your hybrid idea,  i&#39;m reminded of Vaclev Havel&#39;s statement
    that obsession, of any type, is the greatest evil. stuff like Agile, which is
    so dogmatic and one-sided is just one more symptom of IT&#39;s continuing wish
    for silver bullets. no balance tho, and things fall over. so, of course, the beta
    forever, release frequently mantra needs a yin to its yang.<br><br>Ron Wolf
- id: 2847
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-02-03 20:35:55 -0500'
  date_gmt: '2010-02-04 01:35:55 -0500'
  content: Thanks Ron, great example with Craig&#39;s List. Many of my clock cycles
    get caught up hashing over design tradeoff, agree that a silver bullet traps us
    from seeing what fits a particular problem best. This post is another faint grab
    at a framework for approaching challenges.<br><br>I honestly don&#39;t know what&#39;s
    best, but my hope is that feedback from the right users helps influence a good
    starting concept.
- id: 2856
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-02-04 13:53:22 -0500'
  date_gmt: '2010-02-04 18:53:22 -0500'
  content: I need to add an email contact to my about page. This isn&#39;t the first
    time folks have had trouble tracking me down. Contact me at messel at victusmedia
    dot com or messel at gmail dot com
---
<p><em>If it ain't broke, leave it alone? Break it now anyway? Or break something new?</em></p>
<p>Two design patterns compete for adoption: Do No Harm, and Continual Beta. This post suggests a strategy for keeping the best features of both methodologies.</p>
<h2>Do No Harm</h2>
<p>The Do No Harm philosophy may be adopted after other early design methods. Do No Harm may begin from a bear bones form of minimalism, with only a single desirable feature implemented. Or Do No Harm may follow an unstable alpha/beta period. Once a design finds market traction, the breaks are put on and changes are made only when absolutely necessary. Afterall, how much change can users reasonably tolerate? A great example of Do No Harm is the web dating company <a href="http://plentyoffish.com">Plenty Of Fish</a>. Architected by a single designer (its founder Markus Frind) the tool has caught a massive market. Markus tweaked the interface only when absolutely necessary.</p>
<h2>Riding the Edge Means Continuous Beta</h2>
<p>Never settle. Never sleep. The mantra of Continuous Beta is to be ever changing. The market environment is dynamic so why should designs be any less malleable? Continuous Beta seeks iterative change ahead of the market when possible. The goal of design is to trail blaze, leaving other products to copy tactics, while driving market forces trample over static thinking.</p>
<p>The risks of continuous change include copycats and stability. A copycat may do a better job of matching a product to user needs <strong>now</strong>. Without great care and resources stability may suffer, due to constant flux of the design. Product #fail alienates paying customers (and free users).</p>
<p>Example of Continuous Beta success stories include</p>
<ul>
<li>Gmail: it just left "beta" after years but there are always new Google labs tweaks to try out</li>
<li>Twitter: they recoded their most time hungry processes with scala to help with scaling issues. They are opening the streaming API, and the Suggested User List got swapped to improve the new user experience (I agree with <a href="http://scobleizer.com/2010/01/21/review-open-listorious-vs-closed-new-twitter-suggestion-list/">Robert Scoble</a> that leveraging Listorious is a good direction to move in)</li>
<li>Facebook: they just flipped from default private to public and are continuously adapting their infrastructure and API.</li>
</ul>
<p>The space of web programming is ripe for heavily iterative processes. Streamlined external interfaces and new functional combinations drive software evolution. Early prototypes are hacked together feverishly, then torn down and remade. Each release may frustrate some users while satisfying others. Devs that seek wide audience adoption have to make this exchange to increase their user base.</p>
<h2>Dynamic Design Patterns: A Hybrid Solution</h2>
<p>A hybrid design solution focuses on the best aspects of Do No Harm and Continuous Beta. The design favors change or stability as necessary driven by the current and expected market.</p>
<p>The greatest feature of Do No Harm is that it is a working solution for at least one community now. The user interface and experience may be just right.</p>
<p>Continuous Beta recognizes that what works today will not work tomorrow. User needs change and heavier network connectivity offers new opportunities.</p>
<p><strong>The Hybrid</strong>: Begin with the mantra of Continuous Beta at project inception. After each major version release, determine if the product is better off transitioning to a maintenance phase, or to continue to be replaced by new versions with potentially large UI/UX changes. Even a pure minimalist single feature design falls into this pattern. The Continuous Beta period ends when the feature is selected, and no additional features are added without major market pressure.</p>
<p>If the current market is saturated and research dictates little change in user desired features, you have clear signals to transition a product into a maintenance phase. Optimize the hell out of your current model and squeeze every ounce of performance out of it.</p>
<p>The project may fluxuate from dynamic to stable, but a large reverse of this trend is a signal for a complete redesign.</p>
<p>Great Inspiration from:</p>
<ul>
<li><a href="http://arnoldwaldstein.com/2010/01/beta-is-a-state-of-mind/">Beta as a state of mind</a> by Arnold Waldstein</li>
</ul>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://blog.oneriot.com/content/2010/01/three-reasons-why-twitter%25e2%2580%2599s-new-streaming-api-rocks/">Three Reasons Why Twitter's New Streaming API Rocks</a> (oneriot.com)</li>
<li class="zemanta-article-ul-li"><a href="http://www.socialmedia.biz/2010/01/21/2010-conferences-social-media-tech-marketing/">2010 conferences: Social media, tech, marketing</a> (socialmedia.biz)</li>
<li class="zemanta-article-ul-li"><a href="http://code.kynetx.com/2010/01/22/kynetx-developer-program-vision-comes-to-life-with-more-than-800-new-apps/">Kynetx Developer Program Vision Comes to Life with More Than 800 New Apps</a> (code.kynetx.com)</li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Reblog this post [with Zemanta]" href="http://reblog.zemanta.com/zemified/24d83d6a-0dc0-44ab-b729-5df3c7b4a821/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/reblog_e.png?x-id=24d83d6a-0dc0-44ab-b729-5df3c7b4a821" alt="Reblog this post [with Zemanta]" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
