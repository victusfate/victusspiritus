---
layout: post
status: publish
published: true
title: Replication versus Synchronization, my first serverfault answer
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 6933
wordpress_url: http://www.victusspiritus.com/?p=6933
date: '2011-01-26 12:23:18 -0500'
date_gmt: '2011-01-26 19:23:18 -0500'
categories:
- Uncategorized
tags:
- web/tech
- coding
- databases
- stackexchange
comments: []
---
<p>While I've looked up plenty of questions and answers on <a href="http://serverfault.com/">serverfault.com</a> in the past, before a couple of days ago I had yet to answer a question (or log in). While skimming related questions to one I was looking up information on, I came across an <a href="http://serverfault.com/questions/227149/what-is-the-difference-between-replication-and-synchronization">unanswered query</a>:</p>
<blockquote><p>
In phpMyAdmin there is a tab for configuring Replication and one for Synchronization.</p>
<p>    * What is the difference between Replication and Synchronization?<br />
    * When do you should use the one or the other?</p>
<p>Thanks, Udo
</p></blockquote>
<p>I decided to keep my response short and sweet, and responded with a working definition of those two database terms:</p>
<blockquote><p>
Replication is used to describe the event of copying data. Synchronization is usually continuous (at least one way) replication that maintains consistency between multiple data sources.</p>
<p>From <a href="http://www.phpmyadmin.net/documentation/#faq9_1">phpmyadmin.net documentation</a></p>
<blockquote><p>
9.1 How can I synchronize two databases/tables in phpMyAdmin?</p>
<p>You can now synchronize databases/tables in phpMyAdmin using the Synchronize feature. It allows you to connect to local as well as remote servers. This requires you to enter server host name, username, password, port and the name of the database. Therefore you can now synchronize your databases placed on the same server or some remote server.</p>
<p>This feature is helpful for developers who need to replicate their database’s structure as well as data. Moreover, this feature not only helps replication but also facilitates the user to keep his/her database in sync with another database. Other than the full database, certain tables of the databases can also be synchronized.
</p></blockquote>
</blockquote>
