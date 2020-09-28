--- 
layout: post
title: SIte moved to Rimu Hosting
created: 1239782644
categories: 
- Rimu Hosting
- Bryght
- VPS
- Xen
- CentOS
- BMC
---
<a href="http://bryght.com">Bryght</a> is shutting down hosting, so I moved to <a href="http://rimuhosting.com">Rimu Hosting</a>. I already run the <a href="http://bootuplabs.com">Bootup Labs</a> site there, and have recommended it to a number of other people. Do I have more to say about Bryght? Not right now, although it feels like I've got a lot of stories tucked away that need to get told at some point.

I've got a <a href="http://rimuhosting.com/order/startorder1.jsp?hom=t-vps">Miro VPS 2</a> - $30 / month, 400MB memory, 4GB of storage. I never get a control panel - it's running Webmin on CentOS, and I asked for the newest version of PHP, plus Apache and MySQL set to run at startup.

It's actually been a pleasure to "move in" to a new server. The old system had been running for a long time, and various failed experiments at different upgrades -- most around PHP and accelerator versions. Also various different test installs of a variety of sites.

So, just like a fresh operating system install on a computer, I had this brand new server to work on, including how I would set up my SVN check outs, different projects, and so on. I'll document my exact SVN setup in another post -- I've got a small <a href="http://unfuddle.com">Unfuddle</a> account where everything is stored. Suffice to say that there is some great svn:externals stuff going on - nice work, <a href="http://acquia.com/documentation/getting-started/fresh-install/svn">Acquia in SVN</a>.

I've only got one configuration note so far for fresh CentOS servers that are running PHP -- enable the "remi" repo: http://blog.famillecollet.com/pages/Config-en

You'll want to install APC (bunch of dependencies, then use pear - see <a href="http://maisonbisson.com/blog/post/12589/installing-php-apc-on-rhel-centos/" title="Installing APC on RHEL/CentOS">here for CentOS instructions</a>) plus GD and mbstring.

One note: whether it's Rimu Hosting or some other factor (i.e. Drupal), I haven't been able to get email to send to Google Apps for Domains hosted email addresses. Regular Gmail addresses work fine, just not Google Apps.
