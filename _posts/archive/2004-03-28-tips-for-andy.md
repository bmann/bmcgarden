--- 
layout: post
title: Tips for Andy
created: 1080526813
categories: 
- Personal Publishing
- Mac
---
<p>Andy is just about ready to start running a personal publishing system of some kind. He's going to run it off his Mac at home for now, so he wanted a couple of pointers.</p>
<!--break-->
<p>First off, don't bother with a static IP address from your broadband provider. It's absolutely not necessary. I pointed him to <a href="http://www.easydns.com">EasyDNS</a> for domain registration and dynamic DNS. On the Mac, combine that with <a href="http://www.dnsupdate.org/">DNSUpdate</a>. This is very reliable  and has worked great for me.</p>

<p>Andy spent all day look into various open source content management systems. He looked at the <a href="http://www.opensourcecms.com/">Open Source CMS site</a> and in particular mentioned <a href="http://www.angelinecms.org/">Angeline CMS</a>. I don't know much about the app other than it doesn't come up very often when you <a href="http://www.google.com/search?q=angeline+CMS&ie=UTF-8&oe=UTF-8" title="'Angeline CMS' Google Search">search for it with Google</a>, which is never a good sign.</p>

<p>I'm pretty blunt these days: use <a href="http://www.wordpress.org">WordPress</a> if you want a basic blog, choose <a href="http://www.drupal.org">Drupal</a> if you need more features, control, and options.</p>

<p>Then we were talking about hosting more than one domain, or at least different sites for sub-domains (e.g. <code>subdomain.example.com</code>). I remembered I enabled virtual hosts on my Mac before, so I dug out the relevant bits from my <code>httpd.conf</code> file. I've written that up in a how-to called <a href="http://www.bmannconsulting.com/macosx/howto/enable-dynamic-virtual-hosting">Enabling Dynamically Configured Name-based Virtual Hosting on Mac OS X</a>.</p>
