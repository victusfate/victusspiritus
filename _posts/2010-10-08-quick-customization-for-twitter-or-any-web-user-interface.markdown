---
layout: post
status: publish
published: true
title: Quick Customization for Twitter or Any Web User Interface
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 5422
wordpress_url: http://www.victusspiritus.com/?p=5422
date: '2010-10-08 12:20:09 -0400'
date_gmt: '2010-10-08 19:20:09 -0400'
categories:
- Uncategorized
tags:
- Chrome
- design
- Stylish
- firefox
comments:
- id: 8001
  author: Connected Canvas, Adaptive Web Portals to Unlimited Information &raquo;
    Victus Spiritus
  author_email: ''
  author_url: http://victusfate.github.io/victusspiritus/uncategorized/2011/01/03/connected-canvas-adaptive-web-portals-to-unlimited-information/
  date: '2011-01-03 14:50:01 -0500'
  date_gmt: '2011-01-03 21:50:01 -0500'
  content: "[...] 2011  Mark Essel   TweetNot long back I wrote about malleable web
    surfaces and the browser plugin Stylish for customizing stylesheets. The example
    I shared was a retro modification of the twitter web UI with a larger content
    area and [...]"
---
<p><a href="{{ site.url }}/assets/2010/10/MarksTwitterWebUI.png"><img class="aligncenter size-full wp-image-5430" title="MarksTwitterWebUI" src="{{ site.url }}/assets/2010/10/MarksTwitterWebUI.png" alt="" width="500" height="420" /></a><br />
If you're tired of giving up half your browser window real estate to the greedy twitter web UI here's a nifty hack that puts you back in control of your local css.</p>
<p>First install the Stylish extension or plugin.</p>
<ul>
<li><span style="font-size: 13.3333px;">for <a href="https://chrome.google.com/extensions/detail/fjnbnpbmkenffdnngjfgmeleoegfcffe">Chrome/Chromium</a></span></li>
<li><span style="font-size: 13.3333px;">for <a href="https://addons.mozilla.org/en-US/firefox/addon/2108/">Firefox<br />
</a></span></li>
<p>(User Styles will show up on add-ons, haven't test this on firefox yet)</ul>
<p>For <a href="http://www.nystic.com/blog/?p=303">Safari users</a> here's a way to customize your css, and on <a href="http://my.opera.com/micahrayaills/blog/how-to-install-custom-user-style-sheets-in-opera-and-firefox">Opera you can leverage user scripts</a>.</p>
<p>*update* After installing the Stylish addon or greasemonkey scripts <a href="http://userstyles.org/styles/37615">here's a one click install for firefox users</a>.</p>
<p>Firefox friendly css code:</p>
<pre>
@-moz-document url-prefix('http://twitter.com/') {
	div.dashboard { max-width: 255px !important; 
          min-width: 230px !important}
	div.your-activity { float: none !important; 
          width: auto !important; }
	div.main-content { width: 780px !important; }
	div.latest-tweet .tweet-row { height: auto !important; 
          width: 200px !important; }
        div.dashboard .footer { font-size: 8px !important }
}
</pre>
<p>For Chrome/Chromium users you can grab this <a href="https://docs.google.com/leaf?id=0B_dN0hRq3gdgMjc1YjFhNTktZjVjMS00MGQ0LTk5ODItOTI0YmUxNjQzY2U3&amp;sort=name&amp;layout=list&amp;num=50">css snippet</a>:</p>
<pre>.main-content {
-moz-border-radius:5px 5px 5px 5px;
-moz-box-shadow:0 3px 4px #999999;
background:none repeat scroll 0 0 #FFFFFF;
display:inline-block;
float:left;
height:100%;
min-height:700px;
position:relative;
width:75%;
z-index:4;
}

.stream .new-tweets-bar {
-moz-border-radius:3px 3px 3px 3px;
background:none repeat scroll 0 0 #E3F1FA;
border:1px solid #C6E4F2;
cursor:pointer;
display:block;
font-size:13px;
margin:10px 15px;
padding:5px 1px;
text-align:center;
text-shadow:0 1px 0 #FFFFFF;
z-index:2;
}

#message-drawer .message .message-inside {
-moz-border-radius-bottomleft:3px;
-moz-border-radius-bottomright:3px;
background:none repeat scroll 0 0 #FFFFFF;
display:inline-block;
font-size:13px;
min-width:100px;
padding:8px 12px 8px 16px;
}

.dashboard{
min-width:100px;
max-width:auto;
width:20%;
position:relative;
padding:12px 20px;
overflow:hidden;
-webkit-border-top-right-radius:5px;
-moz-border-radius-topright:5px;
border-top-right-radius:5px;
}</pre>
<p>Finally in your plugin/extension Stylish options you'll add a new style. Mine's called twitter web. You paste the css above into the style box, and then change the Specify button to "URLs on the domain" and enter twitter.com. Save the change and reload your twitter.com page to see the results. You can tweak the css however you like by going back and forth and inspecting the twitter styles and adding your own customized views to the Stylish code block. This same method can be applied to any site.</p>
<p>Related Article:<br />
Designer get's a job at ZenDesk for sharp <a href="http://www.rodrigogalindez.com/archivos/realigning-the-new-twitter/">review of Twitter web UI</a>.</p>
