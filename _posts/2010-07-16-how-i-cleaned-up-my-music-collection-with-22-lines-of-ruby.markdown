---
layout: post
status: publish
published: true
title: How I cleaned up my music collection with 22 lines of ruby
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 4581
wordpress_url: http://www.victusspiritus.com/?p=4581
date: '2010-07-16 10:13:39 -0400'
date_gmt: '2010-07-16 17:13:39 -0400'
categories:
- Uncategorized
tags:
- coding
- ruby
comments:
- id: 4880
  author: Guilherme Garnier
  author_email: guilherme.garnier@gmail.com
  author_url: http://blog.guilhermegarnier.com
  date: '2010-08-02 10:42:06 -0400'
  date_gmt: '2010-08-02 15:42:06 -0400'
  content: Great work! I´m trying to do something very similar to catalog my mp3 files,
    but I´m having trouble with special characters (like "`" or letters with accents).
    Do you have any idea how to treat them in the script?<br><br>Thanks!
- id: 4884
  author: Mark Essel
  author_email: messel@gmail.com
  author_url: http://www.victusspiritus.com/
  date: '2010-08-02 21:20:25 -0400'
  date_gmt: '2010-08-03 02:20:25 -0400'
  content: Unfortunately I had the same issue Guilherme. I failed to properly handle
    those character types in files. My solution was to rename those files. Luckily
    there were only 1o-15 cases.
---
<p>*update* I added the music sort files to a github repo: <a href="http://github.com/victusfate/music-sort">http://github.com/victusfate/music-sort</a></p>
<p>I've got a fairly sizable collection of music. It's more than I need, and certainly more than I want to worry about. I decided before nuking it to make one more effort to clean it up and shrink it down to one directory. This script could have been 21 lines of code but I preferred monitoring it with a puts statement.</p>
<p>The first pass code:</p>
<pre>require 'fileutils'
orig = '/home/messel/Desktop/music/'
dest = '/home/messel/Desktop/mobilemusic/'
Dir.chdir(orig)
Dir.glob('*.m3u') do |m3u_name|
  m3us = IO.readlines(m3u_name)
  out_m3u = File.new(dest+m3u_name,'w+')
  m3us.each do |m3u|
    m3u.gsub!(/\/,'/')
    b1 = File.basename(m3u)
    out_m3u &lt;&lt; b1 # write new m3u with carriage return
    m3u = m3u.chomp # remove carriage return for file manip
    unless m3u['#']
      basename = File.basename(m3u)
      puts "orig #{orig+m3u} dest #{dest+basename}"
      if File.exist? orig+m3u and !File.exist? dest+basename
        FileUtils.cp(orig+m3u,dest+basename)
      end
    end
  end
  out_m3u.close
end</pre>
<p>As you can imagine for large music collection operations, there were a number of exception files that were missing or had special characters I failed to handle. My next script identified the missing files from my new music collection folder, but that were still referenced on playlists.</p>
<pre>def check_for_file(m3u_name)
  m3us = IO.readlines(m3u_name)
  m3us.each do |m3u|
    m3u = m3u.chomp # remove carriage return for file manip
    puts "List #{m3u_name} missing #{m3u}" unless File.exist? m3u or m3u['#']
  end
end

if (ARGV.size &gt; 0)
  check_for_file ARGV[0].to_s
else
  Dir.glob('*.m3u').each do |m3u_name|
    check_for_file m3u_name
  end
end</pre>
<p>For this script I added an optional parameter (ARGV) to let me test it on a single file first before going hog wild in the full directory. After identifying a number of missed files, I modified the missing script to go back and grab the files from another remote disk where I back up much of my older music.</p>
<pre>require 'fileutils'

def check_for_file(m3u_name,path,opath)
  m3us = IO.readlines(m3u_name)
  m3us.each do |m3u|
    m3u = m3u.chomp # remove carriage return for file manip
    unless File.exist? m3u or m3u['#']
      puts m3u
      Dir.glob(path+'**/'+m3u).each do |found|
         puts "found file on FIRELITE #{found}"
         FileUtils.cp(found,opath + m3u)
      #      Process.exit
      end
    end
  end
end

path = '/media/FIRELITE_/music/'
opath = '/home/messel/Desktop/music/'

if (ARGV.size &gt; 0)
  check_for_file ARGV[0].to_s, path, opath
else
  Dir.glob('*.m3u').each do |m3u_name|
    check_for_file m3u_name, path, opath
  end
end</pre>
<p>Even after all that there were many play lists with files that I no longer had or knew their whereabouts. Thus came the great pruning. The following program identifies at least one missing music file, then creates a new output play list skipping over any missing files.</p>
<pre>require 'fileutils'
def check_for_file(m3u_name,opath)
  prune = false
  m3us = IO.readlines(m3u_name)
  m3us.each do |m3u|
    m3u = m3u.chomp # remove carriage return for file manip
    unless File.exist? m3u or m3u['#']
      prune = true
      break
    end
  end
  if prune
    puts "Pruning from #{m3u_name}"
    FileUtils.mv(m3u_name,opath+"back_"+File.basename(m3u_name))
    out_m3u = File.new(opath+File.basename(m3u_name),'w+')
    prevline = ''
    m3us.each do |m3u_line|
      m3u = m3u_line.chomp # remove carriage return for file manip
      if m3u['#']
        prevline = m3u + "\n"
        next
      end
      if File.exist? m3u
#        puts prevline unless prevline.length == 0
#        puts m3u_line
        out_m3u &lt;&lt; prevline unless prevline.length == 0
        out_m3u &lt;&lt; m3u_line
        prevline = ''
      end

    end
    out_m3u.close
  end
end

opath = '/home/messel/Desktop/music/'

if (ARGV.size &gt; 0)
  check_for_file ARGV[0].to_s, opath
else
  Dir.glob('*.m3u').each do |m3u_name|
    check_for_file m3u_name, opath
  end
end</pre>
<p>But I wasn't very careful with my script, and used '\n' instead of "\n" (corrected above) which mean instead of line feeds (carriage returns for ancient typewriter folks like me) between description and file lines, I had ONE BIG MESS. After rolling my sleeves up and spelunking the dangerous caverns of regular expressions I came up with one final script to correct my woes. This script was appropriately labeled "oh_god_why.rb".</p>
<pre>require 'fileutils'
def check_for_file(m3u_name,opath)
  prune = false
  m3us = IO.readlines(m3u_name)
  out_m3u = File.new(opath+File.basename(m3u_name),'w+')
  m3us.each do |m3u_line|
    out_m3u &lt;&lt; m3u_line.gsub(/\n/,"\n")
  end
  out_m3u.close
end

opath = '/home/messel/Desktop/music/'

if (ARGV.size &gt; 0)
  check_for_file ARGV[0].to_s, opath
else
  Dir.glob('*.m3u').each do |m3u_name|
    check_for_file m3u_name, opath
  end
end</pre>
<p>Astute readers will notice that I've included several programs beyond the original 22 line script throughout this post. When it comes to doing jobs right, I believe a slight exaggeration goes a long way, but it's best to show your friends the full truth. <em><a href="http://www.youtube.com/watch?v=YWyCCJ6B2WE">"Pay no attention to the man behind the curtain"</a>.</em></p>
<p>references:</p>
<ul>
<li>Ruby <a href="http://ruby-doc.org/core/classes/Dir.html">Dir</a>, <a href="http://ruby-doc.org/core/classes/IO.html">IO</a>, <a href="http://ruby-doc.org/core/classes/File.html">File</a>, <a href="http://ruby-doc.org/core/classes/String.html">String</a></li>
</ul>
