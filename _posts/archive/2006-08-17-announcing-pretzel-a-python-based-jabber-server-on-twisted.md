--- 
layout: post
title: Announcing Pretzel, a Python-based Jabber server on Twisted
created: 1155834507
categories: 
- jabber
- pretzel
- Pretzel Server
- Twisted
- JEP-0080
- geolocation
- IM
- Open Source
---
<p>I have the great pleasure to announce <a href="http://code.google.com/p/pretzel/">Pretzel</a> -- a Jabber server written in Python on the <a href="http://twistedmatrix.com/">Twisted</a> framework.</p><p>The two main authors are <a href="http://ralphm.net/blog/">Ralph Meijer</a>, well known as a long time member of the Jabber community, and <a href="http://term.ie/blog/">Andy Smith</a>, hacker extraordinaire. </p><p>For now, Andy checked in some experimental code hosted on Google&#39;s new code repository. Check it out at <a href="http://code.google.com/p/pretzel/" title="Pretzel - Python Jabber Server on Twisted">http://code.google.com/p/pretzel/</a>. We&#39;re looking for other people to join in -- one of the reasons we started the project was because it seemed there were a lot of people looking for the same thing. It is available under the MIT license to make it potentially usable by the broadest number of people, as well as being under the same license as Twisted.</p><p>Please join us on the <a href="http://groups.google.com/group/pretzel-dev/">pretzel-dev list</a> and we&#39;ll get the discussion going.&nbsp;</p><p>What&#39;s on the roadmap? Well, this is a very early release -- more of a proof of concept. We hope to enable the quick and easy implementation of various JEPs, making it fun and simple to add all sorts of powerful features to the server and clients, truly showing how Jabber can go way beyond &quot;just&quot; instant messaging.</p><p>One of the first goals will be support for geolocation/presence information. <a href="http://ralphm.net/world">Ralph&#39;s map</a> is an interesting example of what could be built...expect that to be live, allowing you to update your location yourself, using your client. Since practically no clients (leave a comment if you know of one) support <a href="http://www.jabber.org/jeps/jep-0080.html">JEP-0080 User Geolocation</a> today, we&#39;ll likely provide some simple text-based ways to send that information (e.g. geoloc:48,100 or some such). </p>
