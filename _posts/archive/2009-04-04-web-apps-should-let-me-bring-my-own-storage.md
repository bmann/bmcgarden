--- 
layout: post
title: Web apps should let me "Bring my own storage"
created: 1238890738
categories: 
- Amazon S3
- Batchbook
- cloud storage
- Dropbox
- Highrise
- Huddle
- Joyent
- Jungle Disk
- Nirvanix
- Rackspace
- side loading
- Web 2.0
- Amazon S3
- Batchbook
- cloud storage
- Dropbox
- Highrise
- Huddle
- Joyent
- Jungle Disk
- Nirvanix
- Rackspace
- side loading
- Web 2.0
---
<p>I've written up <a href="http://bmannconsulting.com/blog/bmann/dropbox-vs-jungledisk">Dropbox vs.&nbsp;Jungle Disk</a> before, and then followed up with the concept of <a href="http://bmannconsulting.com/blog/bmann/side-loading-pre-fetching-and-cloud-storage">side loading</a> - having software assets (purchased or otherwise) be moved from one online location to a cloud storage location owned by you.</p>
<p>The guys at <a href="http://blog.jungledisk.com/2009/04/04/jungle-disk-roadmap-update/">Jungle Disk are looking to add features to their service</a>, asking people to vote between public/private file sharing, multi-computer sync, and network drive offline access. Since this is exactly what I&nbsp;use <a href="https://www.getdropbox.com/referrals/NTM2MDM5ODk">Dropbox</a> for (I use Jungle Disk for backup and long term archive), I really would love to see them add all three.</p>
<p>Dropbox still only has two downsides for me. First, it's reselling Amazon S3 storage to me at a premium, and I resent that. Secondly, because of it's sync model, I have to have enough room for all my files on every computer I enable it. I'm storing all my files in the cloud so I don't *have* to have unlimited storage. Like <a href="http://zumodrive.com/">ZumoDrive</a> does, there should be some smart caching to keep some stuff local, and make all of it available when needed.</p>
<p>I can't really blame Dropbox - they're doing the same thing countless other web app companies are doing. Amazon S3 is one of the biggest, cheapest, and most reliable options out there. <a href="http://www.joyent.com/connector/bingodisk/">Joyent's BingoDisk</a>, <a href="http://www.mosso.com/cloudfs/">Rackspace's CloudFS</a>, and <a href="http://www.nirvanix.com/">Nirvanix</a> are three examples of somewhat equivalent offerings with slightly differing price points, so let's assume those are included in the concept of reselling cloud storage. But here's the thing I realized, and <a href="http://twitter.com/bmann/status/1428370165">posted on Twitter</a> the other day:</p>
<blockquote>
	<p><span class="status-body"><span class="entry-content">Lots of online apps differentiate pricing based on storage. I'd much rather they didn't offer storage, and let me plugin S3 / Dropbox / etc.</span></span></p>
</blockquote>
<p>&nbsp;</p>
<p><!--break--></p>
<p>I was realizing this as I was looking at the <a href="http://www.huddle.net/huddle-price-plans/">pricing plan for Huddle</a> (which is project management sorta like Basecamp):</p>
<p class="rtecenter"><a alt="View the image at QuickSnapper.com" href="http://www.quicksnapper.com/borismann/image/huddle"><img src="http://www.quicksnapper.com/files/4037/84165451349D7F4A92AE5D_m.png" style="width: 481px; height: 325px;" title="Hosted by QuickSnapper.com"></a></p>
<p>Storage seems to be one of the major items of differentiation. But I *know* what the "floor" of pricing is: It's 10¢ / GB. So the actual cost, from left to right, is 10¢, 25¢, $1, $2. OK, OK -- a few handful of cents more for bandwidth transfer, but it comes down to ... not much. So, dear web app provider, please don't over value the storage you are so graciously marking up in price.</p>
<p>And in fact, offering document storage in your web app is actually a *pain in the a$$*. You have files on your desktop, you have files attached to certain messages in Basecamp, in you have file revisioning (or whatever) in web app X. It's the forwarding documents over email problem all over - which is the newest copy, where is the file, who can edit the original, etc. Let me give you an example.</p>
<p>At <a href="http://bootuplabs.com" title="Bootup Labs - startup venture funding and incubator in Vancouver">work</a>, we're happy users of&nbsp; <a href="http://batchblue.com">Batchblue's Batchbook</a> - it's CRM a bit like <a href="http://highrisehq.com">37 Signals' Highrise</a>, with some niceties. One of the things you can do is forward email into it, including with attachments, and it will sit in there. So, a workflow where someone sends you a presentation, that you'd like attached / organized with that person, works really nicely. Except, when I want to actually read that presentation, I have to download it to my computer, and read it there. Every other person in my work group that wants to read it? Also has to separately and manually download it. Same goes for editing. Download, edit, re-upload.</p>
<p>So, we stick that document in Dropbox. And it gets synced automatically, and everyone has it on their desktop, easy to read in full binary document format, be it Word, Powerpoint, or whatever. And everyone can add notes, or edit it as needed. That's how I expect seamless cloud storage / document sharing to work.</p>
<p>Here's my call to action:</p>
<p><strong>When you're designing your next web app, please allow me to enter my existing Amazon S3 or Dropbox account as part of setup.</strong></p>
<p>Call it "<em>Bring your own Storage</em>", and lower your prices appropriately.</p>
<p>P.S. Of course, there is a <a href="http://drupal.org/project/dropbox/">Dropbox API module for Drupal</a> already.</p>
