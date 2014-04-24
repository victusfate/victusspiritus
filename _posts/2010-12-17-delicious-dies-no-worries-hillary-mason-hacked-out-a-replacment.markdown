---
layout: post
status: publish
published: true
title: Delicious Dies, no worries Hillary Mason Hacked out a Replacement
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 6279
wordpress_url: http://www.victusspiritus.com/?p=6279
date: '2010-12-17 05:42:35 -0500'
date_gmt: '2010-12-17 12:42:35 -0500'
categories:
- Uncategorized
tags:
- web/tech
- social web
- coding
comments: []
---
<p>[blackbirdpie url="http://twitter.com/hmason/status/15654839669231616"]<br />
There's a buzz in the background of tech communication channels everywhere about Yahoo's recent decision to close down Delicio.us. As a Google bookmark sync'er I'm not personally affected by the shutdown, although I can empathize with folks who are frustrated, because I did actively share bookmarks to Delicious a year or two back. It turns out that every problem is a great opportunity for a novel solution.</p>
<p>I was alerted early this morning by <a href="http://www.twitter.com/julien51">Julien Genestoux</a> about a quick hack combo <a href="http://www.hilarymason.com/">Hillary Mason</a> put together to both export and socially host your Delicious bookmarks.  I've heard only great things about Hillary through a mutual friend Kevin Marshall. Kevin just happens to be hacking out a future evolution of Delicious, <a href="http://knowabout.it">KnowAbout.it</a> which I've <a href="http://www.victusspiritus.com/2010/12/09/love-instapaper-youll-dig-knowabout-it/">mentioned here</a> before.</p>
<p>Another site <a href="http://blog.licorize.com/2010/12/17/delicious-may-be-shutting-down-heres-how-to-migrate-to-licorize/">Licorize</a>, also supports migration from Delicious. There's little shortage of willing and able developers to support the Delicious community in it's transition period.</p>
<p>The github repo for Hillary's utility is at <a href="https://github.com/hmason/gitmarks">github.com/hmason/gitmarks</a>. I've copied the README here to wet your appetite.</p>
<blockquote><p>
========<br />
Gitmarks<br />
========</p>
<p>A web bookmark manager built on git and designed for github. It's searchable and social!</p>
<p>Gitmarks is a script that, given a URL, description, and tags, will download the content of the web page and store it along with the metadata so that you can easily search it (with grep!) and comment on it (with github!)</p>
<p>It's great for groups to collaboratively collect bookmarks in one spot (thanks to git itself!)</p>
<p>=======<br />
Details<br />
=======</p>
<p>For each URL, gitmarks will pull the content and store it under the 'content' directory. It stores the metadata under each tag in the 'tags' directory.</p>
<p>You can use git as usual to see who committed what and when, or you can grep your way to bookmark happiness on the command line.</p>
<p>=====<br />
Usage<br />
=====</p>
<p>python gitmark.py [url]</p>
<p>options:<br />
	-p = do not push to origin (store bookmark locally only)<br />
	-m = description of the bookmark<br />
	-t = a comma-delimited list of tags</p>
<p>Example:</p>
<p>python gitmark.py -m 'my site' -t me,hilary_mason,code,bookmarks http://www.hilarymason.com</p>
<p>===============<br />
OMG Delicious?!<br />
===============</p>
<p>Yes, you can import your delicious bookmarks!</p>
<p>Usage:</p>
<p>python delicious_import.py [username] [password]</p>
<p>(be patient if you have a lot of them.)</p>
<p>=======<br />
License<br />
=======</p>
<p>Copyright 2010 Hilary Mason.</p>
<p>This program is free software: you can redistribute it and/or modify<br />
it under the terms of the GNU General Public License as published by<br />
the Free Software Foundation, either version 3 of the License, or<br />
(at your option) any later version.</p>
<p>This program is distributed in the hope that it will be useful,<br />
but WITHOUT ANY WARRANTY; without even the implied warranty of<br />
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the<br />
GNU General Public License for more details.</p>
<p>You should have received a copy of the GNU General Public License<br />
along with this program.  If not, see <http://www.gnu.org/licenses/>.
</p></blockquote>
