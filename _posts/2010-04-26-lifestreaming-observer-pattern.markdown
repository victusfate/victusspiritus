---
layout: post
status: publish
published: true
title: Lifestreaming Observer Pattern
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3691
wordpress_url: http://www.victusspiritus.com/?p=3691
date: '2010-04-26 04:31:55 -0400'
date_gmt: '2010-04-26 11:31:55 -0400'
categories:
- Uncategorized
tags:
- startups
- social web
- open design
comments:
- id: 4134
  author: DGentry
  author_email: denny+disqus@geekhold.com
  author_url: http://codingrelic.geekhold.com
  date: '2010-04-26 12:27:46 -0400'
  date_gmt: '2010-04-26 17:27:46 -0400'
  content: "&gt; standardized URL lookups for lifestreams (DNS?) which in the short
    term can be<br>&gt; remedied by a new lifestream domain with user added redirects.<br><br>
    \ I suspect getting individual users to do something special is not the best strategy.
    Even though they might be technically capable of setting up a specific DNS record
    or registering with a lifestreaming domain, requiring them to do so raises a barrier
    to adoption. I&#39;m not sure its a useful barrier to raise, there seem to be
    alternative ways to locate people&#39;s lifestreams.<br>  For example: WebFinger
    is intended to let you map an email address to a profile, and from the profile
    to their lifestreams. Similarly you could handle a substantial percentage of users
    by hooking up to Facebook Connect; they&#39;ve either imported the streams to
    Faceook or they consider Facebook to be their stream."
- id: 4139
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-04-26 14:32:54 -0400'
  date_gmt: '2010-04-26 19:32:54 -0400'
  content: Thanks Denton, appreciate your implementation specific suggestions. Of
    course I want to make the process as simple as possible from all angles (user
    as publisher, follower, and curator). I&#39;m aware of WebFinger and hope to see
    it adopted in more places, good point.
- id: 4148
  author: Leland
  author_email: leland@pickple.com
  author_url: ''
  date: '2010-04-27 02:53:44 -0400'
  date_gmt: '2010-04-27 07:53:44 -0400'
  content: Hey Mark, I can grasp the "how" of this project but you didn&#39;t really
    cover the "why". As in.. needs and wants that people might find fulfilled by this.<br><br>On
    my own I can come up with a few things that would be improved by the creation
    of an open social browser but i wanted to hear how you think this will improve
    peoples&#39; lives.  <br><br>-Leland
- id: 4149
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-04-27 09:22:06 -0400'
  date_gmt: '2010-04-27 14:22:06 -0400'
  content: Social web services do a great job of capturing a slice of our online persona.
    But the data we generate socially isn&#39;t woven into the fabric of the web,
    it&#39;s isolated through APIs. <br><br>This combination of fragmentation and
    corporate ownership lead me to explore a different alternative. The tools I work
    on, and data generated can and will be used outside of a company I build. I believe
    social web businesses should define themselves by providing compelling features
    besides holding our friends status hostage, and opting in should be in small steps
    of building trust.
- id: 4150
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-04-27 09:23:36 -0400'
  date_gmt: '2010-04-27 14:23:36 -0400'
  content: Social web services do a great job of capturing a slice of our online  <br>persona.
    But the data we generate socially isn&#39;t woven into the fabric  <br>of the
    web, it&#39;s isolated through APIs.<br><br>This combination of fragmentation
    and corporate ownership lead me to  <br>explore a different alternative. The tools
    I work on, and data  <br>generated can and will be used outside of a company I
    build. I believe  <br>social web businesses should define themselves by providing
    compelling  <br>features besides holding our friends status hostage, and opting
    in  <br>should be in small steps of building trust.
- id: 4157
  author: Leland
  author_email: leland@pickple.com
  author_url: ''
  date: '2010-04-28 00:59:51 -0400'
  date_gmt: '2010-04-28 05:59:51 -0400'
  content: 'Ah Mark I understand. Right now, people&#39;s social identities are under
    lock and key at the large networks such as twitter and facebook. You are trying
    to do for the social web what linux did for the operating system market. <br><br>An
    open system and language for websites to share and create social information.
    It sounds like an excellent idea! : )'
- id: 4161
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-04-28 02:08:03 -0400'
  date_gmt: '2010-04-28 07:08:03 -0400'
  content: I&#39;m not alone. There are plenty of folks that have been wrestling with
    open standards for a distributed social web for several years. <br>The open standards
    comprise many protocols and formats<br>-RSS<br>-Atom<br>-Pubsubhubbbub<br>-Salmon<br>-XML/RDF<br>-Activity
    Streams<br><br>There will be incredible opportunities for social web tools in
    the coming years.
---
<h2>Extension of the URL</h2>
<p>A project design that has proven elusive for the last month or so has been an open social web reader. The primary information format is web feeds, and the implementation goals are that the tool be distributed, open source, and instinctive to use. The usage pattern is one of quickly locating and browsing lifestreams from people, topics, and dynamic web sites we wish to keep track of. In addition tagging,  editing, and curating content will be built into the tool. In short, I seek to lay the ground work for a read write social web layer. The tool will share a few core features with Google Reader, Twitter, and Wordpress. The River2 reader has some beneficial overlap with some of the features I'm interested in. Google Wave also shares some of these design principles but due to a number of issues* didn't become a mainstream utility. </p>
<h2>A new way to browse the web</h2>
<p>As it turns out, web browsers are fully capable of performing the life stream following, tagging, organizing and writing features I'm interested in. The challenges are:</p>
<ul>
<li>standardized URL lookups for lifestreams (DNS?) which in the short term can be remedied by a new lifestream domain with user added redirects. So http://(directory)/markessel would lead to my real time feed enabled lifestream. One of the issues is folks claiming and identifying this stream. Another is spamming or malware streams, which I believe distributed moderation can solve (report user)</li>
<li>browsers being able to easily turn on or off specific services or feeds from a given lifestream</li>
<li>default filters (tunable, extendable) which enable optional browsing instead of a default temporal order</li>
<li>An instinctive tag, drag, drop, and write interface with a choice of reposting options: by email or xml-rpc</li>
<li>mobile friendly. Minimize assumptions about browsers. Enable location filtering, and other addon utility</li>
</ul>
<p>The technology should be usable from any browser and requires a solid working model with small tests. I'll be searching for easy to extend open source tools to provide specific utilities over the next few weeks. Any help would of course be appreciated. When the technology challenges are overcome, then business opportunities open up. One method of fueling ongoing development is lifestream hosting at the project domain, scaled to user/business needs. </p>
<p>Notes:<br />
*= My personal issues with wave: slow load times, page breaking, difficult permissioning, and primarily because it wasn't natively read/write with the existing web without extensions. In addition the follow model was nonexistent.    </p>
