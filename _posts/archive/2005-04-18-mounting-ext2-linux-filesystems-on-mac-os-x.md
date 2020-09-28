--- 
layout: post
title: Mounting EXT2 Linux filesystems on Mac OS X
created: 1113808487
categories: 
- "*nix"
- E-smith
- Mac
- EXT2
- Linux
- ext2fsx
- EXT3
- "*nix"
- E-smith
- Mac
---
<p>
	I recently decommissioned a Linux (<a href="/e-smith">e-smith</a>, to be exact) server at home. Its main job was to <a href="http://gallery.sf.net" title="The Gallery project is still the best way to work with large amounts of pictures if you really want to host them yourself">store pictures</a>, and now that I&#39;m using Flickr, there was no need to have it sitting in our living room.</p>
<p>
	But, there are a ton of pictures on there that still needed to be taken off. Gigs of pictures. Which are just generally a pain to transfer over the network.</p>
<p>
	I have an external Firewire enclosure for IDE hard drives, so I thought I would experiment in trying to get the Linux file system (EXT2) mounted on Mac OS X. Long story short, after much Googling, I found <a href="http://sourceforge.net/projects/ext2fsx/">ext2fsx</a>. Like many Mac applications, it &quot;just worked&quot; and is really user friendly.</p>
<!--break-->
<p>
	<img align="left" alt="ext2fsx System Pref Icon" src="/sites/bmannconsulting.com/files/syspref_extfsx.jpg" /></p>
<p>
	After you install the package, it adds a cute little icon to the &quot;Other&quot; section of your System Preferences. That&#39;s it. That&#39;s pretty much all you need to know to get Linux disks mounting on OS X.</p>
<p>
	All the command line tools are installed as well, and I did actually have to run the <code>fsck</code> command to fix some problems with the drive I had, but generally you just need to hit one of the three buttons in the control panel:</p>
<p>
	<img alt="ext2fsx Control Panel" src="/sites/bmannconsulting.com/files/ext2fsx_cp.jpg" /></p>
<p>
	So, highly recommended!</p>
<p>
	Note: ext3 is a journaled version of ext2, and this utility works fine with that as well.</p>
