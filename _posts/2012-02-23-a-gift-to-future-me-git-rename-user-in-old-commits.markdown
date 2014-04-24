---
layout: post
status: publish
published: true
title: A gift to future me, git rename user in old commits
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9955
wordpress_url: http://www.victusspiritus.com/?p=9955
date: '2012-02-23 06:22:56 -0500'
date_gmt: '2012-02-23 13:22:56 -0500'
categories:
- Uncategorized
tags: []
comments: []
---
<p>Say goodbye to old crufty commits from unknown@localmachine</p>
<p><code><br />
#!/bin/sh</p>
<p>git filter-branch --env-filter '<br />
if [ "$GIT_COMMITTER_NAME" = "unknown" ];<br />
then<br />
    export GIT_COMMITTER_NAME="user";<br />
    export GIT_COMMITTER_EMAIL="user@email.com";<br />
fi<br />
if [ "$GIT_AUTHOR_NAME" = "unknown" ];<br />
then<br />
    export GIT_AUTHOR_NAME="user";<br />
    export GIT_AUTHOR_EMAIL="user@email.com";<br />
fi'<br />
</code></p>
<p>Thanks to <a href="http://stackoverflow.com/questions/750172/how-do-i-change-the-author-of-a-commit-in-git">StackOverflow</a> for leading me to a solution to the historical commit username swap.</p>
<p>If you mess up your git_rename.sh don't forget this panic button:<br />
git reset --hard refs/original/refs/heads/master</p>
