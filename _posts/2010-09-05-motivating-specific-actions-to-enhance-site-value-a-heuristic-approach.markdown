---
layout: post
status: publish
published: true
title: Motivating Specific Actions to Enhance Site Value, a Heuristic Approach
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5031
wordpress_url: http://www.victusspiritus.com/?p=5031
date: '2010-09-05 14:49:41 -0400'
date_gmt: '2010-09-05 21:49:41 -0400'
categories:
- Uncategorized
tags:
- startups
- web/tech
- far out
- decision making
- design
comments: []
---
<p><a href="http://www.stuckincustoms.com/2010/09/01/forever-skies/"><img class="aligncenter wp-image-5032" title="ForeverSkies-900x900" src="http://www.victusspiritus.com/wp-content/uploads/2010/09/ForeverSkies-900x900.jpg" alt="" width="320" height="240" /></a><br />
I'm working on marketing research for <a href="http://garagedollar.com">GarageDollar</a> and exploring methods to entice visitors to submit sales. Game elements immediately came to mind, and later in this post I'll enumerate a few actions which are applicable to a broad range of social knowledge sites.</p>
<p>My initial hunch is that showing quality garage sales to visitors will lead to targeted traffic. I'll outline a model in the following section that will help answer the ongoing question every founding team wants to know the answer to, "What is the most important feature we should be developing right now?"</p>
<p><em>The App Value Model, Web Application Performance</em></p>
<p>If you are able to understand precisely how an application provides value, you will know where and when to expend resources to maximize it's performance. Beyond internal metrics, competitors and partners both provide external measures to validate and refine your understanding. One method to put all this data to practical use, is to develop a model that's at least relatively consistent between features. Unlike a business model, the <em>app value model</em> is designed to estimate and gauge the performance of a single application.</p>
<p>[caption id="attachment_5086" align="aligncenter" width="320" caption="In this example the best feature combination is an even mix of 2 features"]<a href="http://www.victusspiritus.com/wp-content/uploads/2010/09/gaussian2d.jpg"><img class="wp-image-5086  " title="gaussian2d" src="http://www.victusspiritus.com/wp-content/uploads/2010/09/gaussian2d.jpg" alt="" width="320" height="240" /></a>[/caption]</p>
<p>The heuristic model I've selected for web app value is a parametric surface. The height represents the sum total perceived value. I'll abbreviate total perceived value as TPV and it's measure depends on the specific offering and strategic goals. For ease of use it helps to normalize the final TPV on a scoring range of 1-10. If you're app scores a 10, your users love the app, nag all of their friends to try it, and you're likely on the road to riches. If the app scores very low, it's a good time to review the key features and find out which area needs changing first. There are many ways to transform separate feature scores into TPV, but following Occam's Razor I'll limit the selection to the simplest method that is able to fit historic measurements: a (weighted) sum or product**.</p>
<p>Parameter values are the feature scores. Features represent all the forms of functionality you're considering adding to an app at any time, in addition to all the current application functions. These features are not required to be independent. For example page design (feature 1) and application response speed (feature 2) can be correlated.</p>
<p>Feature quality is up to each team to decide, and optimize to. While the value of each feature is determined uniquely by each project team, it's important that designers be cognizant of how much TPV shrinks or grows based on design decisions. For web apps a good starting metric for feature fitness is <em>network efficiency</em>.</p>
<p>Network efficiency is the result of:</p>
<ul>
<li>virality coefficienct (new visitors)</li>
<li>visitor satisfaction (retention)</li>
<li>change in vulnerability to external networks</li>
</ul>
<p>If a feature doesn't lead to greater customer satisfaction or bring in new customers, it probably doesn't belong in a web app. The exception to this is a feature which greatly improves the product's stability or resilience. One way to test a perceived low value feature, is to temporarily remove that feature and test it internally, or in a limited number of external trials. If your estimate for network efficiency is off the mark, you can investigate why. This measure bares similarities to conversion metrics but instead of customer acquisition or purchase actions, we track the network efficiency of a feature. While these measures are subject to change, larger or more mature applications become less flexible.</p>
<p><em>Identify Behavior with the Strongest Network Effects, and Reward It</em></p>
<p>The first challenge to improving your (web) application's value is to discover the largest social gradients to higher app value and reward those activities the most.</p>
<p>After a bare bones user model is hacked up (username, points) a strategic decision is required on whether to work within larger networks (Facebook, Twitter, Google) or to remain independent. Larger networks enable rapid communication and authentication while making your app vulnerable to the whims of external businesses*. You can see how the feature of connectivity begins to map to the network efficiency of the feature. My default position is to use third party networks if they add value, but not be reliant on them as a sole source of growth^. The more effective channels you have, the more resilient your business is.</p>
<p>I'll conclude with a list of game elements I'm considering for GarageDollar that will enhance displayed sale quality:</p>
<ul>
<li>reward garage sale submissions</li>
<li>reward garage sale reviews</li>
<li>link to a leaderboard for garagedollar members ranked by total points accumulated. have a separate page that shows specific member stats</li>
<li>reward identification of spam/out of date sales</li>
</ul>
<p>Notes:<br />
*= changes in third party systems can force you to repeatedly update how your business connects, Fees can be leveraged for access, etc.<br />
**= The weights could all be unity, a number between 0 and 1 determined by the design team or other meaningful metric, a correlation matrix, or even more complicated models. More complex models can minimize error with an appropriate system model (least squares, L1 norm, filters).<br />
^ =  if you have to sell your soul, make sure you sell it to multiple devils</p>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://www.kaushik.net/avinash/2010/08/qualitative-web-analytics-expert-heuristic-evaluations.html">Qualitative Web Analytics: Heuristic Evaluations Rock!</a> (kaushik.net)</li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Enhanced by Zemanta" href="http://www.zemanta.com/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/zemified_e.png?x-id=173d670a-dc74-4a10-a6e8-06c6032f1c8d" alt="Enhanced by Zemanta" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
