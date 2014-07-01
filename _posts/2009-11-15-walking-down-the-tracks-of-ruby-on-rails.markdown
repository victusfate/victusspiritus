---
layout: post
status: publish
published: true
title: Walking down the tracks with Ruby on Rails
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
excerpt: "<a href=\"http://www.stuckincustoms.com\"><img class=\"aligncenter size-full
  wp-image-2101\" title=\"A Sea of Glass - The Chihuly Exhibit at the Ballagio in
  Vegas\" src=\"{{ site.url }}/assets/2009/11/DaleChihuliGlassSculptures.jpg\"
  alt=\"A Sea of Glass - The Chihuly Exhibit at the Ballagio in Vegas\" width=\"480\"
  height=\"340\" /></a>\r\n<em>this is a follow on post to <a href=\"http://victusfate.github.io/victusspiritus/uncategorized/2009/11/11/pigs-may-not-have-wings-but-i-can-ride-the-rails-with-a-flu/\">Pigs
  may not have wings, but I can Ride the Rails with a flu</a></em>\r\n<h1>Gems Gems
  Gems</h1>\r\nThe first barrier to entry to ramping up on RoR (Ruby on Rails) was
  setting up a build environment. I found several windows friendly developmet options.
  Netbeans has an install. Steel Ruby has a visual studio variant, Instant Ruby creates
  an environment you can drop rails projects into (instantly ;)), and Ruby Forge has
  an executable for windows machines. I opted for the <a href=\"http://victusfate.github.io/victusspiritus/uncategorized/2009/11/11/pigs-may-not-have-wings-but-i-can-ride-the-rails-with-a-flu/\">Ruby
  Forge windows exec </a> after trying the other routes to varying degrees of success.
  Primarily because it almost works (there's no shuffle! Array function on the RoR
  Ruby Forge version, or my environment still has problems), it's command line driven,
  and I know where the common install/gem folder is.\r\n\r\n"
wordpress_id: 2210
wordpress_url: http://www.victusspiritus.com/?p=2210
date: '2009-11-15 06:45:26 -0500'
date_gmt: '2009-11-15 13:45:26 -0500'
categories:
- Uncategorized
tags:
- web/tech
- software
- coding
- ruby
comments:
- id: 1806
  author: 'Practical Programming: Holding the Flow of Code in Mind'
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2009/11/22/practical-programming-holding-the-flow-of-code-in-mind/
  date: '2009-11-22 10:38:59 -0500'
  date_gmt: '2009-11-22 17:38:59 -0500'
  content: "[...] the case of web programming, Rails implements a MVC (model view
    control) design. The library functionality of ruby is based on compiled gems.
    You can zoom into the model [...]"
- id: 1835
  author: term paper
  author_email: gemmaflores82@yahoo.com
  author_url: http://www.superiorpapers.com/
  date: '2009-11-24 15:29:37 -0500'
  date_gmt: '2009-11-24 20:29:37 -0500'
  content: A term paper is a research paper written by students over an academic term
    or semester which accounts for a large amount of a grade and makes up much of
    the course. Term papers are generally intended to describe an event or concept
    or argue a point. A term paper is A written original work discussing a topic in
    detail, usually several typed pages in length and is often due at the end of a
    semester.<br>     There is much overlap between the terms "research paper" and
    "term paper". The phrase "term paper" was originally used to describe a paper
    (usually a research based paper) that was due at the end of the "term" - either
    a semester or quarter, depending on which unit of measure a school used. However,
    the term has fallen out of favor. Common usage has "term paper" and "research
    paper" as interchangeable, but this is not completely accurate. Not all term papers
    involve academic research, and not all research papers are term papers.
