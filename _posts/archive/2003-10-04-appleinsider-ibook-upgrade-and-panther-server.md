--- 
layout: post
title: "AppleInsider: iBook Upgrade and Panther Server"
created: 1065330780
categories: 
- Mac
---
A bunch of quick stuff that's new from several Apple sites -- iBooks and the new, Panther version of OS X Server.

Apparently, the <a href="http://www.appleinsider.com/article.php?id=212">iBooks are getting an upgrade</a>. It is about time, and it might just be the right time to get one. The <a href="http://www.appleinsider.com/article.php?id=170">new Panther Server has a boatload of features</a> and sounds amazing. I still haven't played with an install of OS X Server...
<!--break-->
I've been thinking seriously about a laptop again. It would likely become my main machine, with my current iMac going into rotation as Kate's main machine, and the PC getting shuffled somewhere in "headless" mode -- possibly hooked into sharing a keyboard/mouse/monitor with the iBook. But, I have a few other things that need dollars thrown at them for the moment...

Anyway, looks like the iBooks are getting all the extras -- faster DDR RAM, USB 2.0, Bluetooth, Airport Extreme, etc. A little slower and with a slightly less powerful graphics card than their PowerBook big brothers.

Panther Server is actually scheduled to ship next month. The directory services look to be getting even more open -- there is support for sticking everything in OpenLDAP instead of Apple's NetInfo. It seems that the more standard/open that Apple gets, the more popular it gets.

The news that Cyrus is the mail server rings a few bells with me. Whenever I hear "Cyrus", I think two things: <a href-"http://www.faqs.org/rfcs/rfc2086.html" title="RFC2086 - IMAP4 Access Control List Extension">ACLs</a> and <a href="http://www.bynari.net" title="Bynari">Bynari</a>. Bynari makes a <a href="http://www.bynari.net/index.php?id=500" title="Bynari InSight Connector">plugin for Outlook</a> called InSight Connector that allows for Exchange-like functionality. Using the plugin, you can sync all Outlook items to any IMAP server, and share items if the server supports ACLs. In practice, this means the Cyrus IMAP server, since it has the best-developed ACL features.

So, along with rumours that the version of Mail.app that ships with Panther will support Exchange capabilities (yup, so rumoured that I don't even have a link handy at the moment), this leads me to believe that Apple will ship full support for Exchange functionality to both Mac and Windows clients. Oh? Did I mention that Panther can function as a PDC, and that there is some sort of Active Directory integration without schema modifications?

I think I get to add OS X 10.3 Server as a viable option for both Mac <strong>and</strong> Windows networks...
