---
layout: post
status: publish
published: true
title: Carry only what is essential, Exceptional Copying
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9281
wordpress_url: http://www.victusspiritus.com/?p=9281
date: '2011-06-19 05:43:16 -0400'
date_gmt: '2011-06-19 12:43:16 -0400'
categories:
- Uncategorized
tags:
- operating systems
comments: []
---
<h2>Copying with excluded files and directories on Windows</h2>
<blockquote>
<pre>
xcopy /S /E source destination /EXCLUDE:ExcludeFile.txt
</pre>
</blockquote>
<h2>Copying with excluded files and directories on Linux, Mac OS X, or *nix</h2>
<p>tar works well for the task at hand</p>
<blockquote>
<pre>
tar -X exclude_file.txt -cvf - source | tar xvf - -C dest
</pre>
</blockquote>
<p><a href="http://articles.slicehost.com/2007/10/10/rsync-exclude-files-and-folders">rsync</a> also has exclusion functionality built in:</p>
<blockquote>
<pre>
rsync -r -t -v -b /source_folder /destination_folder
</pre>
<p>with additional args</p>
<pre>
--exclude 'bad_directory'
</pre>
<p>or</p>
<pre>
--exclude-from '/home/backup/exclude.txt'
</pre>
<p>(the exclude.txt file)</p>
<pre>
path/to/BIGdir
monkies.*
</pre>
</blockquote>
<p>And cp with find, the <a href="http://superuser.com/questions/47986/copy-all-files-and-folders-excluding-subversion-files-and-folders-on-os-x">superuser source</a> of some of these commands. I didn't spend too much time with the last one but it was hiccuping on OS X with directory copying.</p>
<blockquote>
<pre>
find ./source -not \( -name exclude_1 exclude 2 \) -print0 | xargs -0 -IFILES cp FILES ./destination
</pre>
</blockquote>
<p>I tried a variant of this command and while it copied directories, it also copied their contents into the top directory at the destination destination.</p>
<blockquote>
<pre>
find ./source -mindepth 1 -not \( -name exclude_1 exclude_2 -prune \) | xargs -Iitem cp -r item destination
</pre>
</blockquote>
