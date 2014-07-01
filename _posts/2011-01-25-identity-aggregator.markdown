---
layout: post
status: publish
published: true
title: Identity Aggregator
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 6922
wordpress_url: http://www.victusspiritus.com/?p=6922
date: '2011-01-25 09:40:30 -0500'
date_gmt: '2011-01-25 16:40:30 -0500'
categories:
- Uncategorized
tags:
- web/tech
- social web
comments:
- id: 8182
  author: Tweets that mention Identity Aggregator » Victus Spiritus -- Topsy.com
  author_email: ''
  author_url: http://topsy.com/www.victusspiritus.com/2011/01/25/identity-aggregator/?utm_source=pingback&amp;utm_campaign=L2
  date: '2011-01-25 10:46:24 -0500'
  date_gmt: '2011-01-25 17:46:24 -0500'
  content: "[...] This post was mentioned on Twitter by Mark Essel, Odyssée Ndayisaba,
    Mahendra Palsule, Abdul Jaleel K.K, HN Firehose and others. HN Firehose said:
    Identity Aggregator: http://bit.ly/gYgUYV [...]"
- id: 8794
  author: Tyler
  author_email: tjgillies@gmail.com
  author_url: http://www.pdxbrain.com
  date: '2011-02-02 10:03:00 -0500'
  date_gmt: '2011-02-02 10:03:00 -0500'
  content: 'Im a huge advocate for RSA keys as being idetifers. anything that uses
    domain in identification is logically flawed. #1 because domains expire. #2 because
    that domain controls your identity (twitter/facebook) and they can do whatever
    they want with it. With RSA keys on the other hand, only YOU control what you
    do with your identity, and its just a number so its not limited by websites or
    even the internet. Its also awesome because ONLY you can sign material proving
    that you own that key, so its 100% resolvable without any central authority.'
- id: 8806
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2011-02-02 14:48:00 -0500'
  date_gmt: '2011-02-02 14:48:00 -0500'
  content: "Excellent decision criteria. \n\nHow do folks \"lay claim\" to new numbers
    (who doles them out)?\n\nHow do you get past the adoption hurdle? \n\"Hey just
    look me up at any service, look me up at \nhttp://(generic domain)/897bed6539accf9409405fb69a791f2ac3eba515c33da5694026047e616b8f7217571e476a6a1dd729d9aed148ab7eed2bc93fe4e82acb0c7b1c9174fb7282a3.\n\nOr
    is the interface (generic domain)/(nickname) and I authenticate with my private
    rsa key?"
- id: 8811
  author: Tyler
  author_email: tjgillies@gmail.com
  author_url: http://www.pdxbrain.com
  date: '2011-02-02 18:39:00 -0500'
  date_gmt: '2011-02-02 18:39:00 -0500'
  content: |-
    in RSA, you generate your own key, the address space is so large that you won't ever find someone with the same key its essentially a UUID. When creating a public key, you also create a private key that matches your public key, so you can create signatures to verify your public key. here is a good article: http://en.wikipedia.org/wiki/RSA

    The best method i have found is to not associates usernames with keys, but instead to let each node pick what name they will call each key, my server has a separate database where you can add an rsa key and a "username" and it will replace all instances of that key with your specified username.

    It only makes sense that way since thats essentially how "real" names work. Your "DNA" (rsa key) is a constant immutable string of bits, and your name is just something that people call you. My Mom calls me Ty. My Grandpa calls me TJ. you call me Tyler, 3 different names granted by three different entities, and it works because my DNA is constant
---
<p>After reading <a href="http://scobleizer.com/2011/01/25/why-angry-birds-could-turn-into-a-major-identity-player/">Robert Scoble's post</a> on Angry Birds as a serious identity provider, I couldn't resist writing up my thoughts. Big network solutions will never be <i>big enough</I> to include everyone without alternatives. This is a quick follow up to an earlier post <a href="http://victusfate.github.io/victusspiritus/uncategorized/2010/12/22/internet-identity-is-broken/">Internet Identity is Broken</a>.</p>
<p>Net identity isn't best served by being part of the biggest network, it's about inclusion through open protocols. I don't want to develop for or see fifteen log in buttons. One button will do. Identity aggregators (why limit it to one provider?) can perform the hard middleman job of negotiating credentials with many different services. All providers can setup hooks for a browser to approve connection to their aggregation backend. </p>
<p>Consider the following example. I land at <I>shiny new service</i> or install <I>hot new app</I>. My first action is to share my identity with a single button. The service connects to the hooks my ID aggregator has set contingent on my selection. Now an Oauth like approval process happens and all the identities I approve for sharing are relayed to the new service. </p>
<p>That's it.</p>
<p>Related Posts:</p>
<ul>
<li><a href="http://www.avc.com/a_vc/2011/01/building-better-social-graphs-continued.html">Building better social graphs</a></li>
</ul>
