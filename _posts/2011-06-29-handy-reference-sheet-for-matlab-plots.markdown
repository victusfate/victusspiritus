---
layout: post
status: publish
published: true
title: Handy Reference Sheet for Matlab Plots
author: Mark Essel
author_login: messel
author_email: messel@gmail.com
author_url: http://messel.myopenid.com/
wordpress_id: 9400
wordpress_url: http://www.victusspiritus.com/?p=9400
date: '2011-06-29 09:46:11 -0400'
date_gmt: '2011-06-29 16:46:11 -0400'
categories:
- Uncategorized
tags:
- visualization
- matlab
comments: []
---
<p>When plotting in Matlab it's useful to quickly pass a plot strong to a plotting function (plot, plot3, etc).</p>
<blockquote>
<pre>plot(x,y,'.r')</pre>
<pre>plot3(x,y,z,'xb')</pre>
<pre>plot(data,^g')</pre>
<p>are all acceptable symbol and color combinations
</p></blockquote>
<h2>Symbols</h2>
<table cellspacing="0" class="body" cellpadding="4" border="2">
<colgroup>
<col width="42%">
<col width="58%"></colgroup>
<thead>
<tr valign="top">
<th bgcolor="#B2B2B2">Marker Specifier</th>
<th bgcolor="#B2B2B2">Description</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562683"></a><tt>'+'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Plus sign</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562687"></a><tt>'o'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Circle</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562691"></a><tt>'*'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Asterisk</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562695"></a><tt>'.'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Point</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562699"></a><tt>'x'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Cross</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562703"></a><tt>'square'</tt> or <tt>'s'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Square</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562707"></a><tt>'diamond'</tt> or <tt>'d'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Diamond</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562711"></a><tt>'^'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Upward-pointing triangle</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562715"></a><tt>'v'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Downward-pointing triangle</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562719"></a><tt>'&gt;'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Right-pointing triangle</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562723"></a><tt>'&lt;'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Left-pointing triangle</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562727"></a><tt>'pentagram'</tt> or <tt>'p'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Five-pointed star (pentagram)</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562731"></a><tt>'hexagram'</tt> or <tt>'h'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>Six-pointed star (hexagram)</p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f61-562735"></a><tt>'none'</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p>No marker (default)</p>
</td>
</tr>
</tbody>
</table>
<h2>Colors:</h2>
<table cellspacing="0" class="body" cellpadding="4" border="2">
<colgroup>
<col width="33%">
<col width="33%">
<col width="34%"></colgroup>
<thead>
<tr valign="top">
<th bgcolor="#B2B2B2">
<p>RGB Value</p>
</th>
<th bgcolor="#B2B2B2">
<p>Short Name</p>
</th>
<th bgcolor="#B2B2B2">
<p>Long Name</p>
</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f19-235305"></a><tt>[1 1 0]</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235307"></a><tt>y</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235309"></a><tt>yellow</tt></p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f19-235311"></a><tt>[1 0 1]</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235313"></a><tt>m</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235315"></a><tt>magenta</tt> </p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f19-235317"></a><tt>[0 1 1]</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235319"></a><tt>c</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235321"></a><tt>cyan</tt></p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f19-235323"></a><tt>[1 0 0]</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235325"></a><tt>r</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235327"></a><tt>red</tt></p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f19-235329"></a><tt>[0 1 0]</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235331"></a><tt>g</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235333"></a><tt>green</tt></p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f19-235335"></a><tt>[0 0 1]</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235337"></a><tt>b</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235339"></a><tt>blue</tt></p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f19-235341"></a><tt>[1 1 1]</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235343"></a><tt>w</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235345"></a><tt>white</tt></p>
</td>
</tr>
<tr valign="top">
<td bgcolor="#F2F2F2">
<p><a name="f19-235347"></a><tt>[0 0 0]</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235350"></a><tt>k</tt></p>
</td>
<td bgcolor="#F2F2F2">
<p><a name="f19-235352"></a><tt>black</tt></p>
</td>
</tr>
</tbody>
</table>
