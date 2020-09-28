--- 
layout: post
title: Google Apps and SXIP Access Identity and the Google Platform
created: 1172189216
categories: 
- Web 2.0
- Open Source
- Vancouver
- SXIP
- Salesforce
- OpenID
- identity
- Google Apps
- Google
---
<p>So, everyone is writing about the <a href="http://www.google.com/support/a/bin/answer.py?answer=60217">Google Apps Premier Edition</a>. Lots of partners have announced services that integrate with Google Apps today -- see the <a href="http://www.google.com/enterprise/gallery/index.html">Google Enterprise Solutions</a> gallery for what&#39;s available today.</p><p>I&#39;ve complained before about <a href="/blog/bmann/googles-identity-infrastructure-is-messed-up-and-no-one-is-talking">Google&#39;s messed up identity system</a> (it&#39;s not fixed yet). And it looks like SXIP is now doing the same thing that it provides for Salesforce: identity management.</p><p>I&#39;ve pinged the folks at SXIP to find out more. Their <a href="http://www.sxip.com/press_releases-Sxip_Identity_Delivers_OnDemand_Identity_Management_for_Google_Apps">press release</a> points to <a href="http://www.sxip.com/sxip_access_google">SXIP Access</a>, which is their, dare I say it, &quot;previous&quot; solution vs. the OpenID bandwagon? Or maybe not?</p><p><strong>Update:</strong> I got the scoop from Lori Pike at SXIP: &quot;At this point in time there&#39;s no relation between [SXIP Access] and OpenID or SXIP 2.0/DIX.&quot; -- and likely there will be a blog post that explains a bit more. </p><p>At Bryght, we built a <a href="http://drupal.org/project/sxip">SXIP module for Drupal</a>. <a href="http://walkah.net">James</a> is building out the <a href="http://drupal.org/project/openid">OpenID client and server modules</a> for the 2.x version of the standard. Lots of identity stuff still in the mix here...I&#39;ve got lots of ideas swirling in my mind, as you should be able to tell by the scattered nature of this post.</p><p>OK, final thought: I mentioned Salesforce, who have App Exchange. I have long been expecting Google to add it&#39;s own shared contact system to complete it&#39;s Microsoft Exchange-killer. But now, they don&#39;t have to: they&#39;ve got this shared platform that anyone can deploy connector apps to. And the most highly critical bits -- email and calendar -- are maintained by Google, so this limits risk for adopters.</p><p>What is interesting to me is the potential for open source here. Will Google allow connectors and solutions that are &quot;free&quot;? Can you connect to other solutions ONLY if you pay for a Premier edition? Google as platform is now a reality...this definitely changes things. </p>
