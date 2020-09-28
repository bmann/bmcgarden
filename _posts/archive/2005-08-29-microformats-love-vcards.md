--- 
layout: post
title: Microformats love vCards
created: 1125351562
categories: 
- Web Development
- Social Media
---
<p>I had a chance to to have a long talk with <a href="http://tantek.com/log">Tantek</a> about <a href="http://www.microformats.org">microformats</a> -- following on <a href="http://www.bmannconsulting.com/node/1539">comments we were trading on the subject</a>.</p>

<p>The impression that I had been getting is that microformats were meant as a <strong>replacement</strong> for today's desktop standard formats -- vCards for people and companies, vCal for events/calendaring data. But the various h* formats are not replacements. They build directly on these existing formats -- the <a href="http://microformats.org/wiki/hcard">hCard spec</a> actually states that it is a "1:1 representation of the vCard standard (RFC2426) in XHTML".</p>

<p>I'm sort of posting this for my own clarity in trying to figure out where microformats fit, especially in comparison to desktop integration (they'll translate to vCard and vCal) and direct API support (e.g. the <a href="http://drupal.org/node/27953">upcoming.org integration into Drupal</a>).</p>

<p>Feedback to microformats promoters: the desktop integration story is something that I was very confused about, and it's where my perception of competition with vCards etc. came from. Other than being mentioned on the spec page, these desktop formats aren't mentioned on the front page or on the about page at all. There isn't a FAQ section, but maybe there should be. Here's my first cut at what I would put on such a page:</p>
<!--break-->
<p>Q: How do microformats integrate with my desktop applications (e.g. Outlook, iCal, Thunderbird, etc.)?</p>

<p>A: insert answer with pointers to Greasemonkey scripts as well as vCard/vCal transformation proxies.</p>

<p>Q: Are microformats in competition with vCard, vCal, or other formats?</p>

<p>A: No. Microformats are primarily for display -- designed for human viewing. They work in conjunction with existing formats to integrate with desktop apps. See (insert link to first Q/A) for more information.</p>

<p>I think the main disagreement between Tantek and myself is how these formats will spread. He believes that hand-coding -- whether of individual static pages or of templates in publishing tools -- will be the main vector. I tend to think that writing plugins that implement APIs to various data sources will surpass this quite quickly. Of course, even in the latter case, developers can (will!) support microformats at the display layer, so everyone can have their own way.</p>

<p>I look forward to serving our new microformat overlords :P</p>
