---
layout: post
status: publish
published: true
title: Twitter's List and Search APIs leave much to be desired
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8783
wordpress_url: http://www.victusspiritus.com/?p=8783
date: '2011-05-13 07:47:29 -0400'
date_gmt: '2011-05-13 14:47:29 -0400'
categories:
- Uncategorized
tags:
- web/tech
- social web
- twitter
- coding
comments: []
---
<p>Like polishing up an old wooden rocking chair, over the past several evenings I've been migrating an old Rails application. I was able to get the 3.1beta Rails app (<a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/05/11/the-four-horsemen-of-rails-3-1beta-coffee-script-jquery-scss-and-assets/">sweet updates</a>)  working locally without much trouble. But it's the first Heroku app I've migrated from the 1.8.7 stack to 1.9.2 Badious Bamboo, and it's not quite ready for prime time.</p>
<p>I gutted 20 or so superfluous files and rearranged the interface to incorporate a few visual tricks I've learned since that project went into hibernation. After I was happy with the look and feel I wanted to jazz up the list search functionality and that's where I hit a roadblock. </p>
<h2>Twitter's List API Blow's Chunks</h2>
<p>I spent a couple of hours digging through the <a href="http://dev.twitter.com/doc">API docs</a> and refreshing myself on limits, paging and returned hash data. There's a straight forward URL to get follow (friend) ids. One call returns up to 5000 friends, with iterative calls returning lists of up to the next 5000 friends:<br />
<script src="https://gist.github.com/970670.js"> </script><br />
The next_cursor value in the returned hash allows repeat calls to receive friend lists greater than 5000 accounts. Easy peasy, you'll have a full set of ids in a few API calls even for a super user like <a href="http://twitter.com/scobleizer">Robert Scoble</a>.</p>
<p>But for lists there's no easy way to get back ids or screen_names. List membership requires the following API call:<br />
<script src="https://gist.github.com/970674.js"> </script></p>
<p>Each page returns member data on 20 users, so a list of 500 accounts requires 25 consecutive API hits, which blows. The reason I'm returning all list members is to rapidly narrow down search within lists (that's a long URL of +OR+from:). Context is vital to the quality of information we extract from datasets, and being unable to easily sift through collections of data makes the challenging task of refining information from large collections even more cumbersome. A well implemented API could take in a set of criteria and a list name (context) and rapidly extract matches from the twitter stream. Here's to hoping Twitter and future social data services nail this feature.</p>
<p><script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.5.1/jquery.min.js"></script><br />
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.10/jquery-ui.min.js"></script><br />
<script type="text/javascript"<br />
src="https://gist.github.com/raw/949945/1468755b2659aa0206ef4b0060100b152f44a8d3/growingdivs.js"></script></p>
