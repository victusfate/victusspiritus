---
layout: post
status: publish
published: true
title: Optimal Dynamic Network Paths, why current wireless Internet frameworks fail
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
excerpt: "<h1><span style=\"background-color: #ffffff;\">Mobile vs. Internet Communication,
  we share one Internet split by greed</span></h1>\r\n<span style=\"background-color:
  #ffffff;\">Current wireless Internet providers use a single service provider or
  access point to the full Internet backbone. Whether you're on AT&amp;Ts network
  through your iPhone, or Verizon's network for your soon to be released <a href=\"http://www.techcrunch.com/2009/10/18/verizon-droid-is-the-real-deal/\">Droid</a>,
  you send and receive information first through a local wireless connection. But
  there is a problem with this restricted network design, not all available paths
  for local wireless connectivity are equally burdened, and enforcing structure on
  information flow at the beginning and end of wireless access only serves to slow
  it down."
wordpress_id: 1905
wordpress_url: http://www.victusspiritus.com/?p=1905
date: '2009-10-18 08:24:43 -0400'
date_gmt: '2009-10-18 15:24:43 -0400'
categories:
- Uncategorized
tags:
- web/tech
- open spectrum
- communication
- collaboration
- design
comments: []
---
<h1><span style="background-color: #ffffff;">Mobile vs. Internet Communication, we share one Internet split by greed</span></h1>
<p><span style="background-color: #ffffff;">Current wireless Internet providers use a single service provider or access point to the full Internet backbone. Whether you're on AT&amp;Ts network through your iPhone, or Verizon's network for your soon to be released <a href="http://www.techcrunch.com/2009/10/18/verizon-droid-is-the-real-deal/">Droid</a>, you send and receive information first through a local wireless connection. But there is a problem with this restricted network design, not all available paths for local wireless connectivity are equally burdened, and enforcing structure on information flow at the beginning and end of wireless access only serves to slow it down.<a id="more"></a><a id="more-1905"></a><br />
</span></p>
<p>I made an off the cuff <a href="http://www.avc.com/a_vc/2009/10/a-big-week-for-the-mobile-web.html#comment-20313564">comment</a> about mobile networks on <a href="http://www.avc.com/a_vc/2009/10/a-big-week-for-the-mobile-web.html">Fred Wilson's post on mobile tech this morning</a>. What we really need is all the wireless providers to come to an agreement, and work out a solution that allows for access to ANY of their networks as a local solution. The least burdened/most capable network provider (judged by a third unbiased party/business) would always win out. The even distribution of wireless data will provide value to all users/customers and profit to the providers themselves.</p>
<h1><strong>How the Internet Works</strong></h1>
<p><span style="background-color: #ffffff;">Here are quick introductions to how the Internet works in regards to data routing (routing for dumbies). Real time packet navigation/routing is non-trivial because the entire network knowledge isn't known at any point in the journey.</span></p>
<ul>
<li><a href="http://www.theshulers.com/whitepapers/internet_whitepaper/index.html">How Does the Internet Work? by Rus Shuler</a></li>
<li><a href="http://www.garretwilson.com/essays/computers/routing.html">The Journey of Internet Packets by Garret Wilson</a></li>
<li><a href="http://en.wikipedia.org/wiki/Packet_switching">Packet Switching</a></li>
<li>And of course <a href="http://en.wikipedia.org/wiki/Internet">The Internet</a> as background info</li>
</ul>
<p>As to why I believe the Internet has become so important, I refer you to <a href="http://www.avc.com/a_vc/2009/10/the-blog-where-everybody-knows-your-name.html#comment-20213433">another comment on Fred's blog</a> (I spend a lot of time commenting there) in response to a friend Shana Carp's comment.</p>
<blockquote><p>I was just having an old man's mid afternoon siesta (was up till 1am playing with Google Wave, then got up at 5am with Michelle) and dreaming about network link strength (a cool visualization chart that I don't know how to code-&gt; much like my current foray into building a google wave robot with scala).</p>
<p>Google's breakthrough information mapping was counting links, real time information quality doesn't have time to develop links, so we require other measures. Every time I follow a link, some part of me feels like I'm strengthening a neural connection of some super smart but as of yet non-existent entity. Our usage of the Internet "teaches it" by making direct connections between abstract concepts. Loosely we train the neural network of the web. Crowd sourcing sites do this with votes, social sites do with likes, and twitter does it with retweets.</p>
<p>The further strides we make in building the Internet's depth, by making it a richer experience, the greater we are rewarded. It's a feedback loop. The more I improve Internet usage efficiency, by adding useful services, the richer I become. The intelligence of the Internet isn't an isolated entity either, it's composed of a billion or so people actively using it, generating and connecting content. Our attention, and shared time and thoughts here are changing the structure of the web in a real way.</p>
<p>Look at what became of traditional advertising, Google's 20billion dollar plus revenue stream didn't come from no where, it came directly out of the pockets of traditional advertising, which was a lot bigger market than 20 billion dollars. So Google shrunk the industry, and captured the revenue - classic disruption.</p></blockquote>
<h1>Information Theory</h1>
<p><a href="http://en.wikipedia.org/wiki/Information_theory#Mutual_information_.28transinformation.29">Shannon's Information Theory</a> provides us with a measure of information transmission capability for a channel, and it's direct relation to the <a href="http://en.wikipedia.org/wiki/Entropy_(information_theory)">Entropy </a>of the information distribution. The more the underlying probability distribution tends toward higher entropy (less predictable system), the greater the amount of information that can be transmitted over a channel.</p>
<p>This applies to dynamic network paths as well theoretical channels (<span style="color: #ff0000;">this is a hypothetical leap for me, it's a gut feeling</span>). Restrict portions of the path, and limit the overall information transmission capability through the network. This is one of the reasons why the Internet works so well for information sharing, it minimizes network path restriction. When telecommunication providers restrict the beginning and end of a wireless packets journey (they're own service), they are in fact reducing the choices for the network path, and ultimately the information transmission rate through the network.</p>
<p>As an interesting aside, in regards to text transmission (blogs, text messages, email), this excerpt describes the entropy of human language in trials (our text data can be encoded in many different binary formats though):</p>
<blockquote><p>A long string of repeating characters has an entropy rate of 0, since every character is predictable. The <a style="text-decoration: none; color: #002bb8; background-image: none; background-attachment: initial; background-origin: initial; background-clip: initial; background-color: initial; background-position: initial initial; background-repeat: initial initial;" title="Entropy rate" href="http://en.wikipedia.org/wiki/Entropy_rate">entropy rate</a> of English text is between 1.0 and 1.5 bits per letter,<sup><a style="text-decoration: none; color: #002bb8; background-image: none; background-attachment: initial; background-origin: initial; background-clip: initial; background-color: initial; white-space: nowrap; background-position: initial initial; background-repeat: initial initial;" href="http://en.wikipedia.org/wiki/Entropy_(information_theory)#cite_note-0">[1]</a></sup> or as low as 0.6 to 1.3 bits per letter, according to estimates by Shannon based on human experiments</p></blockquote>
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles by Zemanta</h6>
<ul class="zemanta-article-ul">
<li class="zemanta-article-ul-li"><a href="http://blogs.wsj.com/marketbeat/2009/10/07/iphone-voip-decision-a-smart-political-play-by-att/">iPhone VOIP Decision: A Smart Political Play by AT&amp;T?</a> (blogs.wsj.com)</li>
<li class="zemanta-article-ul-li"><a href="http://blog.seattlepi.com/techchron/archives/179843.asp?source=rss">Swift response to net neutrality proposals</a> (seattlepi.com)</li>
</ul>
<p>[wave id="googlewave.com!w+ZCtUJ1z4A"]</p>

