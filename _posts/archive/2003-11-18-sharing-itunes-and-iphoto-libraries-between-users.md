--- 
layout: post
title: Sharing iTunes and iPhoto libraries between users
created: 1069209960
categories: 
- iTunes
- iPhoto
- sharing
- Mac
- iPhoto
- iTunes
- sharing
- file upload
- YouSendIt
- Mac
- file upload
- iPhoto
- iTunes
- sharing
- YouSendIt
- Mac
- file upload
- iPhoto
- iTunes
- sharing
- YouSendIt
- Mac
---
<p><strong>Problem: <em>You want all users on your machine to share an iTunes and iPhoto library</em></strong></p>
<p>Using just the Finder and some aliases, this is fairly easily accomplished.</p>
<p><!--break--></p>
<p><strong>Sharing iTunes</strong></p>
<p>For iTunes, this is relatively simple. Make sure iTunes is closed. Now, move your existing iTunes folder (the one you want to share -- located at <code>/Users/[username]/Music/iTunes</code>) to <code>/Users/Shared</code>.</p>
<p>Select the iTunes folder that is in the Shared location and Get Info (Command-I) on it. In the Ownership &amp; Permissions section, change everything to Read &amp; Write, and click "Apply to enclosed items".</p>
<p>Next, make an alias of the folder, move it back to your <code>~/Music</code> folder, and remove the "alias" string from the name. Repeat this step for all users that you want to have access to this shared library. You will need to delete their existing iTunes folder (which should be empty -- move or do a <a href="https://www.yousendit.com/">file upload</a>&nbsp;of any music to the Shared folder).</p>
<p><strong>Sharing iPhoto</strong></p>
<p>You can follow the same process as for the iTunes library, only the folder is called <code>iPhoto Library</code> and is located in the <code>~/Pictures</code> folder.</p>
<p>However, this does not completely work. The link listed under resources describes modifying iPhoto to change permission settings, but it does not work completely either: both users may view all the photos, but there are permission errors related to importing images.</p>
<p><a href="http://www.macosxhints.com/comment.php?mode=display&amp;sid=20030925091034677&amp;title=Sorry%2C+doesn%27t+%28completely%29+work%21&amp;type=article&amp;order=&amp;pid=30078">A comment on the Mac OS X Hints article</a> suggests running a cron job to reset permissions. This would work, but isn't a very elegant solution.</p>
<p><strong>Resources</strong></p>
<ul>
	<li><a href="http://www.macosxhints.com/article.php?story=20030925091034677&amp;query=share+iphoto">Share iPhoto Libraries</a>: MacOSXHints</li>
	<li><a href="http://www.malcolmadams.com/itunes/itinfo/sharedlib.shtml">How to share… (Doug's AppleScripts, Paul Withey)</a>: This is a much longer, more detailed description of essentially the same thing -- it seems to work perfectly under 10.2, but for Panther (as I mention above) importing by both users has permissions problems</li>
</ul>
