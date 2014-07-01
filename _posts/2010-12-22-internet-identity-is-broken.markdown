---
layout: post
status: publish
published: true
title: Internet Identity is Broken
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 6319
wordpress_url: http://www.victusspiritus.com/?p=6319
date: '2010-12-22 06:18:35 -0500'
date_gmt: '2010-12-22 13:18:35 -0500'
categories:
- Uncategorized
tags:
- web/tech
- social web
- digital identity
comments:
- id: 7939
  author: ''
  author_email: dave.winer@gmail.com
  author_url: http://www.scripting.com/
  date: '2010-12-22 14:06:00 -0500'
  date_gmt: '2010-12-22 14:06:00 -0500'
  content: Use domain names.
- id: 7945
  author: msuster
  author_email: msuster@gmail.com
  author_url: http://bothsidesofthetable.com
  date: '2010-12-22 15:23:00 -0500'
  date_gmt: '2010-12-22 15:23:00 -0500'
  content: It sure would be awesome if somebody attacked this problem and gained momentum.  In
    a world that will increasingly fragment it's one of the most important pieces
    of glue we need to remain sane.  Thanks, Mark.  Good dissection of the problem.
- id: 7947
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-12-22 16:18:00 -0500'
  date_gmt: '2010-12-22 16:18:00 -0500'
  content: "I can pick up a new identity for 10 bucks, or a range of IDs newid@domain.ext.
    I might desire different IDs for different services.\n \nDoes it provide any other
    identity information like my name/bio (ala webfinger)? How do other services leverage
    my domain name as an identity, should it be tied to login credentials or provide
    authentication. \n\nI'd prefer not to have to rely on Facebook, Google, Twitter
    or any company (maybe all companies) as an identity provider. "
- id: 7948
  author: ''
  author_email: dave.winer@gmail.com
  author_url: http://www.scripting.com/
  date: '2010-12-22 16:21:00 -0500'
  date_gmt: '2010-12-22 16:21:00 -0500'
  content: I'll give you a sub-domain of scripting.com for free for as long as I have
    the domain. Tell me what IP address to point it to. You can put anything you want
    there. Serious offer.
- id: 7949
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-12-22 16:33:00 -0500'
  date_gmt: '2010-12-22 16:33:00 -0500'
  content: Sounds great. Let me figure out what host/server is best to use and we'll
    go from there. I'll email you at scriptingnews.
- id: 7953
  author: Aaron Klein
  author_email: akdc@seac365.com
  author_url: http://www.aaronklein.com/
  date: '2010-12-22 23:21:00 -0500'
  date_gmt: '2010-12-22 23:21:00 -0500'
  content: This has been a problem for a long time. Looking forward to hearing more
    about what you're building.
- id: 8181
  author: Identity Aggregator &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/01/25/identity-aggregator/
  date: '2011-01-25 09:40:40 -0500'
  date_gmt: '2011-01-25 16:40:40 -0500'
  content: "[...] Identity Aggregator  25Jan 2011  Mark Essel   TweetAfter reading
    Robert Scoble&#8217;s post on Angry Birds as a serious identity provider, I couldn&#8217;t
    resist writing up my thoughts. Big network solutions will never be big enough
    to include everyone without alternatives. This is a quick follow up to an earlier
    post Internet Identity is Broken. [...]"
- id: 10297
  author: How much do you rely on someone else for your digital identity? &mdash;
    Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/07/22/how-much-do-you-rely-on-someone-else-for-your-digital-identity/
  date: '2011-07-22 07:36:11 -0400'
  date_gmt: '2011-07-22 14:36:11 -0400'
  content: "[...] we are is another fractured piece of the digital identity puzzle.
    Late last year I commented on how Internet Identity is Broken. It&#8217;s surprising
    that we rely on something as fragile as our memory and an entity outside of [...]"
