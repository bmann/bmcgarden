--- 
layout: post
title: More Purple
created: 1183776670
categories: 
- Brad Neuberg
- purple
- purple numbers
- purple-include
- transclusion
- Web Development
---
<p><a href="http://codinginparadise.org/">Brad Neuberg</a> <a href="http://bmannconsulting.com/blog/bmann/testing-purple#comment-136422">left a comment</a> on where to find the proxy...or rather, that left me an email address so I could email him that there was no download link :P I've got it now, so now I can transclude the <a href="http://blueoxen.net/c/purple/purple-include/#nidLK">introduction from the purple-include page</a> here directly (note: probably Firefox only at this point -- you should some purple text below after this rolling symbol: <img src="/roller.gif" />):</p>

<blockquote style="color: purple;">
<hx:include src="http://blueoxen.net/c/purple/purple-include/#nidLK"></hx:include>
</blockquote>

<p>And that was just one more line in the Drupal module to set the meta tag:</p>
<code>
drupal_set_html_head(&#39;&lt;meta name=&quot;purple_proxy_path&quot; content=&quot;/&#39; . $path . &#39;/purple-proxy.php&quot; /&gt;&#39;);
</code>

<p>Now I just have to hope that bad, terrible things won't happen from this proxy.</p>
