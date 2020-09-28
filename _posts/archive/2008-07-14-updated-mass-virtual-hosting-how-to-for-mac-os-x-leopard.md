--- 
layout: post
title: Updated Mass Virtual Hosting How to for Mac OS X Leopard
created: 1216021362
categories: 
- apache
- mod_vhost_alias
- vhost
- Leopard
- VirtualHost
- Mac
---
<p>I spent some time this weekend updating a long ago how to post on <a href="http://bmannconsulting.com/macosx/howto/enable-dynamic-virtual-hosting">configuring mass virtual hosting for Apache on Mac OS X</a> -- the <a href="http://bmannconsulting.com/node/1005/revisions/1973/view">original version</a> was from April 2004!</p>

<p>I do lots of testing on my laptop, and while I'm now quite familiar with VirtualHost entries from the dedicated servers I work with, this is actually even easier: just create a directory with the name of the host and requests for that host will be served from the directory. It all comes down to good old <a href="http://httpd.apache.org/docs/2.2/mod/mod_vhost_alias.html">mod_vhost_alias</a>. I probably should do some more direct examples of mixing and matching this with other host directives. As mentioned at the end of the article, aside from symlinking one directory to another, I don't know of another way to point multiple hosts at the same web root. I'll get to it if I end up needing it myself, it works for now.</p>
