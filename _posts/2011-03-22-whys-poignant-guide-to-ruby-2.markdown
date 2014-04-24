---
layout: post
status: publish
published: true
title: Why's Poignant Guide to Ruby
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 8031
wordpress_url: http://www.victusspiritus.com/?p=8031
date: '2011-03-22 07:38:36 -0400'
date_gmt: '2011-03-22 14:38:36 -0400'
categories:
- Uncategorized
tags:
- far out
- coding
- ruby
comments: []
---
<link href="http://ajax.googleapis.com/ajax/libs/jqueryui/1.8/themes/base/jquery-ui.css" rel="stylesheet" type="text/css"/>
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.5.1/jquery.min.js"></script><br />
		<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.10/jquery-ui.min.js"></script></p>
<p>	<script type="text/javascript"><br />
		$(document).ready(function() {<br />
                    $('div.entry').css('overflow','visible');<br />
		    SetupGrowingDivs();<br />
		});<br />
		function SetupGrowingDivs() {<br />
			    var scale = 1.5;<br />
                            $('div.front').css('overflow','visible');<br />
			    $('div.front').find('img').live({<br />
			        mouseover: function() {<br />
			            $(this).css('z-index', '5');<br />
			            $(this).css('overflow', 'visible')<br />
			            var old_width = parseInt($(this).css('width'));<br />
			            var old_height = parseInt($(this).css('height'));<br />
			            $(this).stop().animate({<br />
			                width: old_width * scale,<br />
			                height: old_height * scale,<br />
			                left: 0,<br />
			                top: 0,<br />
			            },<br />
			            200);<br />
			        },<br />
			        mouseleave: function() {<br />
				    var old_width = parseInt($(this).css('width'));<br />
    				    var old_height = parseInt($(this).css('height'));<br />
			            $(this).stop().animate({<br />
			                width: old_width / scale,<br />
			                height: old_height / scale,<br />
			                left: 0,<br />
			                top: 0<br />
			            },<br />
			            200);<br />
			            $(this).css('overflow', 'hidden')<br />
			            $(this).css('z-index', '1');<br />
			        }<br />
			    });<br />
		}<br />
</script></p>
<div class="front">
<p style="text-align: center;"><a href="http://www.victusspiritus.com/wp-content/uploads/2011/03/whys-poignant-guide-to-ruby.pdf"><img class="aligncenter size-full wp-image-8019" title="whys_poignant_guide_to_ruby_cover" src="http://www.victusspiritus.com/wp-content/uploads/2011/03/whys_poignant_guide_to_ruby_cover.png" alt="" width="505" height="709" /></a></p>
</div>
<p>It's been sitting there staring at me with its cold damning eyes for several months. Most books have a way of becoming invisible after I've skimmed a few chapters and moved on, but not this one. At a quiet moment this morning, as I scanned empty tech news posts, I imagined the faint whispers of my ebook collection. Among them a single shiny voice stands out. </p>
<p><b>Why should you read Why's Poignant Guide to Ruby?</b></p>
<div class="front">
<a href="http://www.victusspiritus.com/wp-content/uploads/2011/03/why_read_whys_poignant_guide_to_ruby.png"><img class="aligncenter size-full wp-image-8022" title="why_read_whys_poignant_guide_to_ruby" src="http://www.victusspiritus.com/wp-content/uploads/2011/03/why_read_whys_poignant_guide_to_ruby.png" alt="" width="550" height="527" /></a></p>
</div>
<p>I'm feeling a little under the weather today*, which is a great time to get some reading done. I came across this old pdf floating around on the bottom shelf of my iBooks bookshelf. It's called <a href="http://www.victusspiritus.com/wp-content/uploads/2011/03/whys-poignant-guide-to-ruby.pdf">Why's Poignant Guide to Ruby</a>, but after digging in to the book I think you'll agree it's much more than just another programming language doc. Why was on a mission with this book, and somewhere out past the floating bits of the interweb, I imagine he's still on that mission. Do yourself a favor and put this pdf into your dropbox ebooks folder, add it to every iBookshelf you can, and set it on every desktop of every public computer you happen across as a gift to the curious ones.</p>
<p>References:<br />
Here's a great <a href="http://mislav.uniqpath.com/poignant-guide/">web home</a> for the guide.<br />
Feel free to <a href="http://jsfiddle.net/victusfate/ygjHz/">fiddle</a> with the odd resizing image code.</p>
<p>Notes:<br />
*= Today's particular brand of illness, spaced out + tummy woes</p>
