--- 
layout: post
title: Calendaring in XHTML
created: 1097046000
categories: 
- Social Media
- Web Development
---

<p>A long time ago (almost 1000 posts ago!), I talked about an alternative to <acronym title="Fried Of A Friend">FOAF</acronym> I had dreamed up, called <a href="http://www.bmannconsulting.com/node/442" title="Profile Reveals Origins, Interests, Likes, Etc.">PROFILE</a>. I'm still not a big fan of FOAF's RDF-ishness, but I love open-ness more, and FOAF is the only moderately widespread profile interchange format today (my FOAF is <a href="http://www.bmannconsulting.com/foaf/1">here</a>, thanks to the Drupal module <a href="http://www.walkah.net">James</a> wrote).</p>

<p>I expressed it really badly back then, but what I wanted PROFILE to be was an XHTML-valid format so that it would easily display within web pages using nothing but CSS for styling, but still have enough semantic meaning to be machine-parsable.</p>

<p>So the next target is calendaring information. <a href="http://tantek.com/log/2004/09.html#hcalendar">Tantek calls it hCalendar</a>, inspired by some work at <a href="http://wiki.oreillynet.com/foocamp04/index.cgi?HTMLForCalendars">foocamp04 on HTMLForCalendars</a>.</p>

<p>I recently wrote up some thoughts on <a href="http://dev.bryght.com/cgi-bin/trac.cgi/wiki/EventiCalModule">syndicating events using iCal in Drupal</a>. That is, embed/attach iCal to RSS feeds. This will likely still happen (lots of people can easily consume iCal compatible information today). But for web-to-web representation, especially in feed readers, an XHTML compatible format would provide easy display today.</p>

<p>Hat tip to <a href="http://www.laughingmeme.org">kellan</a> for the Tantek related links.</p>
