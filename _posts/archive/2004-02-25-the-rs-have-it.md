--- 
layout: post
title: The R's Have It
created: 1077730620
categories: 
- Social Media
---
<p><strong>R</strong> as in <a href="http://www.flickr.com/services/">Flickr services</a>, that is. <a href="http://erikbenson.com/entries/2004/02/23/talkrnet_proposal.html">Erik Benson lays out his vision for Talkr</a>, which in a nutshell is distributed identity using Flickr to manage/track/surf posts you make anywhere.</p>

<blockquote>
<p><strong>Example use cases:</strong></p>

<p>Seems like a lot of work, but if you think about it most of it happens behind the scenes.  The first time you use this it will require the following clicks:</p>

<ol><li>Click button to open popup.</li>
<li>Authenticate on flickr.</li>
<li>Choose which details to allow them to use from talkr.</li>
<li>Write your comment and submit.</li>
</ol>
</blockquote>

<p>You may want to implement it as an MT plugin, but please make it a nice sensible API so that it can be added to other systems (the references to pop-up [ugh!] are for MT based blogs).</p>

<!--break-->

<p>Adding authentication to Drupal would consist of simply adding the Flickr authentication scheme to the list of allowed external authentications. The next bit that I want, which is to add/integrate a link to your Flickr profile for each member, would be a bit trickier. This ties in directly with the Talkr proposal, because then the <a href="http://www.bmannconsulting.com/usr/1">user page</a>, where the "view recent blog entries" link is, could actually point to posts and comments all over the place.</p>
