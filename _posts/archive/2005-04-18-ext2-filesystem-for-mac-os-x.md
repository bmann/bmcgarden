--- 
layout: post
title: EXT2 Filesystem for Mac OS X
created: 1113808587
categories: 
- mac os x
- EXT2
- Mac
---
<p>
	Note: this is copied from the distribution of <a href="http://sourceforge.net/projects/ext2fsx/">ext2fsx on Sourceforge.net</a>. I couldn&#39;t find a copy online other than in the download, so have put it here for convenience.</p>
<div align="center">
	EXT2 Filesystem for Mac OS X<br />
	1.3<br />
	2004/08/02</div>
<p>
	&nbsp;</p>
<h2>
	Donations</h2>
<p>
	If you are interested in making a donation, please vist my Kagi Payment page. A minimum of US $10 is requested because of the fees Kagi charges. Please don&rsquo;t take this as a request for donations. Make a donation only if you want to, not because you feel you have to. Gifts from my Amazon wish list are also appreciated (and preferred).<br />
	<br />
	Kagi: https://order.kagi.com/?VN<br />
	Amazon: http://www.amazon.com/exec/obidos/registry/1UV8OJ9VKS9VV/<br />
	&nbsp;</p>
<h2>
	Requirements</h2>
<p>
	Mac OS X 10.2.0 through 10.3.x. Mac OS X 10.0.x, 10.1.x and 10.4.x or higher are not supported.</p>
<h2>
	ExtFS Manager</h2>
<p>
	ExtFS Manager is an OS X Preference Pane for managing Ext2/3 disks. From this pane you can set mount options for any Ext volume. The current options are:<br />
	<br />
	Don&#39;t Automount -- The volume will not be mounted automatically by the system.<br />
	<br />
	Mount Read Only -- When mounted, mount R/O.<br />
	<br />
	Enable Indexed Directories -- See &#39;Supported Features&#39; below.<br />
	<br />
	Ignore Permissions -- When checked, the filesystem will be mounted with only root permissions in effect. All other files will be accessible by any user.<br />
	<br />
	All options (except &quot;Enable Indexed Directories&quot;) can be temporarily overridden using &#39;/sbin/mount_ext2 -x&#39; followed by &#39;disktool -r&#39; to mount the volume.<br />
	<br />
	Note: You must be an admin user and /Library/Preferences must be writable by the admin group or changes made to the options will have no effect.</p>
<h2>
	ExtFS S.M.A.R.T. Hard Disk Monitor</h2>
<p>
	ExtFS Manager includes a utility that is designed to monitor your local ATA disk drives for impending problems. This is done by querying the drives for their S.M.A.R.T. status. S.M.A.R.T. is a built in feature of modern ATA disk drives that allows the drive to perform diagnostic tests on itself. The results of these tests can then be queried by applications.<br />
	<br />
	The ExtFS S.M.A.R.T. monitor is installed in your Login Items the first time you launch the ExtFS Manager preference pane. It will continually monitor your ATA drives for any S.M.A.R.T. warnings or errors and report those to you via an alert panel.<br />
	<br />
	If you do not want the S.M.A.R.T. monitor running, simply remove it from your Login Items and it will not be installed again.</p>
<h2>
	Using command line utilities</h2>
<p>
	The installation includes the full set of Ext2 command line utilities found in Linux; including newfs, fsck, debugfs, etc.. If you want to use these from Terminal, you may wish to add &quot;/usr/local/bin&quot; and &quot;/usr/local/sbin&quot; to your shell PATH variable for easy access. You may also wish to add &quot;/usr/local/share/man&quot; to your shell MANPATH variable for easy access to the man pages.<br />
	<br />
	If you need to operate on a corrupted disk image with one of the repair utils (fsck, debugfs, dumpe2fs, etc), you will need to attach the disk image via the command line util &#39;hdid&#39; with the &quot;-nomount&quot; option; this will prevent the automounter from trying to mount the disk image. After this, you can use the ext2 programs on the device returned from hdid. See &quot;Known Limitations&quot; for an example.</p>
<h2>
	Supported Features</h2>
<p>
	The OS X driver respects/implements the following inode flags (man chattr):<br />
	A -- (NOATIME)<br />
	a -- (append only)<br />
	i -- (immutable)<br />
	<br />
	Ext3 indexed directories are supported. Indexed directories are orders of magnitude faster than standard directories. The driver will auto-recognize and use these when present; if you wish to add support to an existing volume using Mac OS X, then the filesystem must be mounted with the -o index option (this can be enabled via the ExtFS Manager Preference Pane). Note: Indexed directories are backwards compatible with Ext2 filesystems, so you can enable them without worrying about breaking older filesystems (from Linux or Mac OS X).</p>
