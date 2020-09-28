--- 
layout: post
title: Private code repo hosting with Beanstalk and RepositoryHosting.com
created: 1278708578
categories: 
- Web Development
tags:
- Unfuddle
- SVN
- git
- GitHub
- version control
- Repository Hosting
- WebDAV
- project management
- Trac
- Basecamp
- DVCS
- Amazon S3
- Beanstalk
---
<p>For many years, I&#39;ve settled on <a href="http://unfuddle.com">Unfuddle</a> as my hosted tool of choice for development-focused project management and version control repo hosting. It&#39;s a great tool if you want all in one development ticketing / bug tracking (which is what I mean when I say &quot;dev focused&quot; PM) plus your code repository all in one place.</p><p>However, I&#39;ve been moving away from using Unfuddle for this type of project management, or been called into other projects where an existing PM tool is already in place -- most notable, either <a href="http://basecamphq.com">Basecamp</a> or <a href="http://openatrium.com">Open Atrium</a>, with the Drupal-based Atrium being something I&#39;m very keen on supporting (interested in seeing more hosted tools integrated with Open Atrium? <a href="http://bmannconsulting.com/contact">contact me</a>).</p><p>In cases like this, I really ONLY need a (private) hosted code repository*. I saw an article recently <a href="http://journal.uggedal.com/private-dvcs-hosting">comparing various options for private DVCS hosting</a> (DVCS = distributed version control systems like Git or Mercurial) which nicely complimented some of the research/experimentation that I&#39;ve been doing.</p><p>The review states its goals very clearly: lowest cost-per-repository, with storage used as a secondary consideration. Everyone will have their own needs to rank providers across.</p><p>For me, I&#39;m interested in a mix between features and pricing, especially using it on a consulting basis with lots of clients, and different kinds of clients (from those that don&#39;t use version control at all, to those that have in house developers already).</p><p style="text-align: center; "><img alt="" class="imagecache-fullpost lightbox" src="/sites/bmannconsulting.com/files/imagecache/fullpost/postimages/Screen shot 2010-07-13 at 10.59.48 AM.png" title="" /></p><p><a href="http://repositoryhosting.com/">RepositoryHosting.com</a> is clearly the lowest price-per-repository: it&#39;s $6 / month for unlimited repos with a bundled 2GB of storage, plus $1 per additional GB of storage. No &quot;cost per project&quot; means I can generate a project per client / idea / whatever and not have to worry about it. There is bundled ticketing in the form of Trac, and it&#39;s likely OK / has evolved since I got sick of it when we used it at Bryght -- I&#39;m not giving points in this review for PM tools in any case. The WebDAV shares is a very cool feature, especially for integrating clients, designers, and other folks into the mix that will find it hard to adopt the version control system directly.</p><p style="text-align: center; "><img alt="" class="imagecache-fullpost lightbox" src="/sites/bmannconsulting.com/files/imagecache/fullpost/postimages/ss-integrations.png" title="" /></p><p>On the features side of things, my pick goes to <a href="http://beanstalkapp.com/">Beanstalk</a>. It starts with a free plan so you can check it out right away with 1 private repo. The first paid plan is $15 per month, and I&#39;m fine with their 10 repository limit, but I&#39;m always annoyed at limited user counts. Regardless, it is a super clean interface that people will find very easy to use and it integrates with a ton of different tools (Twitter, Basecamp, Harvest, etc.). But the main reason it is a choice that I&#39;m going to be using more and more is that it offers direct FTP / SFTP deployment. I think this makes it a perfect tool for design-centric shops -- they can continue to use FTP-based hosting services and workflows, while starting to adopt best practices version control.</p><p><strong>Bottom line:</strong> <a href="http://unfuddle.com">Unfuddle</a> is a great all in one solution and one that I recommend to clients over and over again if they have no PM or development management tools in place, but for just repo hosting, you should consider <a href="http://repositoryhosting.com">RepositoryHosting.com</a> and <a href="http://beanstalkapp.com">Beanstalk</a>.</p>
<p>*yes, <a href="http://github.com/bmann">I&#39;m using GitHub</a>. It&#39;s awesome, end of story.</p>
