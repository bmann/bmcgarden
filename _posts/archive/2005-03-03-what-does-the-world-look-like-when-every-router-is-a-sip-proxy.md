--- 
layout: post
title: What DOES the world look like when every router is a SIP proxy?
created: 1109871685
categories: 
- VoIP
---

<p>Alec Saunders is experimenting with <a href="http://sipath.sourceforge.net">SIPatH</a>, a <acronym title="Session Initiation Protocol">SIP</acronym> proxy that runs on a $50 Linksys WRT-G router. Here's what his rules for the future of telecom are:</p>

<blockquote>
<ol>
<li>Your PSTN connectivity is outsourced to the lowest bidder.  The only calls you pay for are calls that terminate on the PSTN.</li>
<li>Your &quot;telephone number&quot; is simply a SIP address terminating on your local SIP proxy. To call me, you use your SIP client to reach alec@saunders.com - the SIP proxy I have at home.</li>
<li>The telephone network, as we know it, ceases to exist.  Telephony is nothing more than an embedded application running on a common transport.</li>
</ol>
<cite><a href="http://radio.weblogs.com/0111520/2005/03/02.html#a916">Alec Saunders .LOG</a></cite>
</blockquote>

<p>He also points out <a href="http://www.toyz.org/mrblog/archives/00000186.html">Mr. Blog</a>, talking about running <a href="http://lestblood.imagodirt.net/archives/83-Asterisk-on-OpenWRT.html#extended">Asterisk on the same router</a> (where Asterisk is a full-fledged IP-PBX).</p>

<p>I suppose I should stop being amazed, but we're not quite there yet. I had a quick look at both projects, and they would both take more fiddling than I'm willing to deal with at this point. However, since they are running on commodity home networking gear, it means we're not more than a year or so away (less?) from having a shippable product that is pre-installed and relatively plug and play. In the meantime, I'm still looking for a good PSTN termination provider in Canada.</p>
