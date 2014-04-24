---
layout: post
status: publish
published: true
title: Music Management Feature Gap for iOS and Apple
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9158
wordpress_url: http://www.victusspiritus.com/?p=9158
date: '2011-06-05 11:15:00 -0400'
date_gmt: '2011-06-05 18:15:00 -0400'
categories:
- Uncategorized
tags:
- music
- apple
- design
- CouchDB
comments: []
---
<p>Last week I loaded up on a hundred+ Drum and Bass and mixed Electronica tracks thanks to Pandora's discovery engine and the Music Genome project. But I'm having trouble configuring a set of playlists for my favorites which changes with time. Out of the mixed albums I purchased I may decide to regularly listen to only half or fewer of the tracks after a few listening cycles.</p>
<p> My options are:</p>
<ul>
<li>to listen to the music at home or via the iPod app and manually create playlists from all the songs. I'd have to do this regularly to maintain a current list. But I don't have time to listen for hours at home, and synchronizing music with iTunes has always caused me issues with duplicates, plugging in the phone, plus it's way too slow</li>
<li>DropBox allows caching local files, but m3u playlists don't work, and the DropBox music player has limited features</li>
<li>BoxyTunes extends DropBox music by enabling the creation of a single locally cached playlist of songs. It's missing the option for several playlists, and doesn't automatically repeat lists when it finishes playing the last track. Interruption from work flow or reading to restart is an unnecessary distraction</li>
</ul>
<h2>Plan B</h2>
<p>An option that I didn't call out above is one I'd need to hack out myself, when my schedule opens up in late summer/fall. What I'm dreaming up is a local CouchDB or connected database cached on every listening device:</p>
<ul>
<li>any iOS device, iPhone, iPod, iPad I set up</li>
<li>any laptop or desktop: aka my MacBook Air and iMac</li>
<li>anything else with sufficient resources like a modern sound system</li>
</ul>
<p>On iOS or other mobile devices an app front end saddled to local, and remote (when available) databases would be ideal. On the desktop a rich web app or dedicated app would suffice. All UIs would be designed to support local playlist editing and continuous synchronization when the system is on wifi, or single click manually activated wireless sync. </p>
<p>Songs which don't strike an immediate chord may be filtered and that action replicated everywhere. In addition there'd be topics (tags) where friends suggest and share tracks, creating dynamic stations (gotta respect licensing).</p>
<h2>Open Questions</h2>
<ol>
<li>Has this already been done?</li>
<li>If not is it too tough to patch together in a couple months part time?</li>
</ol>
