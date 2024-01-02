--- 
layout: post
title: Fussing about formats, Micro or otherwise
created: 1125005194
categories: 
- Web Development
- Social Media
---
<p>OK, Peter Caputa, you pushed me over the edge with this one:</p>

<blockquote>
<p><a href="http://www.unmediated.org/archives/2005/08/econometa_on_mi.php">Exactly</a>. Microformats could be as big an innovation as databases were. </p>

<p>If databases let us store information. Microformats let us access the world's databases. Potentially! </p>

<p>Yes, APIs do this too. But, microformats make the database (or data store) distributed. Not controlled by one entity. </p>
<cite><a href="http://worcester.typepad.com/pc4media/2005/08/microformats_en.html">pc4media: MicroFormats Enable Distributed Applications!</a></cite> 
</blockquote>

<p>Umm. OK. Except....all the microformats that are going to be in wide usage are going to be auto-generated by dynamic systems of some kind (e.g. WordPress, Drupal). Which run on databases. Which can just as easily use an API directly or generate a standard format (e.g. vCard, vCal, etc.) that *works today*.</p>

<p>I'm not against microformats. <a href="http://www.factoryjoe.com">Chris</a> and I had a long discussion in Portland about this, wherein I couldn't make my point clearly. The usefulness that I have seen is some Greasemonkey scripts that take hCard and hCal and automatically create....vCard and vCal.</p>

<p>For the time being, these standard formats are well understand by lots of applications. Double-click them, and your local OS will "do stuff".</p>

<p>I think Chris' point is that eventually, the browser will be able to understand all of these things natively, while parsing. Well, except, I don't want my browser to be one big bloated app that does everything. We've been there before, and it sucks. See also: Firefox, Thuderbird, Sunbird, etc.</p>

<p>For now, I'm sitting microformats out. We'll happily support them and generate them (and yes, having a common layout from a design perspective is useful), it's just that it's easier to build distributed apps today by using APIs. Which <strong>are</strong> distributed.</p>

<p>Please bang me about the head if there is something I'm missing here.</p>