---
<p><a href="http://www.myfreewallpapers.net/comics/pages/clark-kent-and-superman.shtml"><img src="{{ site.url }}/assets/2010/12/20101222-081358-300x225.jpg" alt="" title="20101222-081358.jpg" width="300" height="225" class="aligncenter size-medium wp-image-6318" /></a><br />
Yesterday morning I left a comment on <a href="http://www.bothsidesofthetable.com/2010/12/20/the-power-of-twitter-in-information-discovery/#comment-116246391">Mark Suster's <i>Power of Twitter</i> post</a>, relating to the challenges of identity convergence across namespaces (clarifications added).</p>
<blockquote><p>
Can twitter be challenged by an open protocol/channel like Evan (Prodromou) and others believe with ostatus? I believe so, but the relationship between identity and feed source needs to be resolved (UI). When I retweet a post the context and relevance of @username has significance in the twittersphere. Outside of twitter webfinger to bothsidesofthetable.com becomes a symbol for Mark Suster (specifically user@domain). This is the design issue I got caught on while working on OpenGard.in an open social feed reader and it's non-trivial. I plan to follow up and keep working it as resources allow.
</p></blockquote>
<p>Mr. Suster's post was a <i>tip of the hat</I> to the incredible consumption power of twitter as a news and information routing tool. Mark's response to my comment alluded to an identity glue between two popular services.</p>
<blockquote><p>
I had friends who built integrations where if you Tweeted an @ sign and sent to Facebook it converted to your Facebook name. It's true that we need a better integration across namespaces
</p></blockquote>
<p>As a developer I'm aware of the problems with converging symbols across namespaces. Instead of @victusfate a more web friendly description of my twitter identity is twitter.com/victusfate, the URL to my stream. The form <a href="http://code.google.com/p/webfinger/">webfinger</a> utilizes is username@domain.extension which by no coincidence is the same format as an email address.</p>
<blockquote><p>
People have been trying to use URLs as identifiers for people (as OpenID does), as it has great readability/discoverability properties, but this effort has largely failed because of UI/UX design failings, user confusion about URLs, etc.</p>
<p>It's now increasingly accepted that email addresses would be good identifiers for people (since that's what people are used to already, and have on business cards and in their addressbooks, etc.), but we're back to the original problem that email addresses are write-only.</p>
<p>If I give you my email address today, you can't do anything with it except email me. I can't attach public metadata to my email address to give you more information.</p>
<p>WebFinger is about making email addresses more valuable, by letting people attach public metadata to them. That metadata might include:</p>
<p>public profile data<br />
pointer to identity provider (e.g. OpenID server)<br />
a public key<br />
other services used by that email address (e.g. Flickr, Picasa, Smugmug, Twitter, Facebook, and usernames for each)<br />
a URL to an avatar<br />
profile data (nickname, full name, etc)<br />
whether the email address is also a JID, or explicitly declare that it's NOT an email, and ONLY a JID, or any combination to disambiguate all the addresses that look like something@somewhere.com<br />
or even a public declaration that the email address doesn't have public metadata, but has a pointer to an endpoint that, provided authentication, will tell you some protected metadata, depending on who you authenticate as.<br />
... but rather than fight about the exact contents of that file, WebFinger is about making that file discoverable at all. The community can explore and innovate within that discovery file later.
</p></blockquote>
<p>This way victusfate on service X isn't in conflict with victusfate on twitter or any other service. A URL based global ID approach is implemented by the <a href="http://openid.net/get-an-openid/what-is-openid/">openID initiative</a> and requires a server (self hosted or third party) hold your web identity and credentials.</p>
<blockquote><p>
OpenID was created in the summer of 2005 by an open source community trying to solve a problem that was not easily solved by other existing identity technologies. As such, OpenID is decentralized and not owned by anyone, nor should it be. Today, anyone can choose to use an OpenID or become an OpenID Provider for free without having to register or be approved by any organization.
</p></blockquote>
<p>Another identity method which I don't have time to go into great detail in the remainder of this post is OAuth. OAuth uses a third party service to hold your identity like OpenID, but in this case control of identity is restricted to platform providers (Twitter, Facebook, Google, etc).</p>
<p>No matter which tactic is used for identity on the Internet, there are hindrances to portable ID which I hope (and work) to see solved in the next couple of years. Services, URLs, email addresses, and authentication methods all have limited ability to enable cross service compatibility without requiring repeated effort from developers and repeat account creation by users. </p>
