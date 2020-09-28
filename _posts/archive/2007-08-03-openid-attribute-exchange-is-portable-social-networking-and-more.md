--- 
layout: post
title: OpenID Attribute Exchange is portable social networking and more
created: 1186166947
categories: 
- identity
- OpenID
- Attribute Exchange
- Scott Kveton
- SXIP
- FOAF
- XFN
- Social Media
---
<p>Scott Kveton does a bit of a round up of what <a href="http://kveton.com/blog/2007/08/03/portable-social-networking-is-coming/">some folks are working on a technical level with portable social networking</a>, in and around OpenID and some loose markup.</p>

<p>He takes what, in my opinion, is a bit of a cut against <a href="http://openid.net/specs/openid-attribute-exchange-1_0-05.html">Attribute Exchange</a>:</p>

<blockquote>
Also, attribute exchange doesn’t solve the portable social networking component although I imagine it could be hacked up to do so.
</blockquote>

<p>Sorry, Scott, when you use phrases like "hacked up", I take issue. Frankly, I would never have gotten on board with OpenID if I didn't see AX on the horizon as the logical conclusion of the SREG stop gap.</p>

<p>AX is an extensible system that will be able to pass many different kinds of information back and forth between systems. It has the same decoupled nature that OpenID has. Different sites can loosely couple by doing nothing more than using the same keys to define different sets of attributes. Why, exactly, would one NOT use this? In theory, one could do something as simple as host an agreed upon list of attributes -- based on FOAF, XFN, or for that matter any one of them in their own namespaces or with mapping between them.</p>

<p>I mean, we implemented syncing of user profiles using <a href="http://www.bryght.com/news/2004/10/19/bryght-releases-foaf-module">Drupal's simple distributed authentication + FOAF</a> *3 years ago*. Working with <a href="http://www.sxip.com">SXIP</a> in their various protocol incarnations, DIX, and finally the merging into OpenID and AX has all been part of the process of consensus around standards.</p>

<p>Attribute Exchange is a flexible, extensible base on which to implement many use cases around data exchange for user profiles and related information. Any solution around portable social networking should use this at its base, and the OpenID community should move to finalize the extension and move forward to building cool sh*t on top of it.</p>
<!--break-->
