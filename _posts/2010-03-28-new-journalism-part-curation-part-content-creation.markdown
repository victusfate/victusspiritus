---
layout: post
status: publish
published: true
title: New Journalism, Part Curation Part Content Creation
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 3386
wordpress_url: http://www.victusspiritus.com/?p=3386
date: '2010-03-28 05:29:17 -0400'
date_gmt: '2010-03-28 12:29:17 -0400'
categories:
- Uncategorized
tags:
- social web
- victus media
- opengardin
- curation
- design
comments:
- id: 3648
  author: eugmandel
  author_email: eugene.mandel@gmail.com
  author_url: ''
  date: '2010-03-28 17:20:10 -0400'
  date_gmt: '2010-03-28 22:20:10 -0400'
  content: I checked out opengard.in. For now it looks like simply a <a href="http://status.net"
    rel="nofollow">status.net</a> deployment. I bet there is more to it, as implied
    in your post, but none of it shows on the actual site. Care to elaborate? <br>Thanks,<br>  -Eugene
- id: 3649
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-03-28 17:35:02 -0400'
  date_gmt: '2010-03-28 22:35:02 -0400'
  content: Sure Eugene, <a href="http://status.net" rel="nofollow">status.net</a>
    is a placeholder for the work we have in development. Not by chance, we&#39;re
    relying on much of the protocols within the <a href="http://status.net" rel="nofollow">status.net</a>
    group to get real time feeds and create an open social web reader. We have plenty
    of work to do:<br><br>- coming up with a great feed organization page<br>- adding
    a tagging system so browsers can tag content in their streams<br>- developing
    a point system to keep a tally of user effort tagging content, or creating bundles
    that are appreciated by friends<br>- creating a framework for users to customize
    their portals. We&#39;ll have a couple of simple front ends for compressed browsing
    but I&#39;m hoping users will hack out their own favorites.<br><br>Now after reading
    Robert&#39;s request & feedback I&#39;m brainstorming ways we can integrate easy
    drag and drop from feed/stream data to bundles. I think the wave protocol or a
    variant of it could be ideal for this but I&#39;m not sure how light weight we
    can make it.<br><br>We&#39;ll make as much of this open source as we can. Do you
    develop at all, we could use help? I&#39;m looking around today for open source
    solutions to save time to get a wire frame live.
- id: 3650
  author: eugmandel
  author_email: eugene.mandel@gmail.com
  author_url: ''
  date: '2010-03-28 17:45:39 -0400'
  date_gmt: '2010-03-28 22:45:39 -0400'
  content: 'Thanks for the clarification Mark. I liked R. Scoble&#39;s post - I see
    it as a CMS for journalists/curators. I do develop, but the problem I&#39;m after
    is different - digesting signals created by multiple content creators and curators.
    Here is an example of a digest for the foodie community on Twitter: <a href="http://www.mustexist.com/demo"
    rel="nofollow">http://www.mustexist.com/demo</a><br>Your work does look interesting
    and I will be following it. Would like to talk sometime.<br><br>Cheers,<br>  -Eugene'
- id: 3651
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-03-28 18:16:24 -0400'
  date_gmt: '2010-03-28 23:16:24 -0400'
  content: I&#39;m highly available asynchronously and almost never available otherwise.
    Please hit me up by email anytime, messel at victusmedia dot com.<br><br>If you
    like where we&#39;re going with Victus Media and it&#39;s business I&#39;ll make
    sure I get in touch with you by phone<br><br>So are you going for the StockTwits
    of foodies? <br><br>Growing a community out of a twitter segment has proven to
    be effective if you have the right super psychologist (Phil Peralman) or community
    superstar (Howard Lindzon), or dataminer addict (Soren Macbeth) on your side.
- id: 3718
  author: Seize Moments of Opportunity, Doubling Down &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/03/31/seize-moments-of-opportunity-doubling-down/
  date: '2010-03-31 05:21:33 -0400'
  date_gmt: '2010-03-31 12:21:33 -0400'
  content: "[...] Silicon Dragon (SDr), the most accomplished wave programmer I know
    to get his feedback on a curation tool idea. I&#8217;m now planning to make a
    technology investment by hiring SDr for a temporary project. The [...]"
---
<p style="text-align: center;"><a href="http://aakin.com/"><img class="aligncenter size-full wp-image-3390" title="Aakin.com" src="{{ site.url }}/assets/2010/03/Aakin.com_.jpg" alt="" width="500" height="380" /></a><br />
<em> Image courtesy of Aakin Patel (enjoy his other work)</em></p>
<p>Tech media and fellow startup junky Robert Scoble <a href="http://scobleizer.com/2010/03/27/the-seven-needs-of-real-time-curators/">recently</a> <a href="http://www.cinchcast.com/scobleizer/35985">clarified</a> the type of tool(s) he needs to make the job of curating <a class="zem_slink" title="real-time web" rel="homepage" href="http://www.readwriteweb.com/archives/introduction_to_the_real_time_web.php">real time web</a> information easier, faster, and more productive. Part of what he needs overlaps heavily with what we're designing towards with <a href="http://opengard.in">opengard.in</a>'s social reader, but some of what Rob's looking for is totally new. One of the most intriguing concepts he discussed is the bundle or molecule (he and <a class="zem_slink" title="Dave Winer" rel="homepage" href="http://scripting.com">Dave Winer</a> have discussed the idea before).</p>
<p>Here's a use case: While a curator is checking out a stream of feed updates, they spot something novel and it ripples in the information stream they're observing. The curator can then drag and drop the updates and recreate them into a new bundle which they can annotate and repost (refeeds). What we need to accomplish this is a reorganization of the real time stream of updates. Blogs can achieve this task now, but it can take a fair amount of work on the part of the author.</p>
<p>What I believe is the best solution are social readers that enable drag and drop functionality, and content creation systems which can speak the same language. An open standard for content transformation would allow any capable reader, and any capable blogging platform to fulfill the need Robert is asking for help with. Both social reader and content creation will enable tagging, and give the curator a permalink at bundle initialization. This way bundles have raw tags and curated tags, perhaps with different meanings. After the curator/creator is satisfied with the bundle they can publish it by dragging it onto another capable launching area, or by simply hitting a post now button. The raw feed data will be visible in the bundle, in the same format that it appears natively on the web (audio, video, images, visual or text).</p>
<p>More to come as we focus in on what aspects of this we can best achieve with the resources we have at <a href="http://victusmedia.com">Victus Media</a>. If anyone else is targeting specific aspects of this, in an open source form please get in touch with myself (messel at victusmedia dot com) or ping Tyler (<a href="http://identi.ca/tylergillies">http://identi.ca/tylergillies</a>). I'm particularly interested in the protocols for easy drag and drop exchange of feed updates between browsers.</p>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><a class="zemanta-pixie-a" title="Reblog this post [with Zemanta]" href="http://reblog.zemanta.com/zemified/78d2608e-1663-431f-a994-6aa5ddd2d571/"><img class="zemanta-pixie-img" style="border: none; float: right;" src="http://img.zemanta.com/reblog_e.png?x-id=78d2608e-1663-431f-a994-6aa5ddd2d571" alt="Reblog this post [with Zemanta]" /></a><span class="zem-script more-related pretty-attribution"><script src="http://static.zemanta.com/readside/loader.js" type="text/javascript"></script></span></div>
