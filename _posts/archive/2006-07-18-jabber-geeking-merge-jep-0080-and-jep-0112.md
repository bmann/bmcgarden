--- 
layout: post
title: "Jabber geeking: merge JEP-0080 and JEP-0112?"
created: 1153242125
categories: 
- IM
- XMPP
- JSF
- JEP-0112
- JEP-0080
- jabber
- geolocation
---
<p>I&#39;m in Stuttgart meeting with some clients. Lots of Drupal + Jabber integration talk, and luckily <a href="http://ralphm.net/">ralphm</a> is here to bring along lots of Jabber expertise.</p><p>We&#39;ve been talking a lot about geolocation notification over Jabber -- so users can indicate their location over Jabber. There are few (if any?) clients that support this today, so we&#39;ll probably support some short hand for testing purposes -- being able to type in geoloc:[lat],[lon].</p><p>So, I was looking at <a href="http://www.jabber.org/jeps/jep-0080.html">JEP-0080 (geoloc)</a> and <a href="http://www.jabber.org/jeps/jep-0112.html">JEP-0112 (physloc)</a>. 112 is a plain text representation of physical location, and JEP 80 is the latitude / longitude. JEP 80 also has a plain text &quot;description&quot; field. So...why not collapse the two? physloc could replace the current JEP 80 &quot;description&quot; entry...every single entry is optional, so the text field in physloc can handle the current usage of the description field. It just seems wasteful to maintain two separate JEPs for what is essentially the same information.</p><p>As well, if a service already knows the physical location, it can send it along with the geoloc -- you can&#39;t derive the physical location from the geolocation, so in the current case, you would have to send two messages.<br /> </p><p>The *one* issue is the reverse: the latitude and longitude for geoloc are currently set to MUST. This means we can&#39;t send only the physical location, and leave the lat/long blank...I think this should be changed...people can send updates of either geolocation or physical location -- the server side can do a geoloc lookup if needed.</p><p>BTW, I reapplied for <a href="http://wiki.jabber.org/index.php/Membership_Applications_July_2006">membership in the Jabber Software Foundation</a> -- apparently the April voting had some issues.&nbsp;</p>
