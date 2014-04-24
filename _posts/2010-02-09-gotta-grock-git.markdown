---
layout: post
status: publish
published: true
title: Gotta Grok Git
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 2994
wordpress_url: http://www.victusspiritus.com/2010/02/09/gotta-grock-git/
date: '2010-02-09 05:34:15 -0500'
date_gmt: '2010-02-09 12:34:15 -0500'
categories:
- Uncategorized
tags:
- collaboration
- coding
- source control
comments:
- id: 2919
  author: David Semeria
  author_email: david@lmframework.com
  author_url: http://lmframework.com/blog/about
  date: '2010-02-09 12:43:12 -0500'
  date_gmt: '2010-02-09 17:43:12 -0500'
  content: Thanks Mark, that&#39;s useful.
- id: 2926
  author: Tyler from Everyone Loves Tea
  author_email: tjgillies@gmail.com
  author_url: http://www.everyonelovestea.com
  date: '2010-02-10 01:14:06 -0500'
  date_gmt: '2010-02-10 06:14:06 -0500'
  content: It&#39;s Grok ;)
- id: 2927
  author: Tyler from Everyone Loves Tea
  author_email: tjgillies@gmail.com
  author_url: http://www.everyonelovestea.com
  date: '2010-02-10 01:22:03 -0500'
  date_gmt: '2010-02-10 06:22:03 -0500'
  content: very well done. so proud of you *tear*
- id: 2928
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-02-10 10:38:11 -0500'
  date_gmt: '2010-02-10 15:38:11 -0500'
  content: Haha I lose
- id: 2957
  author: Augmented Reality Overload &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/02/15/augmented-reality-opportunities/
  date: '2010-02-15 08:28:45 -0500'
  date_gmt: '2010-02-15 15:28:45 -0500'
  content: "[...] augmented structures connected to massive back end databases. I
    like to think a future version of git may be like the rows of guns from the matrix
    with millions of applications streaming by, to allow [...]"
- id: 3445
  author: Less than 100 Ways to Make Flexible Web Tools &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/03/19/less-than-100-ways-to-make-flexible-web-tools/
  date: '2010-03-19 07:13:04 -0400'
  date_gmt: '2010-03-19 14:13:04 -0400'
  content: "[...] There are a ton of generous hackers out there that will help you
    get over the hump (Github + Git basics). Web coding isn&#8217;t a spooky [...]"
- id: 4614
  author: Welcome to Ruby, Javascript and Ubuntu Linux Ben | Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2010/06/26/welcome-to-ruby-javascript-and-ubuntu-linux-ben/
  date: '2010-06-26 04:27:36 -0400'
  date_gmt: '2010-06-26 11:27:36 -0400'
  content: "[...] a great tool to share code (you can explore git later [...]"
- id: 5666
  author: ugg boots
  author_email: hzm5157@yahoo.com
  author_url: http://www.cheap-boots-shop.us
  date: '2010-07-08 09:06:00 -0400'
  date_gmt: '2010-07-08 09:06:00 -0400'
  content: Thanks a landlord it! I acquired yet some insight. Life is so colorful,
    we should be able to live in, such as Korea and honor the planet. Human life is
    like rivers, slowly flowing, flowing rivers, flowing through the snow, flows through
    the prairie and ultimately into the sea, return to the embrace of nature, start
    a new reincarnation. Allow us to feel the meaning of life will come only to those
    you have those memories  http://www.cheap-nikeshox.com
- id: 6131
  author: vibram fivefingers
  author_email: 836092693@qq.com
  author_url: http://www.vibramfivefingerse.com
  date: '2010-09-27 02:55:00 -0400'
  date_gmt: '2010-09-27 02:55:00 -0400'
  content: "Aerosmith frontman Steven Tyler and singer Jennifer Lopez will be judges
    on the forthcoming 10th series of American Idol, it has been announced.\r\n"
- id: 9700
  author: One line installs, One button deploys &raquo; Victus Spiritus
  author_email: ''
  author_url: http://www.victusspiritus.com/2011/03/28/one-line-installs-one-button-deploys/
  date: '2011-03-28 06:20:14 -0400'
  date_gmt: '2011-03-28 13:20:14 -0400'
  content: "[...] transcend corporate silos. When I wanted to leverage and learn from
    social coding, I was pointed to git and github. For endless questions about development
    tool installation and configuration I rely on [...]"
---
<p>Git is a file syncronization, and source control tool. Git has been my enemy. It's still a <a href="http://www.victusspiritus.com/2010/02/08/each-time-i-get-my-hands-dirty-i-learn/">spooky animal</a>. Here's how I survive git now without letting it get in the way of me breaking new things.</p>
<p>Install Git Ubuntu/Debian <a href="http://en.m.wikipedia.org/wiki/Advanced_Packaging_Tool?wasRedirected=true">linux</a>:<br />
sudo apt-get install git-core<br />
(refer to references for <a HREF="http://github.com/guides/using-git-and-github-for-the-windows-for-newbies">windows</a> or <a href="http://help.github.com/mac-git-installation/">mac</a> installs)</p>
<p>Setup:<br />
git config --global user.email you@bigco.com<br />
git config --global user.name "Your Name"</p>
<p>Setup new repo?<br />
cd myprojectdirectory<br />
git init<br />
git add .<br />
git commit -am "first commit message" </p>
<p>Grab a repo?<br />
git clone git:repo/proj.git</p>
<p>Status:<br />
git log</p>
<p>Good commit habit to a remote repo:<br />
git commit -am "my new commit"<br />
git pull repo<br />
(no conflicts?)<br />
git push<br />
(if conflicts?)<br />
*run around screaming and breaking things*<br />
git mergetool<br />
or read <a HREF="http://stackoverflow.com/questions/161813/how-do-i-fix-merge-conflicts-in-git">here</a></p>
<p>Revert:<br />
git revert commitnumber<br />
Or to revert one commit<br />
git revert HEAD  </p>
<p>Branch:<br />
git branch mybranchname</p>
<p>Switch branch (changes files think lazy susan):<br />
git checkout mybranchname</p>
<p>List branches:<br />
git branch</p>
<p>Merge branch master into current branch<br />
git merge master  </p>
<p>References:</p>
<ul>
<li><a HREF="http://wiki.freegeek.org/index.php/Git_for_dummies">Git for Dummies</a></li>
<li><a HREF="http://toolmantim.com/articles/setting_up_a_new_remote_git_repository">Toolman Tim</a></li>
<li><a HREF="http://www.kernel.org/pub/software/scm/git/docs/gittutorial.html">Git Tutorial</a></li>
<li><a HREF="http://git-scm.com/documentation">Git Homepage</a></li>
<li><a HREF="http://git.wiki.kernel.org/index.php/InterfacesFrontendsAndTools">Interfaces and Tools</a></li>
<li><a HREF="http://meld.sourceforge.net/install.html">Meld visual merge tool</a></li>
<li><a HREF="http://git.wiki.kernel.org/index.php/GitHistory#Historical_background">History</a>
</ul>
