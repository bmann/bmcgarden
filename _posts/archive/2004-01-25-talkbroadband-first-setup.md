--- 
layout: post
title: TalkBroadband - First setup
created: 1075103880
categories: 
- VoIP
---
<p>This is my first post about using the service after I <a href="http://www.bmannconsulting.com/node/view/795">described it and signed up</a>. I couldn't wait until tomorrow morning, so I got it all setup and working tonight.</p>

<p>Read on for this initial setup, with a couple of details on port-forwarding.</p>

<!--break-->

<p>Since I'm trying to set things up in a non-standard way (because of the server that I use as a router) I <strong>don't</strong> want to put the gateway where it will be NAT'ing the rest of my network.</p>

<pre>
Cable Modem -- Server -- Switch -- DVG, other computers
</pre>

<p>From the <a href="http://support.dlink.com/faq/view.asp?prod_id=1416&question=DVG-1120M%20/%20DVG-1120S">D-Link tech support page</a>, the DVG is definitely web-accessible.</p>

<p>Later…</p>

<p>Well, that was pretty easy. It looked at first as if the red status light was flashing, and that the DVG wasn't going to work behind my e-smith server. I just left it alone for a while since I needed to do some research and was busy with some other stuff. When I went back to check, the green light was on, and I could receive calls no problem.</p>

<p>I never did manage to get into the web interface. Apparently the default address is <code>192.168.15.1</code>. Hmm. This doesn't make a whole lot of sense, since <code>.2.1</code> or <code>.1.1</code> would be the standard ones, especially for a <acronym title="Network Address Translation">NAT</acronym> router. I set my computer to be in the proper subnet, but the page never came up.</p>

<p>Then I had the brain flash that the site is probably only visible from the internal port (labeled "Ethernet"). I only have the WAN connector plugged in, since the DVG is behind my switch and server with nothing else attached to it. I'll test this hypothesis later.</p>

<p>So, outgoing calls work great -- made a call to my cellphone (the call display appended a "1" to the beginning of the number) and to my parents' land line. An incoming call test to my number bounced me to call answer box (a generic message -- I don't remember what it said) but I <em>thought</em> I had it set to forward to my cellphone.</p>

<p>I figured as much, since my server would be the publicly visible IP address. I looked up the <a href="http://wlanresearch.com/VoIPTCPUDPPorts.htm">ports used for VoIP</a> and found that <acronym title="Session Initiation Protocol">SIP</acronym> uses the following:</p>

<blockquote>
<ul>
<li>Either the UDP or TCP port for the signaling to port 5060.</li>
<li>RTP audio stream to UDP port 16384 through 32767.</li>
</ul>
</blockquote>

<p>I set my server to forward the appropriate port ranges, and everything worked great. It should be relatively easy to do the port-forwarding on most home routers. If you're not running a server behind your router, you could also choose to put the DVG into the DMZ or virtual server position -- all ports that are not specifically forwarded are then forwarded to it by default.</p>

<p>More feedback about voice quality and other issues as I do some testing over the next few days.</p>

<p><strong>Update:</strong> apparently, Primus TalkBroadband uses MGCP, <em>not</em> SIP. My setup worked because SIP and MGCP use the same ports for RTP streaming. I don't have the signaling ports explicitly forwarded, but it seems to work without it.</p>

<blockquote>
For MGCP version 1.0
<ul>
<li>MG and CA signaling to MG through UDP port 2427 and CA through UDP port 2727.<br>
<em>Note: This is because some CAs have the MG functionality built in them.</em></li>

<li>RTP audio stream to UDP port 16384 through 32767.</li>
</ul>

<p>Note: RTP port selection is MG specific. Depending on the number of voice ports on the MG, the RTP port range is selected. It does not go as high as 32767 and the range can be as small as 256.</p>
</blockquote>

<p>When <a href="http://www.bmannconsulting.com/node/view/827">talking with Andy from TalkBroadband tech support</a>, he did say that the configuration web page is not currently locked. I mentioned my suspicions that it can only be accessed from the internal Ethernet port, and he noted that down. Apparently there are internal discussions going on about whether or not to lock down that page. I passed on the feedback that it is likely that many early-adopters like myself wouldn't use the service if it couldn't be setup in a non-standard way, which might in some cases require access to that page.</p>
