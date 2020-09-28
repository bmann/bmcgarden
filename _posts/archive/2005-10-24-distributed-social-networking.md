--- 
layout: post
title: Distributed Social Networking
created: 1130163749
categories: 
- p2p
- ton zylstra
- jabber
- FOAF
- XFN
- vCard
- Canter's Law
- barcamp amsterdam
- social networking
- Social Media
---
<p>I didn't get nearly as much time (hardly any!) to talk to <a href="http://www.zylstra.org">Ton Zylstra</a> at BarCamp Amsterdam as I would have liked to. He's continuing the conversation on his blog, with this post about P2P social networking:</p>  <blockquote> <p>I would like to have a true peer to peer social networking platform.&nbsp;Also I'd like to have my own spiders and agents.</p> <p>FOAF isn't ready for this kind of thing I think, but we might look to an <a href="http://www.zylstra.org/blog/archives/001807.html">existing p2p infrastructure like Skype</a> to be a carrier. <a href="">Boris Mann</a> pretty much repeatedly said Jabber can do anything during BarCamp, and seemed to be only half joking. <a href="http://www.zylstra.org/blog/archives/001818.html">Ton's Interdependent Thoughts: How to Get P2P Social Networking</a> </p></blockquote>  <p>You're right, Ton, I <em>was</em> only half joking. I think real time is very important. If the &quot;IM Wars&quot; have shown us anything, it's that we need to have common standards and formats. For XML message passing, including IM, Jabber is the answer to this (and might be the answer for voice and video as well, but I've got more to write about this later).</p>  <p>But whatever the pieces of the infrastructure are, we still need to be able to pass rich user profiles back and forth. We've got an RDF-based one in <a href="http://www.foaf-project.org/">FOAF</a>, we've got a microformat one in <a href="http://gmpg.org/xfn/">XFN</a>, and we've got a desktop app-compatible one in vCard. What's missing? An extensible XML-based format for user profiles that is standardized and widely deployed. Actually, <a href="http://www.jabber.org/jeps/jep-0054.html">Jabber uses an XML version</a>, with an interesting <a href="http://www.jabber.org/protocol/vcard-xml/history.html">historical note</a>. The <a href="http://www.w3.org/TR/vcard-rdf">W3C has an RDF spec</a> of vCard, but I still think an XML one is going to be required. I think this will become clear along with advances in the identity infrastructure. In the meantime, we'll need to follow <a href="http://marc.blogs.it/archives/2005/09/canters_law_1.html">Canter's Law #1</a>, and support all formats.</p>