<h2>
	Known Limitations</h2>
<p>
	Volumes will fail to auto-mount if they are corrupted. The auto-mounter funs fsck (in verification mode only) before mounting a volume and if fsck fails, the auto-mounter won&#39;t even try to mount the volume. If you are having problems with volumes not auto-mounting, try running fsck_ext2 on the device. After any volume errors have been corrected, you can get the auto-mounter to try mounting the device again by running &#39;disktool -r&#39; from Terminal. Please note that the kernel will also fail to mount any filesystem R/W if it is not clean.<br />
	<br />
	If you re-format an existing partition as Ext2, then that partition may fail to automount in the future. This is because re-formating does not change the partition type in the partition header of the disk. Automounter uses this type as a &quot;hint&quot; when trying to find the right filesystem utility to use. Unfortunately, the &quot;hint&quot; is actually literal; automounter will find an incorrect filesystem utility based on the partition type and when that utility fails the probe phase, automounter will return an error without trying other filesystem utilities. There is no known way to change a partition type without re-formating the entire disk. (Amendment: Dan C. pointed out that pdisk can apparently alter the partition table without destroying other partitions. So you could drop a partition and replace it with a new type. I don&#39;t know if I trust this, so for now I&#39;ll leave this up to the intrepid user.)<br />
	<br />
	Renaming a volume in the Finder is only supported on 10.3.0 and later (not 10.2.x) . To change the name of a volume while running 10.2.x, you must use the Terminal program &#39;e2label&#39;. Example (using a disk image):</p>
<pre>
brian$ hdid -nomount Desktop/MyExt2Image.dmg</pre>
<pre>
/dev/disk1              Apple_partition_scheme         </pre>
<pre>
/dev/disk1s1            Apple_partition_map            </pre>
<pre>
/dev/disk1s2            EXT2        </pre>
<pre>
brian$ /usr/local/sbin/e2label /dev/disk1s2 &quot;My Image&quot;</pre>
<pre>
brian$ hdiutil detach /dev/disk1</pre>
<pre>
hdiutil: detach: &quot;disk1s1&quot; detached successfully.</pre>
<pre>
hdiutil: detach: &quot;disk1s2&quot; detached successfully.</pre>
<pre>
hdiutil: detach: &quot;disk1&quot; detached successfully.</pre>
<p>
	<br />
	Linux does not care what character encoding is used for directory entries (IOW, file names). Linux just treats the name as a byte stream with no interpretation done. If you are using non-ASCII characters in file names, there is no way to find out what encoding is used for a particular file (or the FS as a whole). The solution to this is to use UTF-8. This is what Mac OS X does. Unfortunatly, if you are not currently using UTF-8 in Linux, then your names will be mis-interpreted on Mac OS X and there is nothing that can be done to fix this.<br />
	<br />
	Block fragments are not supported!<br />
	<br />
	NFS export is not supported.<br />
	Boot/Root is not supported.<br />
	EXT3 journaling, extended attributes, and ACL&#39;s are not supported.<br />
	Quotas are not supported.</p>
<h2>
	Reporting a Bug</h2>
<p>
	Bug reports should be entered into the bug tracking system at<br />
	&lt;http://sourceforge.net/projects/ext2fsx/&gt;.<br />
	<br />
	Please include the following.<br />
	<br />
	Your name and e-mail address -- in case I need to contact you.<br />
	System Version (including build number)<br />
	Version of Ext2 FS for Mac OS X<br />
	A copy of your system log in /var/log/system.log.<br />
	A detailed description of what lead to the problem and how to reproduce it.<br />
	<br />
	If the problem is a kernel panic, please include a copy of the panic. Mac OS X 10.2 (or later) logs panic information to the /Library/Logs/panic.log file after the machine is rebooted.</p>
<h2>
	Credits</h2>
<p>
	Engineering: Brian Bergstrand, and Dan Kalowsky<br />
	<br />
	German Localization: S&ouml;ren Kuklau<br />
	<br />
	Tux&#39;n&#39;Tosh icons: Bandar Raffa &lt;http://www.sadeem.net/tux.html&gt;<br />
	<br />
	Special Thanks: Sam Vaughan</p>
