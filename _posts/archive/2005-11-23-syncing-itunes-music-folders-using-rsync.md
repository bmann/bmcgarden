--- 
layout: post
title: Syncing iTunes Music folders using rsync
created: 1132762951
categories: 
- rsync
- iTunes
- Mac
- Music
---
<p>
	Very much a work in progress. This took about 15min over a wireless connection, for 3000 songs on my Powerbook to the desktop machine. Shouldn&#39;t be used on anything other than 10.4 Tiger because the &quot;E&quot; flag is specific to that version, which keeps Apple resource fork information when copying.</p>
<p>
	rsync -rtE --progress iTunes/iTunes\ Music/ yourothercomputer.com:/Volumes/MaxtorBlue/Music</p>
<p>
	You&#39;ll be prompted for your password on the remote machine (assumes you have the same username on both machines).</p>
<ul>
	<li>
		r: recurse into directories</li>
	<li>
		t: maintain the time stamp on the files</li>
	<li>
		E: keeps Apple resource forks intact</li>
	<li>
		progress: scrolls by a list of transfers and how long they take</li>
</ul>
