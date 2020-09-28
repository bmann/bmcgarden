--- 
layout: post
title: Using PHP to integrate RSS feeds into your website
created: 1074470820
categories: 
- RSS
- MagpieRSS
- PHP
---
<p>
	PHP can be used to easily include feeds from other sites. The main advantage over a JavaScript solution is that everything can be run from your own site and you can take advantage of caching. The PHP can output straight HTML, which is fully searchable by search engines. As well, since all the files are &quot;local&quot; (except for updates to the included feeds), display tends to be faster, not relying on a JavaScript call to an external site for every page view.</p>
<!--break-->
<p>
	I&#39;ve chosen to use <a href="http://magpierss.sourceforge.net/">MagpieRSS</a> for my example, mainly because it is very, very easy to use while at the same time being quite feature rich. It is of course GPL, so you can use and extend it to your heart&#39;s content.</p>
<p>
	It should work &quot;out of the box&quot;. Download the <code>magpierss</code> archive to your server space and decompress it. Now, go to the <code>magpie_simple.php</code> file (which should be at <code>http://www.example.com/magpierss-0.5.2/scripts/magpie_simple.php</code>) and enter in the URL of a feed. Ta-da! You&#39;ve got a feed displayed.</p>
<p>
	You&#39;ll want to add all the settings and includes in one file, so that your feed can easily be included in any page by just using a simple line or two of PHP. From the Magpie site, here is a really simple example of all the code you need:</p>
<pre>
require_once &#39;rss_fetch.inc&#39;;

$url = &#39;http://magpie.sf.net/samples/imc.1-0.rdf&#39;;
$rss = fetch_rss($url);

echo &quot;Site: &quot;, $rss-&gt;channel[&#39;title&#39;], &quot;&lt;br&gt;\n&quot;;
foreach ($rss-&gt;items as $item ) {
	$title = $item[title];
	$url   = $item[link];
	echo &quot;&lt;a href=$url&gt;$title&lt;/a&gt;&lt;/li&gt;&lt;br&gt;\n&quot;;
}
</pre>
<p>
	For the complete example, including the walk-through of uploading files and setting permissions, see the specific example for OpenSourceXperts.com.</p>