- id: 2500
  author: An Echo through Time, the Minimalist Trend &raquo; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2009/12/26/an-echo-through-time-the-minimalist-trend/
  date: '2010-01-05 13:22:45 -0500'
  date_gmt: '2010-01-05 20:22:45 -0500'
  content: "[...] of the user. Developers tend to isolate the view, controls, and
    data into different code sections (see more on MVC. This approach lends itself
    well to one where users are in charge of their interface, removing all [...]"
- id: 4617
  author: Welcome to Ruby, Javascript and Ubuntu Linux Ben | Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2010/06/26/welcome-to-ruby-javascript-and-ubuntu-linux-ben/
  date: '2010-06-26 06:05:48 -0400'
  date_gmt: '2010-06-26 13:05:48 -0400'
  content: "[...] Rails the most popular MVC framework for Ruby  http://rubyonrails.org/
    \ https://help.ubuntu.com/community/RubyOnRails back when I had windows: http://victusfate.github.io/victusspiritus/uncategorized/2009/11/15/walking-down-the-tracks-of-ruby-on-rails/
    [...]"
- id: 9828
  author: Cthulhu in Wonderland, Chihuly &mdash; Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/04/14/cthulhu-in-wonderland-chihuly/
  date: '2011-04-14 04:54:45 -0400'
  date_gmt: '2011-04-14 11:54:45 -0400'
  content: "[...] Cthulhu in Wonderland, Chihuly  April 14, 2011    TweetWhile visiting
    the Boston Museum of Fine Arts yesterday evening, my Michelle and I experienced
    first hand the surreal glass sculptures designed by Dale Chihuly. I unknowingly
    shared a picture of Dale&#8217;s work in 2009 while discussing Ruby and gems.
    That piece is at the Belagio in Las Vegas and is titled a Sea of Glass. [...]"
---
<p><a href="http://www.stuckincustoms.com"><img class="aligncenter size-full wp-image-2101" title="A Sea of Glass - The Chihuly Exhibit at the Ballagio in Vegas" src="{{ site.url }}/assets/2009/11/DaleChihuliGlassSculptures.jpg" alt="A Sea of Glass - The Chihuly Exhibit at the Ballagio in Vegas" width="480" height="340" /></a><br />
<em>this is a follow on post to <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/11/11/pigs-may-not-have-wings-but-i-can-ride-the-rails-with-a-flu/">Pigs may not have wings, but I can Ride the Rails with a flu</a></em></p>
<h1>Gems Gems Gems</h1>
<p>The first barrier to entry to ramping up on RoR (Ruby on Rails) was setting up a build environment. I found several windows friendly developmet options. Netbeans has an install. Steel Ruby has a visual studio variant, Instant Ruby creates an environment you can drop rails projects into (instantly ;)), and Ruby Forge has an executable for windows machines. I opted for the <a href="http://victusfate.github.io/victusspiritus/uncategorized/2009/11/11/pigs-may-not-have-wings-but-i-can-ride-the-rails-with-a-flu/">Ruby Forge windows exec </a> after trying the other routes to varying degrees of success. Primarily because it almost works (there's no shuffle! Array function on the RoR Ruby Forge version, or my environment still has problems), it's command line driven, and I know where the common install/gem folder is.</p>
<p><a id="more"></a><a id="more-2210"></a></p>
<p>Let me warn potential windows RoR coders that while all of these options may work to varying degrees, if your ultimate server destination is Linux Apache, you may save a lot of headaches by setting up a dual boot Ubuntu installation (today's plan for me). After running into the bug with shuffle! and spending time finding and understanding it, your very limited learning and development time would be better served by avoiding the additional complications introduced with a different OS. Keep in mind I had a much more learned co-pilot helping me along in understanding using <a href="https://www.acrobat.com/#/connectnow/ConnectNowBegin">Adobe Connect</a>.</p>
<h1>Darn GEMS!</h1>
<p>There are inconsistencies in gem names, versus the gem packages. This is to avoid name conflicts because gems sit in repositories on public facing web servers. I also found several close variants of gem names that have subtle implementation differences. One of the pitfalls I fell into was in assuming I had to call rake, and pass all our unit tests. It turns out I assumed wrong. In the race to develop something that is valuable to users, we have opted to skip some of the long term habits Rails nudges us towards (I'm sure as time allows we'll find our way to testing). So the tests weren't setup quite right for our specific project (they were using sqlite a default database for rails while we use <a href="http://www.avc.com/a_vc/2009/02/mongo-db.html">MongoDB</a>, a new NonSQL database option).</p>
<h1>MVC Directory Structure First Timer</h1>
<p><a href="http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller">MVC</a> stands for:</p>
<ul>
<li><span style="background-color: #ffffff;">model (data and it's handling)</span></li>
<li><span style="background-color: #ffffff;">view (how we see it an other intermediate stuff), and</span></li>
<li><span style="background-color: #ffffff;">control (algorithms, processing, application flow , the CPU of RoR?).</span></li>
</ul>
<p>When you first construct a bare bones Rails app (rails hello) , the folder structure looks something like this:<br />
C:\Users\Dude Jones\Desktop\My Dropbox\Mystuff\people&gt;tree<br />
C:.<br />
├───app<br />
│   ├───controllers<br />
│   ├───helpers<br />
│   ├───models<br />
│   └───views<br />
│       ├───layouts<br />
│       └───people<br />
├───config<br />
│   ├───environments<br />
│   ├───initializers<br />
│   └───locales<br />
├───db<br />
│   └───migrate<br />
├───doc<br />
├───lib<br />
│   └───tasks<br />
├───log<br />
├───nbproject<br />
│   └───private<br />
├───public<br />
│   ├───images<br />
│   ├───javascripts<br />
│   └───stylesheets<br />
├───script<br />
│   └───performance<br />
├───test<br />
│   ├───fixtures<br />
│   ├───functional<br />
│   ├───integration<br />
│   ├───performance<br />
│   └───unit<br />
│       └───helpers<br />
├───tmp<br />
│   ├───cache<br />
│   ├───pids<br />
│   ├───sessions<br />
│   └───sockets<br />
└───vendor<br />
└───plugins</p>
<p>Here's that same structure with files<br />
C:\Users\Dude Jones\Desktop\My Dropbox\Mystuff\people&gt;tree /f<br />
C:.<br />
│   Rakefile<br />
│   README<br />
│<br />
├───app<br />
│   ├───controllers<br />
│   │       application_controller.rb<br />
│   │       people_controller.rb<br />
│   │<br />
│   ├───helpers<br />
│   │       application_helper.rb<br />
│   │       people_helper.rb<br />
│   │<br />
│   ├───models<br />
│   │       person.rb<br />
│   │<br />
│   └───views<br />
│       ├───layouts<br />
│       │       people.html.erb<br />
│       │<br />
│       └───people<br />
│               edit.html.erb<br />
│               index.html.erb<br />
│               new.html.erb<br />
│               show.html.erb<br />
│<br />
├───config<br />
│   │   boot.rb<br />
│   │   database.yml<br />
│   │   environment.rb<br />
│   │   routes.rb<br />
│   │<br />
│   ├───environments<br />
│   │       development.rb<br />
│   │       production.rb<br />
│   │       test.rb<br />
│   │<br />
│   ├───initializers<br />
│   │       backtrace_silencers.rb<br />
│   │       inflections.rb<br />
│   │       mime_types.rb<br />
│   │       new_rails_defaults.rb<br />
│   │       session_store.rb<br />
│   │<br />
│   └───locales<br />
│           en.yml<br />
│<br />
├───db<br />
│   │   development.sqlite3<br />
│   │   schema.rb<br />
│   │   seeds.rb<br />
│   │   test.sqlite3<br />
│   │<br />
│   └───migrate<br />
│           20091111235941_create_people.rb<br />
│<br />
├───doc<br />
│       README_FOR_APP<br />
│<br />
├───lib<br />
│   └───tasks<br />
├───log<br />
│       development.log<br />
│       production.log<br />
│       server.log<br />
│       test.log<br />
│<br />
├───nbproject<br />
│   │   project.properties<br />
│   │   project.xml<br />
│   │<br />
│   └───private<br />
│           private.properties<br />
│           rake-d.txt<br />
│<br />
├───public<br />
│   │   404.html<br />
│   │   422.html<br />
│   │   500.html<br />
│   │   favicon.ico<br />
│   │   robots.txt<br />
│   │<br />
│   ├───images<br />
│   │       rails.png<br />
│   │<br />
│   ├───javascripts<br />
│   │       application.js<br />
│   │       controls.js<br />
│   │       dragdrop.js<br />
│   │       effects.js<br />
│   │       prototype.js<br />
│   │<br />
│   └───stylesheets<br />
│           scaffold.css<br />
│<br />
├───script<br />
│   │   about<br />
│   │   console<br />
│   │   dbconsole<br />
│   │   destroy<br />
│   │   generate<br />
│   │   plugin<br />
│   │   runner<br />
│   │   server<br />
│   │<br />
│   └───performance<br />
│           benchmarker<br />
│           profiler<br />
│<br />
├───test<br />
│   │   test_helper.rb<br />
│   │<br />
│   ├───fixtures<br />
│   │       people.yml<br />
│   │<br />
│   ├───functional<br />
│   │       people_controller_test.rb<br />
│   │<br />
│   ├───integration<br />
│   ├───performance<br />
│   │       browsing_test.rb<br />
│   │<br />
│   └───unit<br />
│       │   person_test.rb<br />
│       │<br />
│       └───helpers<br />
│               people_helper_test.rb<br />
│<br />
├───tmp<br />
│   ├───cache<br />
│   ├───pids<br />
│   ├───sessions<br />
│   └───sockets<br />
└───vendor<br />
└───plugins</p>
<p>There are scripts that will populate subdirectories with ruby files. One that adds to the application, model and view folders at once is scaffold.<br />
It looks like this on a windows prompt:</p>
<p>ruby script/generate scaffold person name:string password:string email:string age:integer</p>
<p>It creates several files of which I believe a few are key after <a href="http://guides.rubyonrails.org/getting_started.html#the-mvc-architecture">reading some of getting started</a> (I prefer to learn by doing, then going back to understand what I did worked or broke and why):</p>
<ul>
<li><span style="background-color: #ffffff;">The model support file is the Rails migration db/migrate/20091111235941_create_people.rb</span></li>
<li><span style="background-color: #ffffff;">a model in app/models/person.rb</span></li>
<li><span style="background-color: #ffffff;">a controller app/controller/people_controller.rb</span></li>
</ul>
<p>The scaffold script also generates several tests (look for person/people above, a helper).</p>
<h1>IDE</h1>
<p>I used <a href="http://netbeans.org/kb/trails/ruby.html">Netbeans</a>, <a href="http://www.eclips3media.com/workshop/2007/08/using-visual-studio-as-a-ruby-on-rails-ide/">Visual Studio</a>, and for editing Notepad and <a href="http://www.scintilla.org/SciTE.html">ScITE</a>. Of all of these, I think I prefer Visual Studio the best for speed, style and responsiveness, but Netbeans is a good backup integrated development platform. ScITE was handy for quick editing though. I ran the server off of the console so I can see what messages (errors) it was printing out, instead of constantly have to reopen the log file. I suspect you will become quite intimate with log/development.log as you experience building your own Rails projects.</p>
<p>Check out what we're up to at <a href="http://victusmedia.com/">Victus Media</a>, a cool dev build should be going live this week for <a href="http://victus1.victusmedia.com">Intelligent Advertising Media</a>.</p>
<p>Don't forget this handy <a href="http://spreadsheets.google.com/ccc?key=0AvdN0hRq3gdgdEM4dDhETFRONHZtaFFBWS1OY25OYkE&amp;hl=en">Google Doc</a> I started for diving into Ruby on Rails.</p>
<p>[iframe http://spreadsheets.google.com/pub?key=tC8t8DLTN4vmhQAY-NcnNbA&amp;output=html 480 600]</p>
