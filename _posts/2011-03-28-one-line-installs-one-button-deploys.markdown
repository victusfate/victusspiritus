---
layout: post
status: publish
published: true
title: One line installs, One button deploys
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8125
wordpress_url: http://www.victusspiritus.com/?p=8125
date: '2011-03-28 06:14:58 -0400'
date_gmt: '2011-03-28 13:14:58 -0400'
categories:
- Uncategorized
tags:
- web/tech
- coding
- mac os x
comments: []
---
<p><I>Without exaggeration single button deploys and one line installs have changed my dev life. Read on to find out why. I'll note a few of the configuration management tools I use on OS X and why I chose them towards the end of the post.</I></p>
<h2>preface</h2>
<p>Ever since I made the decision and effort to bring ideas to life through web apps, fortune has smiled upon my enthusiasm and placed generous allies along my way. It was only last year that I accepted that I'm on a life long journey, with no promise of a payoff beyond the satisfaction of the struggle. A sunk startup is a humbling and grounding experience, and I suggest everyone go through it exactly once ;).</p>
<p>When I was clueless how to begin development and irresistibly drawn to build my first web app, a good friend and partner materialized out of crossing real time updates, and showed me that I need to get my <a href="http://www.victusspiritus.com/2010/02/08/each-time-i-get-my-hands-dirty-i-learn/">hands dirty</a>. When I wanted to better understand distributed social networks, I was introduced to <a href="http://www.victusspiritus.com/2010/03/08/open-web-protocols-and-discussion-groups/">open social protocols</a> which transcend corporate silos. When I wanted to leverage and learn from social coding, I was pointed to <a href="http://www.victusspiritus.com/2010/02/09/gotta-grock-git/">git</a> and <a href="http://github.com/victusfate">github</a>. For endless questions about <a href="http://www.victusspiritus.com/2010/06/26/welcome-to-ruby-javascript-and-ubuntu-linux-ben/">development tool installation and configuration</a> I rely on personal blogs, web docs, and the community at <a href="http://stackoverflow.com/">StackOverflow</a>. The personal productivity boons that have minimized my dev iteration time and kept me sane in a world of endless options, are <i>one button deploys, and one line installation scripts</i>.</p>
<h2>One button deploys</h2>
<p>There's nothing that compares to <a href="http://heroku.com">Heroku's</a> ease of use and deployment ruby projects. From the homepage:</p>
<blockquote><p>
Create Heroku apps instantly:<br />
<code><br />
$ sudo gem install heroku $ heroku create sushi Created http://sushi.heroku.com/ git@heroku.com:sushi.git<br />
</code></p>
<p>Full deployment is simply a git push:<br />
<code><br />
$ git push heroku master -----> Heroku receiving push -----> Rails app detected -----> Launching..... done http://sushi.heroku.com deployed<br />
</code></p>
<p>Everything apps need and more, all manageable by API:<br />
<code><br />
$ heroku sharing:add fugu@sushi.com $ heroku domains:add sushi.com $ heroku rake db:migrate $ heroku db:push $ heroku addons:add memcache<br />
</code>
</p></blockquote>
<p>Deploying static pages to github is a simple one line deploy with <a href="http://pages.github.com/">github pages</a>. <i>Note to self, setup a landing page for victusfate.github.com.</I></p>
<p>EngineYard comes close for easy deploys with Ruby stacks and more flexibility after setting them up, but has a minimum monthly subscription (it cost us $70 a month). I've heard that Rackspace, Amazon, and several other hosts have developer friendly environments. I have a homework/side project to kick up a jruby/rails app on aws to see how it goes. </p>
<p>I have hands on experience deploying to the Google App Engine, which is fine for python or Java but slightly less friendly to JVM language stacks like JRuby or Scala due to a slow JVM warm up time. I'd really like to see one button/line deploys commoditized with a Freemium model and low to zero infrastructure switching costs.</p>
<h2>One line install scripts</h2>
<p>I have synchronized dev environments on my iMac desktop and Macbook Air. Dropbox and git keeps my code in synch, but I manually maintain development tools on both systems. The following utilities make my job much simpler. If you're developing on Linux you may use apt-get, debian packages, or yum. Since I primarily develop on OS X I rely on <a href="https://github.com/mxcl/homebrew">homebrew</a> as a general package tool, but have specific favorites for different languages/frameworks.</p>
<ul>
<li>For Ruby:<br />
I use <a href="http://rvm.beginrescueend.com/">rvm</a> as an incredible environment management tool. I shed a single tear after finding out rvm isn't available for my windows friends, but there are alternatives (<a href="https://github.com/vertiginous/pik">pik</a> or dedicated specific ruby loaded cmd shells). I can swap ruby interpreters or compilers with their associated gem sets on the fly. Speaking of which, gem is another amazing library utility which grabs required tools and dependencies on the fly. Bundler is a great gem packaging system which works just as well with the java virtual machine deploys on the google app engine, or tuned Badious Bamboo environments of </li>
<p></p>
<li>For node.js:<br />
The <a href="https://github.com/creationix/nvm">nvm</a> provides as a similar role as rvm. The <a href="http://npmjs.org/">npm</a> node package manager serves as a node utility tool like gem for Rubyists.</li>
<p></p>
<li>For python:<br />
I'm new to node and python but there are amazing packages that make them worth learning. I tried <a href="http://pypi.python.org/pypi/virtualenv">virtualenv</a> for isolated python environments and packages but prefer <a href="https://github.com/utahta/pythonbrew">pythonbrew</a> for it's similarity to rvm and nvm.</li>
</ul>
<p>If you have your own favorite configuration time saving hacks I'd love to hear about them in the comments.</p>
