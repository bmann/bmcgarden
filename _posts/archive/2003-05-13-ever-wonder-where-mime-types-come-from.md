--- 
layout: post
title: Ever wonder where MIME types come from?
created: 1052872860
categories: 
- Web Development
- PHP
---
It turns out that <a href="http://www.iana.org/">IANA</a> (the Internet Assigned Numbers Authority) is also responsible for <a href="http://www.iana.org/assignments/media-types/">registering MIME types</a>.

You can also go to IANA to find out who/what owns various top-level domains (TLDs) and the various ccTLDs (country code TLDs). My dreams of registering <strong>canada.eh</strong> were dashed when I found out that <a href="http://www.iana.org/root-whois/eh.htm">Western Sahara owns .eh</a>. And they don't have a registry.

What was I doing? I was working on a PHP script that will set a file for download, setting the header "Content-Type" to the specific type of file. In my case, a comma-separated value (CSV) file. Closest thing is application/vnd.ms-excel, which is probably where I want it to end up anyways.
