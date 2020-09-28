--- 
layout: post
title: MovableType is the Windows of the Personal Publishing World
created: 1079717491
categories: 
- Drupal
- Drupal
- Personal Publishing
- Drupal
---
<p>Everyone is all a-twitter that <a href="http://www.movabletype.org/news/2004_03.shtml">MT 3.0</a> is about to come out of hiding. Am I biased because I use a <a href="http://www.drupal.org">different publishing system</a>? Probably.</p>

<p>But I maintain that MT has gotten to the top of the heap because of it's wide adoption. Much like Windows. Many people agree that OS X or even Linux is a technically superior operating system, but it's still Windows with the lion's share of the market. Much like MT.</p>

<p>So, herewith, a list of things that I don't like about MT.</p>
<!--break-->
<p>These are in no particular order. I've used MT (kicking and screaming), but am by no means proficient. These are my opinions, so you can disagree with them. Feel free to comment or otherwise <a href="http://www.bmannconsulting.com/feedback">let me know</a> if I get something factually wrong. And yes, I am talking about a default install.</p>

<ul>
<li><strong>Runs on Perl</strong>
<p>Perl is great for many things. It was used to build many of the first web applications. I still have many fond memories of <a href="http://stein.cshl.org/WWW/software/CGI/">CGI.pm</a>. Today, the CGI directory lock-down, the necessity for manually installing extra libraries, and the eclipse of Perl by other languages (notably PHP and Python) make it a pain to work with. Yes, this can and will cause a "my programming language is better" flame war.</p>
</li>
<li><strong>Anchor-based permalinks</strong>
<p>Also known as "individual pages for posts turned off by default". There are many <a href="http://www.bmannconsulting.com/node/view/952">Search Engine Voodoo</a> reasons why this is a bad thing. A big long page with lots of categorically-unrelated posts is not that great to link to. With comments on a separate page (see below), it keeps even more related content on a separate page. <a href="http://radio.userland.com/">Radio</a> is guilty of this as well.</p>
</li>
<li><strong>Static pages</strong>
<p>Basically, MT has you create an entry, then "publishes" it, turning it into a static HTML page. The downside of this is two-fold:</p>
<ol>
<li>Hard to include dynamic content</li>
<li>Increasing server load as content and/or comments increase</li>
</ol>
<p>Yes, there are some advantages to speed for really busy sites, since static pages can always be served faster than dynamic. But, I've heard of the comment system breaking down completely under heavy load. Drupal (for instance) implements database caching of pages for anonymous users.</p>
</li>
<li><strong>Pop-up comments</strong>
<p>Why? <em>Why?</em> What is the use case for having pop-up comments? It makes it harder for search engines to index, it's harder to read, and pop-ups are so 1998. <a href="http://www.brendonwilson.com/profile/" title="Brendon Wilson's Profile">Brendon</a> does a good job with comments in MT.</p>
</li>
<li><strong>Complicated, hard to use admin and posting system</strong>
<p>MT's backend is hard to use. I would not want to point <em>any</em> non-technical user at it. I find it confusing, and I consider it technical. I don't have a running install of MT kicking around anymore, otherwise I would break down its UI failings more thoroughly.</p>
</li>
<li><strong>Hard to install</strong>
<p>This is kind of related to running on Perl, since the most common hang up seems to be around missing libraries. Still, the necessity of putting files in different places (cgi-bin vs. main html directory) just makes it harder than other systems.</p>
</li>
<li><strong>No out-of-the-box template switching</strong>
<p>The default MT template is plain and ugly. The recent <a href="http://www.movablestyle.com/">Movable Style</a> website has a way to easily switch layouts. If someone downloaded and installed MT, is there a way to easily install a different template?</p>
</li>
<li><strong>Not free</strong>
<p>Let's not debate free. You can't use MT commercially without paying a licensing fee. Many other systems are true open source, allowing full modification and no payment to anyone.</p>
</li>
<li><strong>Comment spam</strong>
<p>No other system that I know of suffers from comment spam like MT does. Is it because it's the most popular system (again, like Windows)? Or is it because of failings in its technical architecture (again, like Windows)? I don't know the definitive answer, but I suspect it is a bit of both.</p>
</li>
</ul>

<p>What systems do I like? Depends on what you want to do. In any case, ease of installation and ease of use are two primary goals that always need to be satisfied.</p>

<p><a href="http://www.wordpress.org">Wordpress</a> is an excellent individual or blog-only application that has many standards-based features built in from the get-go. It falls down a bit with its media management, but is still the engine I recommend for people that just want a blog.</p>

<p><a href="http://www.drupal.org">Drupal</a> is my pick for advanced users, anyone that wants a community-based site, or as a content management system for business websites. Its base set of modules have everything included, its template system is flexible enough that you can build whatever you like, and its aggregation and feed-generating capabilities are without par.</p>

<p>I'm sure that MT 3 will address some of these issues. Like Windows, it may very well introduce a whole set of new ones.</p>

<p><strong>Related Links:</strong></p>
<ul>
<li><a href="http://cyberdash.com/node/view/231">cyberdash</a></li>
<li><a href="http://www.blogherald.com/archives/000601.php">Blog Herald</a></li>
<li><a href="http://www.rolandtanglao.com/archives/2004/03/20/movabletype_is_the_windows_of_blog_systems">Roland Tanglao</a> - Roland extends my analogy to say Drupal is like Linux and Wordpress might be like the Mac</li>
<li><a href="http://www.das-netzbuch.de/index.php?id=P1366">das Netzbuch (German)</a> - makes a further expansion: <a href="http://www.typekey.com/">TypeKey</a> == MSN Passport</li>
</ul>
