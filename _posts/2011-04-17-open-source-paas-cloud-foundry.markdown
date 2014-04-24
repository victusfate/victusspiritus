---
layout: post
status: publish
published: true
title: Open Source PaaS Cloud Foundry
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8484
wordpress_url: http://www.victusspiritus.com/?p=8484
date: '2011-04-17 12:05:47 -0400'
date_gmt: '2011-04-17 19:05:47 -0400'
categories:
- Uncategorized
tags:
- web/tech
- coding
comments: []
---
<p>It's possible the buzzword density broke my <em>discerning</em> application taste filter, but a roll your own platform as a service is definitely worth trying on for size. The dream is to have a a platform that can perform like Wordpress.org, but instead of serving bloggers it's an open source Heroku like stack. Ideally I could deploy this platform on any ubuntu host and begin serving apps immediately. </p>
<p>I decided to try out the PaaS after my weekends and evenings are freed up in May. I started of by <em>loosely</em> following (trying 10.10 the latest release) the <a href="https://github.com/cloudfoundry/vcap/blob/master/README.rdoc">installation instructions</a>.</p>
<h2>Getting started</h2>
<p>I downloaded and installed Virtual Box for Mac OS X a few weeks ago. In addition I downloaded the Ubuntu 10.10 32bit and 64bit iso images. Ubuntu 64 installed without a hitch, and I found a <a href="http://helpdeskgeek.com/linux-tips/install-virtualbox-guest-additions-in-ubuntu/">handy site</a> which suggested I install guest additions for a full display virtual machine. After a little customizing my installation was humming along like my old Ubuntu desktop.</p>
<p>If you'd like to try out the PaaS, I've included the notes linked to in the installation instructions above.</p>
<blockquote>
<h2>Installation Notes</h2>
<p>
Cloud Foundry is made up of a number of system components (cloud controller, health manager, dea, router, etc.). These components can run co-located in a single vm/single os or can be spread across several machines/vm’s.</p>
<p>
For development purposes, the preferred environment is to run all of the core components within a single vm and then interact with the system from outside of the vm via an ssh tunnel. The pre-defined domain *.vcap.me maps to local host, so when you use this setup, the end result is that your<br />
development environment is available at <a href="http://api.vcap.me">api.vcap.me</a>.</p>
<p>
For large scale or multi-vm deployments, the system is flexible enough to allow you to place system components on multiple vm’s, run multiple nodes of a given type (e.g., 8 routers, 4 cloud controllers, etc.)</p>
<p>
The detailed install instructions below walk you through the install process for a single vm installation.</p>
<p>
Versions of these instructions have been used for production deployments, and for our own development purposes. many of us develop on mac laptops, so some additional instructions for this environment have been included.</p>
<h2>Detailed Install/Run Instructions:</h2>
<ul>
<li>step #-1:
<pre> 
  - setup a VM with a pristine Ubuntu 10.04.2 server 64bit image,
    (http://www.ubuntu.com/business/get-ubuntu/download)
  - you may wish to snapshot your VM now in case things go pear shaped.
  - great snapshot spots are here and after step #4
  - to enable remote access (more fun than using the console), install ssh.
 
   sudo apt-get install openssh-server
</pre>
</li>
<li>step #0, install system and rvm dependencies
<pre> 
  sudo apt-get install autoconf curl git-core ruby bison build-essential zlib1g-dev libssl-dev libreadline5-dev
</pre>
</li>
<li>step #1, install rvm
<pre> 
  #for detailed rvm install instructions see: [https://rvm.beginrescueend.com/rvm/install/]
  #or follow the quick steps below.
 
  #grab rvm
  #note, he -k switch is only needed if the certificate validation fails
  bash < <(curl -s -k -B https://rvm.beginrescueend.com/install/rvm)
 
  #follow the instructions given by the RVM installer (a copy is
  #include below for your convenience).
 
  # you must complete the install by loading RVM in new shells.
  #
  #
  #  1) Place the folowing line at the end of your shell's loading files
  #     (.bashrc or .bash_profile for bash and .zshrc for zsh),
  #     after all PATH/variable settings:
  #
  #     # This loads RVM into a shell session.
  #     [[ -s \"$rvm_path/scripts/rvm\" ]] && source \"$rvm_path/scripts/rvm\"
  #
  #     You only need to add this line the first time you install rvm.
  #
  #  2) Ensure that there is no 'return' from inside the ~/.bashrc file,
  #     otherwise rvm may be prevented from working properly.
  #
  #     This means that if you see something like:
  #
  #    '[ -z \"\$PS1\" ] && return'
  #
  #  then you change this line to:
  #
  #  if [[ -n \"\$PS1\" ]] ; then
  #
  #    # ... original content that was below the '&& return' line ...
  #
  #  fi # <= be sure to close the if at the end of the .bashrc.
  #
  #    # this is a good place to source rvm
  #         [[ -s \"$rvm_path/scripts/rvm\" ]] && source \"$rvm_path/scripts/rvm\"
  #
  #   <EOF> - this marks the end of the .bashrc
  #
  #     Be absolutely *sure* to REMOVE the '&& return'.
  #
  #     If you wish to DRY up your config you can 'source ~/.bashrc' at the
  #     bottom of your .bash_profile.
  #
  #     Placing all non-interactive (non login) items in the .bashrc,
  #     including the 'source' line above and any environment settings.
  #
  #  3) CLOSE THIS SHELL and open a new one in order to use rvm.
</pre>
</li>
<li>step #2, use rvm to install ruby 1.9.2 and make it default
<pre> 
  rvm install 1.9.2-p180
  rvm --default 1.9.2-p180
</pre>
</li>
<li>step #3, use rvm to install ruby 1.8.7
<pre> 
  rvm install 1.8.7
</pre>
</li>
<li>step #4, clone the vcap and vmc repos:
<pre> 
  mkdir ~/cloudfoundry; cd ~/cloudfoundry
  # optionally create new ssh keys and add them to your github account: ssh-keygen -t rsa -C markl@vmware.com
  # note, this release uses a handful of submodules. its important
  # to understand the impact of this which is:
  # 1) after clonding the vcap repo, you must run git submodule update --init
  #    this ends up mounting the services and tests repos in the directory tree of vcap
  #
  # 2) any time you git pull in vcap, you must also git submodule update
  git clone https://github.com/cloudfoundry/vcap.git
 
  # note, there should be a .rvmrc file in vcap/rvmrc
  # make sure that the vcap/.rvmrc is present and that it contains
  # rvm use 1.9.2
  cd ~/cloudfoundry/vcap
  git submodule update --init
  gem install vmc --no-rdoc --no-ri
</pre>
</li>
<li>step #5, run vcap_setup to prep cloudfoundry for launch
<pre> 
  # Points to keep in mind.
  # 1) Answer Y to all questions
  # 2) Remember your mysql password, you will need it in a minute
  cd ~/cloudfoundry/vcap
  sudo setup/vcap_setup
 
  # after vcap_setup completes, edit your mysql_node config file
  # with the correct password created during install
  cd ~/cloudfoundry/vcap/services/mysql/config
  vi mysql_node.yml and change mysql.pass to your password
</pre>
</li>
<li>step #6, restart nginx with a custom config
<pre> 
  cd ~/cloudfoundry/vcap
  sudo cp setup/simple.nginx.conf /etc/nginx/nginx.conf
  sudo /etc/init.d/nginx restart
</pre>
</li>
<li>step #7, install bundler gem and run bundler:install
<pre> 
  cd ~/cloudfoundry/vcap
  gem install bundler --no-rdoc --no-ri
  rake bundler:install
</pre>
</li>
<li>step #8, start the system
<pre> 
  cd ~/cloudfoundry/vcap
  bin/vcap start
  bin/vcap tail  # see aggregate logs
</pre>
</li>
<li>step #9 *Optional, mac users only*, create a local ssh tunnel # from your<br />
vm, run ifconfig and note eth0, possiby 192.168.252.130 # go to your mac<br />
terminal window and create a local port 80 tunnel as # once you do this,<br />
from both your mac, and from within the vm, api.vcap.me and *.vcap.me # map<br />
to localhost which maps to your running cloudfoundry instance sudo ssh -L<br />
80:192.168.252.130:80 mhl@192.168.252.130 -N</p>
</li>
</ul>
<h3>Trying your setup</h3>
<ul>
<li>step #10, validate that you can connect and tests pass # from the console<br />
of your vm, or from your mac (thanks to local tunnel)</p>
<p>
#try vmc target api.vcap.me vmc info</p>
<p>
#it should produce roughly the following…</p>
<p>
VMware’s Cloud Application Platform For support visit<br />
support@cloudfoundry.com</p>
<p>
Target: <a href="http://api.vcap.me">api.vcap.me</a> (v0.999) Client:<br />
v0.3.10</p>
<p>
#play around as a user, start with vmc register —email foo@bar.com<br />
—passwd password vmc login —email foo@bar.com —passwd<br />
password</p>
<p>
#to see what else you can do try vmc help</p>
</li>
</ul>
<h2>Testing your setup</h2>
<p>
#Once the system is installed, you can run the following command Basic<br />
System #Validation Tests (BVT) to ensure that major functionality is<br />
working. cd cloudfoundry/vcap cd tests && bundle package; bundle<br />
install && cd .. rake tests</p>
<p>
# unit tests can also be run using the following. cd cloudcontroller rake<br />
spec cd ../dea rake spec cd ../router rake spec cd ../health_manager rake<br />
spec</p>
<p>
-step #11, you are done, make sure you can run a simple hello world app.</p>
<pre> 
  #1) create an empty directory for your test app (lets call it env), and enter it.
  cd env
 
  #2) cut and paste the following app into a ruby file (lets say env.rb)
  vi env.rb
 
  ==== cut ===
</pre>
<p>
require ‘rubygems’ require ‘sinatra’</p>
<p>
get ’/’ do</p>
<pre> 
  host = ENV['VMC_APP_HOST']
  port = ENV['VMC_APP_PORT']
  "<h1>XXXXX Hello from the Cloud! via: #{host}:#{port}</h1>"
</pre>
<p>
end</p>
<p>
get ’/env’ do</p>
<pre> 
  res = ''
  ENV.each do |k, v|
    res << "#{k}: #{v}<br/>"
  end
  res
</pre>
<p>
end</p>
</blockquote>
<p>Links</p>
<ol>
<li><a href="http://cloudfoundry.com/">Cloud Foundry</a></li>
<li><a href="https://github.com/cloudfoundry/vcap">vcap Cloud Foundry on github</a></li>
</ol>
