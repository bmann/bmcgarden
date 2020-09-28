---
title: Automatic WordPress Backup using Amazon S3
---
<p>I mentioned the <a href="http://www.webdesigncompany.net/automatic-wordpress-backup/">Automatic WordPress Backup plugin</a> briefly in my post about Standing Cloud. I've now installed and configured it, and aside from a few UI issues, it's great.</p>
<p>You'll need an [[AWS]] / [[Amazon S3]] account to get started. Grab your access key and security key from the security credentials part of your account. Download / install the backup plugin (here it is <a href="http://wordpress.org/extend/plugins/automatic-wordpress-backup/">on wordpress.org</a> - search inside WP for "automatic wordpress backup" and it should come up).</p>
<p>You choose what to backup. You really do want to check all the boxes -- your database, all your files, plugins, themes, uploaded content, etc. On the site in which I have it installed, each backup is about 100MB.</p>
<p>Backups are kept for a month and then deleted, and monthly backups are kept for a year. At 100MB / backup, that's about 3GB (plus a bit more for keeping those monthly backups). At Amazon S3's <a href="http://aws.amazon.com/s3/pricing/">pricing</a> of 15¢ / GB, that's.... under 50¢ / month to have your site backed up every single day.</p>
<p>You can restore directly from within the interface as well, so this is a pretty turn key system. The UI is all in one page and a little clunky, and I did make some comments on what could be improved:</p>
<ul>
	<li>In general, I would split the one big page into several tabs. A backups tab, a restore tab, and so on.</li>
	<li>if you add a progress indicator, or in general display a floating message that says “backup in progress”, then people will understand that a backup is happening.</li>
	<li>I would also do an immediate check against the access key / secret key and put in a green checkmark to indicate that it has connected correctly – with the secret key hidden, I’m always unsure if I’ve cut / pasted it correctly.</li>
</ul>
<p>Of course, what about <a href="http://vaultpress.com">VaultPress</a>, the commercial service? Well, in beta, they're charging $15 / month per blog at the Basic level, $40 / month for Premium. Or, um, 30x - 80x more expensive than doing it yourself with this plugin and Amazon S3. Their FAQ says that they are also doing security monitoring -- aka figuring out when your blog is hacked. And yes, most people are going to have to spend some time figuring out the Amazon interface and so on. But I really can't see how they can keep pricing at this level with this kind of free plugin available.</p>

<p>The <a href="http://drupal.org/project/backup_migrate">Backup Migrate</a> and <a href="http://drupal.org/project/backup_migrate_files">Backup Migrate Files</a> module are the equivalent solution for Drupal, although I've always had trouble getting the files version to work with its PEAR dependency.</p>
<p><strong>Update:</strong> <a href="/sillygwailo" class="internal-link">Richard</a> let me know that there is a <a href="http://drupal.org/node/715470">patch that fixes Backup Migrate Files</a>. Excellent, thanks!</p>
<p>Are you backing up your site automatically? Amazon S3 and plugins like those above make it automatic and inexpensive.</p>
