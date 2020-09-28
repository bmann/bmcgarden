--- 
layout: post
title: Testing Purple
created: 1183528129
categories: 
- code
- Eugene Eric Kim
- Les Orchard
- purple
- purple numbers
- purple-include
- Semantic Web
- transclusion
- Web 3.0
- XPath
- Drupal
---
 <p id="p-0">It's been quite some time since I wrote about <a href="http://bmannconsulting.com/blog/bmann/purple-everywhere">purple numbers</a> -- fragment identifiers for bits of text within HTML documents. Or, <a href="http://www.eekim.com/software/purple/purple.html">Granular Addressability in HTML documents as E.E. Kim describes</a> in 'An Introduction to Purple'.</p>

<p id="p-1">Back then, I wasn't a fan of these anchor links, as anchor links aren't first class web citizens -- where links are currency. I'm still not a fan, but maybe the anchor links are just there to make it easy to grab pieces of this content.</p>

<p id="p-2">A recent <a href="http://blogs.opml.org/decafbad/2007/07/03#When:1:45:16PM">reference by Les Orchard</a> (oh, look, OPML anchor tags!) to <a href="http://blueoxen.net/c/purple/purple-include/">purple-include</a>, which enables transclusion (aka including content from elsewhere, directly inline, rather than copy/paste) got the brain cells tickling tonight. So I built a Purple module for Drupal. Which, in reality, just includes the purple-include.js and a little bit of CSS to make purple links show up. I am trying to include some of <a href="http://simonwillison.net/2004/May/30/plinks/">Simon Willison's plinks cleverness</a>, but not sure if I'm going to get that working.</p>

<p id="p-3">Transclusion feels very <acronym title="Semantic Web">SemWebby</acronym>. No, I'm not going to use the dreaded Web 3.0-label (but do go read the <a href="http://money.cnn.com/magazines/business2/business2_archive/2007/07/01/100117068/index.htm?postversion=2007070305">Business 2.0 article</a> if you want a backgrounder (via <a href="http://novaspivack.typepad.com/nova_spivacks_weblog/2007/07/web-30----no-hu.html">Nova Spivack, of course</a>). Ahem. Back to the point.</p>

<p id="p-4">From Facebook apps to photos stored on Flickr, we want to have all our "stuff" just magically collected together wherever we happen to be, whatever network we happen to be interacting with. Aggregation, sucking this content in, pushing it over there -- all just temporary ways of flowing content around. One that arguably duplicates content and spews extraneous permalinks around. I just want my pictures right here, or I just want to link deep into someone else's posting and pull in a piece of text. And I want the "other end" to know about that inclusion, a gentle ping, yeah, kind of a trackback. That's the Semantic Web to me: where every plain old HTML file is dynamic and intelligent and knows about the links and people that are incoming and outgoing.</p>

<p id="p-5">OK, now to Purple. Here's an example that includes a file I have on my server, shamelessly copied from the <a href="http://blueoxen.net/c/purple/purple-include/tests/examples.html">purple-include examples page</a>. First the code:</p>
<code>
&lt;hx:include src=&quot;/sites/bmannconsulting.com/files/purple_include.html#xpath!//p&quot;&gt;&lt;/hx:include&gt;
</code>
<p id="p-6">And now the transcluded bit:</p>
<code>
<hx:include src="/sites/bmannconsulting.com/files/purple_include.html#xpath!//p"></hx:include>
</code>

<p id="p-7"><strong>Update:</strong> <a href="http://haggaret.com">Kevin</a> reports that the transclusion doesn't work in Safari. Stupid client side technologies :P</p>

<p id="p-8">Note: I don't *actually* know XPath. But if you open the <A href="/sites/bmannconsulting.com/files/purple_include.html">file directly</a>, you'll see it just grabbed the paragraph. I'm assured you can do more complicated things than that :P</p>

<p name='p-todo' id='p-todo'>To Do: <a href='#p-todo' class='plink'>#</a></p>
<ul>
<li>Find out where purple-proxy is hiding / what to do with it so I can transclude from elsewhere</li>
<li>autogenerate plinks / pilcrows / numbers, perhaps via a Drupal filter</li>
<li>make a real module available somewhere, maybe also tracking down jluster's old purple numbers code</li>
</ul>
<!--break-->
<p id="p-9">Here's pretty much the entire "meat" of the module, which does nothing but include some JavaScript and CSS:</p>

<pre>
function purple_footer() {
  $path = drupal_get_path('module', 'purple');
  drupal_add_css($path .'/purple.css', 'module', 'screen');
  drupal_add_js($path . '/purple-include.js','module');
}
</pre>

<p id="p-10">That was fun, and somewhat therapeutic. It's only going to get really interesting when I grab the proxy code. Oh, and of course, I'm typing in bare HTML here and turning off the WYSIWYG which eats funky hx-namespaced code for breakfast.</p>

<p id="p-11">Oh yes, and to the various folks I've bumped into that tell me "Sometimes I have no idea what you're talking about"...well, sorry, this is probably one of those posts :P</p>
