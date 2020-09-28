--- 
layout: post
title: "Distributed commenting: Disqus, Echo and IntenseDebate"
created: 1278092773
categories: 
- Web 2.0
- Social Media
tags:
- comments
- Echo
- Disqus
- IntenseDebate
- Posterous
- JanRain
- identity

---
<p>
	I start a lot of my posts these days with a reblog using <a href="http://posterous.com">Posterous</a>. Thus, a lot of permalinks end up over on <a href="http://asides.bmannconsulting.com">my &quot;asides&quot; blog</a>, because a lot of the &quot;comment&quot; activity ends up either over there, or on Twitter.</p>
<p>
	My particular dual website problem might not be solved by this, but it&#39;s clear that keeping track of the discussion around blog posts is very much a distributed issue. Don&#39;t even get me started on the &quot;Share with Note&quot; in Google Reader that leaves comments stranded over in Reader where post authors are unlikely to to see them :P</p>
<p>
	The three big systems that I&#39;m aware of at the moment are <a href="http://disqus.com">Disqus</a>, <a href="http://aboutecho.com">Echo</a>, and <a href="http://intensedebate.com">IntenseDebate</a>.</p>
<p>
	On the <a href="http://blog.bootuplabs.com">Bootup Labs</a> and <a href="http://bootup.ca">Bootup Entrepreneurial Society</a> WordPress blogs, I went with IntenseDebate. It&#39;s my favourite system mainly because I know the <a href="http://automattic.com">Automattic</a> team and I trust them to do what&#39;s right for the web long term. Being part of Automattic also removes the (immediate) need to monetize heavily, so they can focus on features and support.</p>
<p>
	<a href="http://disqus.com">Disqus</a> is very similar to IntenseDebate. In fact, I think it&#39;s great that they were being developed at around the same time, because I think the teams competing against each other spurred development and features. Disqus is VC funded, and so is trying a number of different monetization strategies. They have a<a href="http://disqus.com/vip/"> paid VIP program</a>, although pricing isn&#39;t disclosed.</p>
<p>
	I found a great <a href="http://tomuse.com/comment-system-compare-wordpress-intense-debate-disqus/">compare and contrast blog post between Disqus and IntenseDebate that goes feature by feature</a>. At the time (May 2009), IntenseDebate didn&#39;t support Facebook or Twitter logins, although they added them both. I have a hard time telling the two systems apart - any passionate users of either system want to point out killer features (or missing ones)?</p>
<p>
	Echo is the only system without a free option: you can get a 30 day free trial and then switch to either a <a href="http://aboutecho.com/pricing.html">$10 or $100 month version</a>. Of course, it is fundamentally a very different system. While they do have &quot;JS Kit&quot; (their former name) accounts, this is very much de-emphasized in favour of only using distributed logins from other systems. As well, it aggregates &quot;comments&quot; from elsewhere - whether the comment is a link on Delicious, Friendfeed, Facebook, etc. etc. This has more in common with Trackbacks, but in the Echo system, it is highly integrated and seems more natural than the other two that are &quot;comments first&quot;. Finally, Echo doesn&#39;t currently write back to the native comment system, using only a JavaScript plugin. This has implications for SEO, and implications for me really wanting to have my own copy of the comment should the service in the sky &quot;go away&quot; :P</p>
<p>
	On the Drupal side of things, only Disqus and Echo have plugins available, at&nbsp;<a href="http://drupal.org/project/disqus">http://drupal.org/project/disqus</a> and&nbsp;<a href="http://drupal.org/project/jskitcomments">http://drupal.org/project/jskitcomments</a> respectively. From a technology perspective, I like the real time nature of Echo and the general direction that it is heading -- it&#39;s almost like having Friendfeed embedded under each post. But, the JavaScript only plugin and the lack of free option for personal bloggers makes it a no go. Since there currently isn&#39;t an IntenseDebate plugin for Drupal, I&#39;m going to go with Disqus for now, even though I would rather support the Automattic team.</p>
<hr />
<p>
	<strong>UPDATE:</strong> I just realized after re-reading the Disqus module description, that it will *import* comments from Drupal, but it does not then write those comments back to the native comment system. So, in Drupal, we have zero options for a distributed comment system that writes back / syncs with native comments.</p>
<hr />
<p>
	Lastly, the interesting thing about all these comment systems is that in reality, they are about identity. Rather than using an account on one site, or commenting anonymously, it&#39;s about re-using identifiers from widely used systems. Whether it is the commenting profile itself, or a third party like Facebook or Twitter.</p>
<p>
	Since this is the case, tools like <a href="http://www.janrain.com/products/engage">Janrain Engage</a>&nbsp;(<a href="http://drupal.org/project/rpx">Drupal module here</a>) should also be considered if you are trying to &quot;solve&quot; getting more comments, and in particular more authenticated comments.</p>
<p>
	I&#39;m using it here on this site, and just turned off anonymous commenting to experiment more fully with it. This means it should be easy for you to use the &quot;native&quot; comments, but still allow people to easily login and start commenting. You do have to allow unmoderated account creation on the site you intend to use it.</p>
