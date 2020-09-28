--- 
layout: post
title: First Mac OS X Trojan
created: 1081463980
categories: 
- Mac
---
<blockquote>
<p>Intego, the Macintosh  security specialist, has just released updated virus definitions for  Intego VirusBarrier to protect Mac users against the first Trojan horse  that affects Mac OS X. This Trojan horse, MP3Concept (MP3Virus.Gen),  exploits a weakness in Mac OS X where applications can appear to be  other types of files.</p>

<p>The Trojan horse's code is encapsulated in the ID3 tag of an MP3 (digital  music) file. This code is in reality a hidden application that can run  on any Macintosh computer running Mac OS X.</p>
<cite><a href="http://www.intego.com/news/pr40.html">Intego: Intego Announces Protection against the First Mac OS X Trojan Horse: MP3Concept</a></cite>
</blockquote>

<p>Is this a buffer overflow? As far as I know, there is nothing inside ID3 that gets "executed" -- it just gets read. Does this also happen when you drag and drop the file onto the iTunes application or dock icon? More questions than answers...</p>

<p><strong>Update:</strong> Jay Allen was asking the same questions I did, and then went a couple of hundred steps further and really dissected the Intego press release. He's kept his <a href="http://www.jayallen.org/journey/2004/04/mp3concept_a_mac_mp3_virus_or_hoax">post up to date</a> with all current information. Bottom line: this is much less of a problem than it sounds.</p>
