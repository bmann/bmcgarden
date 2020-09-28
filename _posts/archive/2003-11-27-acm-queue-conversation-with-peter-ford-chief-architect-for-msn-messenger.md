--- 
layout: post
title: "ACM Queue: Conversation with Peter Ford (Chief Architect for MSN Messenger)"
created: 1069943340
categories: 
- IM
- VoIP
---
<p>Greg brought this article to my attention, which is an <a href="http://www.acmqueue.com/modules.php?name=Content&pa=showpage&pid=89&page=1">interview with Peter Ford</a>, the chief architect for MSN Messenger. The interview questions are asked by Eric Allman, chief technology officer and founder of <a href="http://www.sendmail.com/">Sendmail</a>.</p>

<p>I learned a few interesting tid-bits from the article, such as the fact that the newest versions of MSN Messenger are actually based around <acronym title="Session Initiation Protocol">SIP</acronym>, which is the standard that all newer VoIP implementations are based on as well.</p>

<p>Read on for the protocol battle and some quotes.</p>
<!--break-->
<p>So SIP is supported by Microsoft, Lotus, Sun, and Novell (in IM -- as I said, telecommunications companies are going to be using SIP as well, just not for IM at this point). I'll have to ask Dave and Trevor what Nortel is using for presence/IM. Also, although it wasn't mentioned, iChat AV is based on SIP. There still really don't seem to be any technical details on this, and does this mean that <acronym title="AOL Instant Messaging">AIM</acronym> (since it can talk to iChat users) is also based on SIP?</p>

<p>Here's the relevant information <a href="http://www.instantmessagingplanet.com/public/article.php/2226921">Instant Messaging Planet</a>, found at <a href="http://forums.osxfaq.com/viewtopic.php?t=6842">OSXFAQ</a>:</p>

<blockquote>
While it uses SIP to launch a multimedia session, iChat AV doesn't seem to function as a full-featured SIP client, however. Aside from receiving initiation requests in conjunction with AIM, the client can't initiate Voice-over-IP sessions using standard SIP INVITE messages -- for instance, those originating from a SIP phone.
</blockquote>

<p>So AIM is AIM, and SIP is handled separately for the voice and/or video.</p>

<p>On the other side of the fence, <acronym title="eXtensible Messaging and Presence Protocol">XMPP</acronym> (which is really just a standardized version of <a href="http://www.jabber.org">Jabber</a>) is being used by Intel, HP, Hitachi, Sony, and "more or less the entire open source world".</p>

<p>The trick between these two protocols is one of intended purpose. XMPP was designed from the ground up to support presence and other IM features. SIP, on the other hand, was actually designed to connect two end-points (hence "Session Initiation Protocol") -- passing media (eg. audio) is actually handled by <acronym title="Real Time Protocol">RTP</acronym> or <acronym title="Real Time Streaming Protocol">RTSP</acronym>.</p>

<p>In this case I'm (gasp!) actually going to side with Microsoft: I think SIP should be the basis for further development in the IM world, as it will also support voice and eventually video. But, instead of cloodging on presence onto the SIP spec, why not use XMPP alongside/encapsulated with SIP? Heck, this even leaves the door open for cool stuff like text-to-speech and speech-to-text: IM someone on their phone, and it could speak it to them. Call a deaf person and it gets translated to text.</p>

<p>A discussion about what happens to IM messages when you are offline was interesting -- mainly because <a href="http://www.icq.com">ICQ</a> (the first big IM network) has always supported this.</p>

<blockquote>
The current IM clouds really aren't built for that. By building smarter endpoints, it's pretty easy to get that kind of functionality. Then, also, in the MSN messenger network, we don't actually go peer to peer with text messaging. We always go through an intermediate system we call a switchboard. You could put something like a queuing mechanism there. We don't do queuing today.
</blockquote>

<p>Lots of good stuff in the article, although it seemed to me that Eric Allman could have challenged Peter Ford a lot more -- there wasn't a lot of confrontation on any of Ford's points.</p>
