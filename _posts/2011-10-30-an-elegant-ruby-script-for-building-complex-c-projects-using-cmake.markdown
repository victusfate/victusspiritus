---
layout: post
status: publish
published: true
title: An elegant ruby script for building complex c++ projects, using cmake
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9903
wordpress_url: http://www.victusspiritus.com/?p=9903
date: '2011-10-30 16:20:54 -0400'
date_gmt: '2011-10-30 23:20:54 -0400'
categories:
- Uncategorized
tags:
- coding
- ruby
- c++
comments: []
---
<p><i>Disclaimer: As a blogger I leverage the creative license to call solutions elegant, although in reality they may be far from it. Descriptive veracity is up to each reader.</i></p>
<p>"I'm mostly blogging this for my own future use, to be able to find how to do something I remember doing before. There you go, future me."</p>
<p>A friend and fellow blogger Denny Gentry reminded me of the <a href="http://codingrelic.geekhold.com/2011/10/tornado-httpclient-chunked-downloads.html">value of helping out my future self</a> by capturing a handy piece of code within a blog post.</p>
<p>Last week I had to back port a fairly complex project from Visual Studio 10 to Visual Studio 9. Microsoft likely has some tools laying around to achieve this, but I'm often tasked with rapidly moving our projects over to linux or other operating systems, and I decided to write a short script to solve the problem of cross platform project building once and for all. </p>
<p>All that's needed now are cmake, a ruby interpreter, and two lists of files. One list is for libraries (order matters, last dependency last) and another for executables. One caveat is that if the system you're ultimately moving too doesn't have cmake you may need to delete any project dependencies on CMakeLists.txt in the created project (I had to). By default cmake watches for changes to this file and remakes project files, which will lead to build errors without cmake's installation.</p>
<p><a href="https://github.com/victusfate/create_cmake"><br />
<h2>create_cmake.rb</h2>
<p></a></p>
<p><a href="https://github.com/victusfate/create_cmake">create_cmake</a> is a simple ruby script and sample lib which takes a list of libraries (with paths) and executables and generates a CMakeLists.txt file. The CMakeLists.txt file will generate build files on many platforms include linux, os x, and windows in the form of makefiles and visual studio solutions. See <a href="http://www.cmake.org/">cmake.org</a> for all supported build systems.</p>
<h2>The create_cmake.rb script</h2>
<p><script src="https://gist.github.com/1316698.js?file=create_cmake.rb"></script></p>
<h2>With sample inputs:</h2>
<p>library list:</p>
<pre><code>
  one_lib
  another/lib
  third_lib
</code></pre>
<p>exec list:</p>
<pre><code>
  test/test.cpp
</code></pre>
<p>In this example to generate the CMakeLists.txt file first a lib.list and an exec.list are needed. See the included repo files for examples of formats (file lists where order matters, put your latest dependency last on the lib list).</p>
<p>In the project directory run:</p>
<pre><code>ruby create_cmake.rb lib.list exec.list test &gt; CMakeLists.txt
</code></pre>
<p>Then from the project root type</p>
<pre><code>cd build
cmake ..
</code></pre>
<p>And cmake will determine a default build system for your architecture. </p>
<p>You may specify targeted builds by typing:</p>
<pre><code>
    cmake
</code></pre>
<p>This yields a listing of supported platforms. Here's an example of what showed up on my home system:</p>
<pre>
The following generators are available on this platform:

    Unix Makefiles              = Generates standard UNIX makefiles.
    Xcode                       = Generate XCode project files.
    CodeBlocks - Unix Makefiles = Generates CodeBlocks project files.
    Eclipse CDT4 - Unix Makefiles = Generates Eclipse CDT 4.0 project files.
    KDevelop3                   = Generates KDevelop 3 project files.
    KDevelop3 - Unix Makefiles  = Generates KDevelop 3 project files.
</pre>
<p>To create an Xcode project enter:</p>
<pre><code>cmake -G Xcode (path to CMakeLists.txt file)
</code></pre>
