--- 
layout: post
title: What is a person connected to?
created: 1054532100
categories: 
- Social Media
---
I've still got Don's command to "start rocking" ringing in my ears.

I was going to call it a night, when a little voice said: Self, you have this interesting collection of pictures that you have cycling on your desktop -- why not implement a little "picture of the day" function and start displaying them?

From there, I had the idea for FOTD -- Friend/Face of the Day, a.k.a. an alternative to Blogrolls. Basically, a picture that links to a bunch of information about this face. Remember this part, it will come back again.

In this first iteration, the information is put into a standardized format (such as the sample, XML-ish one I've put together at the end of this post). Sure, it could be FOAF. Or maybe not... This info is hosted by the friend themselves -- it is up to the local site to decide how/what to display.

In the second iteration, we have tools (like <a href="http://www.drupal.org">Drupal</a>, which runs this site, or MovableType, or whatever...) which allow us to post our "face" onto comments, stories, or maybe even just the front page. It says "Hi, I stopped by and had a look around". Because these sites are virtual gathering places, watering holes, places where everyone knows your name...up until now, not your face, though...

So, a two way connection is formed: readers stop by, show their face. A crowd gathers, a crowd of faces. Maybe there is a "Who's New" section, maybe there is a "Stopped by Today" section. Wow -- a crowd is gathering!

And then, maybe, we want to randomly select someone as a FOTD of the day. So, what do we want to know about this person? First of all, it is up to the person themselves to decide what to let others know. They host their own, um, friend descriptor (it's not a profile, it's more like an email sig).

So let's walk through my little description, very specifically NBAF (Not Based on Any other Format).

Well, my name and any nicknames, etc. are probably best to get out of the way first.

<pre>	< name >
		< first >Boris< /first >
		< middle >Frederik< /middle >
		< last >Mann< /last >
	< /name ></pre>Now some dates that are important to me

<pre>	< dates >
		< date type="birthday" year="1975" month="02" day="22" alt="Born in Vancouver" / >
		< date type="misc" year="1979" title="Moved to Bowen Island" / >
< date type="misc" year="1995" month=12" alt="My anniversary with Kate" / >
	< /dates ></pre>A whole bunch of resources, which I've labeled as 'personal'

<pre>	< resources label="personal" >
		< link type="website" href="http://www.bmannconsulting.com" title="B. Mann Consulting" alt="My personal home page" / >
		< link type="website" href="http://www.bmannconsulting.com/module.php?mod=blog&id=1&all=1" title="Personal Blog" / >
		< link type="image" href="http://www.bmannconsulting.com/images/boris.jpg" / >
		< link type="misc" href="http://www.homestarrunnner.com/sbemail58.html" alt="Favourite Strongbad Episode" / >
		< link type="misc" href="http://gallery.bmannconsulting.com" title="Personal Photo Gallery" / >
	< /resources ></pre>Some other resources that I want to label as 'work'
<pre>	< resources label="work" >
		< link type="website" href="http://www.phenomenalsolutions.com" alt="Phenomenal Solutions" / >
		< link type="profile" href="http://www.zerendipity.com/profile.aspx?id=111" alt="Zerendipity Profile" / >
	< /resources ></pre>Of course, with both 'personal' and 'work', I could list other resources that in fact model relationships. Perhaps a link type of "relationship" (contact? associate? connection? not sure what would make people most comfortable...) with which I could point to profiles...

<pre>	< link type="relationship" href="http://www.zerendipity.com/profile.aspx?id=59" title="Andrew Jones" / ></pre>...or maybe indicate my approval of other people and/or their work (or disapproval, like my recent dislike of <a href="http://www.canadiantire.ca">Canadian Liar</a>, who will invariably send you to another store to buy a fishing license, even though they have no idea if the other store actually sells them or not...and their specials are always sold out):

<pre>	< link type="recommend" href="http://www.docuverse.com/blog/donpark/" title="Don Park's Blog" / ></pre>Chris Corrigan talked about <a href="http://www.chriscorrigan.com/miscellany/bijournal/blogger.html">'People Blogging Places'</a> -- very specifically talking about their environment, their community. He does it too, and it's kind of how I found him -- he lives where I grew up, on Bowen Island. I'm proud of it, and I think it is part of what makes me what I am, so I want that in my description.

<pre>	< location label="hometown" >
		< neighbourhood >Millers Landing Road - Seven Hills< /neighbourhood >
		< city >Bowen Island< /city >
		< province >British Columbia< /province >
		< country >Canada< /canada >
		< link type="map" href="http://www.multimap.com/map/browse.cgi?X=-13737500&Y=6300000&scale=500000&coordsys=mercator" alt="Multi Map" / >
	< /location ></pre>Now I live in Ottawa, in a neighbourhood called Centretown. It's a funky little area, with lots going on. It's in.

<pre>	< location label="home" >
		< neighbourhood >Centretown< /neighbourhood >
		< city >Ottawa < /city >
		< province >Ontario< /province >
		< country >Canada< /country >
		< link type="map" href="http://www.multimap.com/map/browse.cgi?X=-8426250&Y=5656250&scale=50000&coordsys=mercator" >
	< /location ></pre>I hope that gets some ideas rockin'.
