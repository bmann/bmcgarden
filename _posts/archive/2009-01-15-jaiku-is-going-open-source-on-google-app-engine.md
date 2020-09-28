--- 
layout: post
title: Jaiku is going open source on Google App Engine
created: 1232013556
categories: 
- Google
- Jaiku
- Jaiku Engine
- microblogging
- Google App Engine
- OAuth
- Presently
- Identi.ca
- Montreal Startup Fund
- Yammer
- Stowe Boyd
- Open Source
- Web 2.0
---
<p>As <a href="http://google-code-updates.blogspot.com/2009/01/changes-for-jaiku-and-farewell-to.html">announced on the Google Code blog</a> / <a href="http://www.jaiku.com/blog/2009/01/15/were-going-open-source/">cross-posted to the Jaiku blog</a>, Jaiku is going open source:</p>
<blockquote>
<p>As we mentioned last April, we are in the process of porting Jaiku over to Google App Engine. After the migration is complete, we will release the new open source Jaiku Engine project on Google Code under the Apache License. While Google will no longer actively develop the Jaiku codebase, the service itself will live on thanks to a dedicated and passionate volunteer team of Googlers.     With the open source Jaiku Engine project, organizations, groups and individuals will be able to roll-their-own microblogging services and deploy them on Google App Engine. The new Jaiku Engine will include support for OAuth, and we're excited about developers using this proven code as a starting point in creating a freely available and federated, open source microblogging platform.</p>
</blockquote>
<p>The rest of the Google Code announcement actual mentions the end of <a href="http://dodgeball.com">Dodgeball</a> (also similar to Jaiku and <a href="http://brightkite.com">Brightkite</a>) plus the <a href="http://editor.googlemashups.com/">Mashup&nbsp;Editor</a> (which I had never heard of). Technically, the Mashup&nbsp;Editor is also moving to the App Engine infrastructure.</p>
<p>I had heard rumours of the coming open source nature of Jaiku, but didn't think it would extend to Google itself essentially not further developing it. There has been talk of a tightening of focus, which is fine, but I think real time, Jaiku-like services (and really, Jaiku was first ... Twitter, Friendfeed, etc. came later) are going to become more important, not less.</p>
<p>The open sourcing of Jaiku should make one wonder about the <a href="http://gigaom.com/2009/01/14/identica-gets-funding-to-make-open-source-twitter-variant/">recent funding for Identi.ca</a>. I think what the Montreal Startup Fund guys are doing is fantastic, but don't know that I agree with putting money into open source projects before they've shown real traction.</p>
<p>That funding link points to a GigaOm post that also points to Twitter for Enterprise &quot;clones&quot; <a href="http://yammer.com">Yammer</a> and <a href="http://present.ly">Presently</a>. I like both of those tools, and think they work great for internal / group communicatons. <a href="http://www.stoweboyd.com/message/2008/12/presently---cre.html">Stowe Boyd's write up of Presently</a> is what made me go try it, plus we had a need for shared / private groups for Bootup Labs.</p>
<p>So, the open sourcing of Jaiku is one thing. The BIG thing is that this allows turn key public / private microblogging on a scalable infrastructure. No fail whale, you just get more resources via the underlying Google App Engine. And by turnkey, I mean anyone with a Google Apps for Domains account can follow a few steps to run their own instance, on their own domain.</p>
<p>Oh right, and by the BIG thing, I mean that this instantly catapults microblogging into a fully federated system: I set up jaiku.bootuplabs.com, which can federate with all the other Jaiku instances on Google App Engine. It's open source, so allowing one to map identities to Twitter, Identi.ca, or other systems is certainly possible as well. Or, as Presently does it, by pre-pending a special tag for posts you want to show up on other systems.</p>
<p>OK, I don't know if that last bit is true, I'm just hoping it is: will federation be turned on out of the box? Or an option? In any case, it's open source, so it would definitely be possible to add this feature.</p>
<p>One final question I have is where the centralized discussion of future features / development / etc. for Jaiku Engine?</p>
<!--break-->
<p>I guess a code.google.com site will be going up, in the meantime there is the <a href="http://getsatisfaction.com/jaiku/">Get Satisfaction</a> site. If we can, it might be useful to start a new &quot;product&quot; there called Jaiku Engine to differentiate it from jaiku.com (which theoretically will stay up).</p>
