--- 
layout: post
title: Dropbox vs. JungleDisk
created: 1227677974
categories: 
- Review
tags:
- Amazon S3
- cloud computing
- Dropbox
- Jungle Disk
- storage
- Web 2.0
---
<p>I wrote a <a href="http://www.bmannconsulting.com/archive/omnibus-bbq-jungle-disk-wordpress-etc/">bit about Jungle Disk in passing</a>. I am using it for personal archive and backup. It's been working great, and I decided to try out the <a href="http://www.jungledisk.com/workgroup/index.aspx">Workgroup edition</a>: you add additional accounts and can set permissions on different buckets / folders for each person / account. At $2 / account / month for the workgroup functionality, it's quite good.</p>

<p>Except, you have to get people to install and setup Jungle Disk (the download link for Workgroup is a bit hidden). And ... it's not <a href="http://getdropbox.com">Dropbox</a>. I tried it for a bit, and it works as advertised, but you a) have to keep paying on a monthly basis and b) you have to do a fair bit of handholding and account management.</p>

<p>Then I tried Dropbox today. Easy. Amazing. Amazingly easy. And it does shared files, too. Share a folder, add some email addresses to invite people, and you've got synced folders / documents on multiple computers. The public stuff is actually easier ... there is a default folder called Public, and files in there you can right click on and get a publicly accessible link directly to.</p>

<p><strong>Update:</strong> <strong style="color: red;">CAUTION!</strong> -- I didn't realize this, but <a href="http://mjtsai.com/blog/2008/11/26/dropbox/">according to Michael Tsai, Dropbox doesn't support resource forks on Mac OS X</a> -- "If you use Dropbox, resource forks disappear, packages turn into folders and can no longer be double-clicked, etc. ". What this means is that some files will have issues. Basic files like Word docs and binaries shouldn't run into issues, but for applications, potentially Keynote files and others, your files may not work correctly any more.</p>

<p>Currently, there is a 2GB storage limit to the accounts (free). This also sits on Amazon S3, although on their account, not yours like Jungle Disk. Dropbox is offering a <a href="https://db.tt/0HiQby3a">paid upgrade to 50GB of space</a> for $9.99 / month, or $99 / year. Hmmm....2GB still seems enough for now...</p>

<p>I'll stick with the Jungle Disk Desktop edition for my backups and long term archives. I've paid the $20 for the Desktop edition and I can backup and store as much as I want on my own Amazon S3 account.</p>

<p>For multi user sharing of documents, Dropbox is just so much simpler. The low end pricing is cheaper than Jungle Disk (free!) while the high end of 50GB is cheaper with Jungle Disk (0.15/GB/month with S3 x 50GB = $7.50).</p>

<p>I think we're going to continue to see great innovation in better ways to share  / sync / collaborate on files, in part driven by cheap, reliable, API-driven storage options like S3. <a href="http://epdio.com/">Epd.io</a> is a local Vancouver startup to keep an eye on...</p>
<!--break-->
