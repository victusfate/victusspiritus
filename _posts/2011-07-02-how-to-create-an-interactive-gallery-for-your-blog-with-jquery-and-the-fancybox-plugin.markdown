---
layout: post
status: publish
published: true
title: How to create an interactive gallery for your blog with jquery and the fancybox
  plugin
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9544
wordpress_url: http://www.victusspiritus.com/?p=9544
date: '2011-07-02 03:19:05 -0400'
date_gmt: '2011-07-02 10:19:05 -0400'
categories:
- Uncategorized
tags:
- javascript
- design
- html5
comments: []
---
<p>Yesterday I was inspired to create a short montage of <a href="http://victusfate.github.io/victusspiritus/uncategorized/2011/07/01/the-ocean/">ocean and beach</a> related photos to accompany a SoundCloud recording I made while strolling the shore. The built in Wordpress gallery is fairly limited, but in May I discovered the cycle jquery plugin for a photo sharing post. While the on page script worked at the time, it has since run into issues so I've been looking for an alternative. I found a nifty interactive image browser called Fancybox a few weeks back, and this post describes how you can incorporate it's functionality into your own blog or site.</p>
<h2>The Markup</h2>
<p>The html markup is straight forward, and the important bits are href's to the zoomed in photo, and 150x150 or small photos for the gallery. The entire set is aggregated in a ul element or unordered list for css child properties that we'll look at in a moment.<br />
<script src="https://gist.github.com/1059891.js?file=gallery.html"></script></p>
<h2>Style and Script</h2>
<p>At the top of the reference scripts is jquery, followed by the required mousewheel, and fancybox scripts which I entered into gists on github. The astute reader may notice that the jquery fancybox css is referenced in my media upload directory. It was just easier using Wordpress to upload the file than Hostmonster's file manager.<br />
<script src="https://gist.github.com/1059891.js?file=style_and_script.html"></script></p>
<h2>Text Control Plugin</h2>
<p>I had one remaining issue of Wordpress putting &lt;	p&gt; &lt;/p&gt;, and &lt;br /&gt;  tags in the post. The <a href="http://wordpress.org/extend/plugins/text-control/">Text Control</a> plugin makes the post editable by informing Wordpress not to enter any format or character encoding.</p>
<h2>Sample Gallery</h2>
<p>Here's what a gallery looks like. It's easy to customize the css on the images to adjust their size or layout.</p>
<div style="border:outset; width:650px; height:440px; background-color:#A7E5FF; position:relative;">
<ul class="polaroids">
<li><a rel="example_group" href="{{ site.url }}/assets/2011/07/IMG_3348.jpg" title="walking north"><img alt="" src="{{ site.url }}/assets/2011/07/IMG_3348-150x150.jpg" title="walking north" /></a></li>
<li><a rel="example_group" href="{{ site.url }}/assets/2011/07/IMG_3349.jpg" title="waves creeping up"><img alt="" src="{{ site.url }}/assets/2011/07/IMG_3349-150x150.jpg" title="waves creeping up"/></a></li>
<li><a rel="example_group" href="{{ site.url }}/assets/2011/07/IMG_3350.jpg" title="dark to light blue sky"><img alt="" src="{{ site.url }}/assets/2011/07/IMG_3350-150x150.jpg"  title="dark to light blue sky"/></a></li>
<li><a rel="example_group" href="{{ site.url }}/assets/2011/07/IMG_3351.jpg" title="dunes"><img alt="" src="{{ site.url }}/assets/2011/07/IMG_3351-150x150.jpg" title="dunes"/></a></li>
<li><a rel="example_group" href="{{ site.url }}/assets/2011/07/IMG_3352.jpg" title="crashing waves"><img alt="" src="{{ site.url }}/assets/2011/07/IMG_3352-150x150.jpg" title="crashing waves" /></a></li>
</ul>
<h2 style="color:blue; text-align:center; position:absolute; margin-left: 70px; bottom:0px;">Image gallery (click and scroll with mouse wheel or tap)</h2>
</div>
<h2>References</h2>
<ul>
<li><a href="http://fancybox.net/">Fancybox</a></li>
<li><a href="http://www.zurb.com/playground/css3-polaroids">Polaroid with CSS</a></li>
</ul>
<p><script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.6.1/jquery.min.js"></script><br />
<script type="text/javascript" src="https://raw.github.com/gist/1058744/cb66588e29c237d80f5a944c7f0d47bc97dd9a39/jquery.mousewheel-3.0.4.pack.js"></script><br />
<script type="text/javascript" src="https://raw.github.com/gist/1058744/1373ed0838bc1be6841339fef703a07c1ee7267f/jquery.fancybox-1.3.4.pack.js"></script></p>
<link rel="stylesheet" type="text/css" href="{{ site.url }}/assets/2011/07/jquery.fancybox-1.3.4_mine.css" media="screen" />
<style>
a img {<br />
	border: 1px solid #BBB;<br />
	padding: 2px;<br />
	margin: 10px 20px 10px 0;<br />
	vertical-align: top;<br />
}</p>
<p>a img.last {<br />
	margin-right: 0;<br />
}</p>
<p>.polaroid_box {<br />
	margin:20px 0 0px 25px;<br />
}</p>
<p>ul.polaroids {<br />
	width: 95%;<br />
	margin: 0px 0px 18px 0px;<br />
	float: left;<br />
	list-style: none;<br />
	padding: 20px;<br />
}<br />
.polaroids li {<br />
	display: inline;<br />
}<br />
.polaroids a {<br />
	background: #fff;<br />
	display: inline;<br />
	float: left;<br />
	margin: 0 0 0px 20px;<br />
	width: auto;<br />
	padding: 10px 10px 5px;<br />
	text-align: center;<br />
	font-family: "Marker Felt", sans-serif;<br />
	text-decoration: none;<br />
	color: #333;<br />
	font-size: 16px;<br />
	-webkit-box-shadow: 0 3px 6px rgba(0,0,0,.25);<br />
	-moz-box-shadow: 0 3px 6px rgba(0,0,0,.25);<br />
	-webkit-transform: rotate(-2deg);<br />
	-webkit-transition: -webkit-transform .15s linear;<br />
	-moz-transform: rotate(-2deg);<br />
}<br />
.polaroids img {<br />
	display: block;<br />
	height: 120px;<br />
	width: 120px;<br />
	margin-bottom: 12px;<br />
}<br />
.polaroids img.small {<br />
	height: 100px;<br />
	width: 100px;<br />
}</p>
<p>.polaroids a:after {<br />
	content: attr(title);<br />
}</p>
<p>.polaroids li:nth-child(even) a {<br />
	-webkit-transform: rotate(2deg);<br />
	-moz-transform: rotate(2deg);<br />
}<br />
.polaroids li:nth-child(3n) a {<br />
	-webkit-transform: none;<br />
	position: relative;<br />
	top: -5px;<br />
	-moz-transform: none;<br />
}<br />
.polaroids li:nth-child(5n) a {<br />
	-webkit-transform: rotate(5deg);<br />
	position: relative;<br />
	right: 5px;<br />
	-moz-transform: rotate(5deg);<br />
}<br />
.polaroids li:nth-child(8n) a {<br />
	position: relative;<br />
	right: 5px;<br />
	top: 8px;<br />
}<br />
.polaroids li:nth-child(11n) a {<br />
	position: relative;<br />
	left: -5px;<br />
	top: 3px;<br />
}</p>
<p>.polaroids li a:hover,<br />
.polaroids a:hover {<br />
	-webkit-transform: scale(1.25);<br />
	-moz-transform: scale(1.25);<br />
	-webkit-box-shadow: 0 3px 6px rgba(0,0,0,.5);<br />
	-moz-box-shadow: 0 3px 6px rgba(0,0,0,.5);<br />
	position: relative;<br />
	z-index: 5;<br />
}</p>
</style>
<p><script type='text/javascript'><br />
	$("a[rel=example_group]").fancybox({<br />
		'transitionIn'		: 'none',<br />
		'transitionOut'		: 'none',<br />
		'titlePosition' 	: 'over',<br />
		'titleFormat'		: function(title, currentArray, currentIndex, currentOpts) {<br />
			return '<span id="fancybox-title-over">Image ' + (currentIndex + 1) + ' / ' + currentArray.length + (title.length ? ' &nbsp; ' + title : '') + '</span>';<br />
		}<br />
	});<br />
</script></p>
