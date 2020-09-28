--- 
layout: post
title: VoIP Presence System
created: 1043785440
categories: 
- VoIP
- IMPP
---
<p>
	This idea came about from thinking about the uses of a voice over IP (VoIP) system at university campuses, especially when married to instant message and presence features. Basically, your &quot;identity&quot; is matched to your &quot;phone number&quot;. By default, your identity resides on your phone, in your dorm room. Might even have the situation where multiple &quot;identities&quot; are mapped to the same phone -- perhaps the shared phone in the common area (where 4 students share housing -- not for an entire dorm). Even a dorm room with 2 students could share one phone, but have 2 identities. You might even need to authenticate yourself to use (or answer) calls, although some dorm roomies might say &quot;let identity B [my roommate] answer calls for me&quot;. Now, that&#39;s just the extrapolation.</p>
<p>
	My main idea was that you could logon to the presence/voice/multimedia system with a soft client from elsewhere, say from your laptop in the library. Your identity would actually be &quot;logged off&quot; your main phone in your room. Like a regular phone, you could choose to accept calls, or send them to voice mail -- or in the ideal SIP world, accept the call, but try and negotiate an IM session instead (because you&#39;re in the library, and can&#39;t talk). This functionality is already present in today&#39;s IM sessions -- if you log into your account from a 2nd device when you&#39;re already logged in elsewhere, the 1st device is kicked off (there is only one &quot;you&quot; at any one time). I haven&#39;t read over the relevant RFC&#39;s in a while, but the <a href="http://www.ietf.org/html.charters/impp-charter.html">Instant Messaging and Presence Protocol (IMPP)</a> working group is the place to look.</p>
