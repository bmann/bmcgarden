--- 
layout: post
title: Site specific browsers for mobile?
created: 1216496984
categories: 
- SSB
- Fluid
- Prism
- Tim Bray
- Dean Bubley
- Roland Tanglao
- iPhone
- Wireless, Cellular, and Mobile
---
<p>I'm catching up on some mobile-related blog reading today, and was spurred to write something by <a href="http://www.tbray.org/ongoing/When/200x/2008/07/18/Mobile-Net-Gloom">Tim Bray's Mobile Blues</a> and <a href="http://disruptivewireless.blogspot.com/2008/07/great-article-on-web-vs-native-mobile.html">Dean Bubley's re-post</a> of an <a href="http://www.dw2-0.com/2008/07/mobile-development-in-hurry.html">article by David Wood</a>. (And thanks to <a href="http://www.rolandtanglao.com">Roland's</a> <a href="http://www.google.com/reader/shared/02230306742891645763">Google Reader Shared Items</a>, where I am getting a wealth of mobile and food related links)</p>

<p>Canada (and the world in general) is caught up in a storm of mobile imaginings based on the launch of the 3G iPhone. Recent results of app sales potentially point to a future where carriers *don't* have a chokehold on the mobile handset experience: for the first time, your average non-technical end users can easily buy and install applications for your mobile fun. Except, of course, it's just another kind of walled garden, just one run by a computer company instead of a carrier.</p>

<p>Tim in particular has issues with that, as well as with having to learn yet another development environment to program native apps for the iPhone:</p>

<blockquote>
<p>But there’s a little problem and a big problem. The little problem is that I don’t wanna learn Objective-C and I don’t wanna learn a whole new UI framework. I acknowledge that lots of smart people think Objective-C and Cocoa are both wonderful, and quite likely they’re right. I don’t care. I’m lazy; I know enough languages and enough frameworks. You’re free to disapprove, but there are a whole lot of people like me out there.</p>

<p>The big problem is this: I don’t wanna be a sharecropper on Massa Steve’s plantation. I don’t want to write code for a platform where there’s someone else who gets to decide whether I get to play and what I’m allowed to sell, and who can flip my you’re-out-of-business-switch any time it furthers their business goals. …</p>
</blockquote>

<p>OK, points taken. You don't *have* to learn another programming environment, but every experience I've had with Java on every single phone I've ever owned has been .... terrible. Use Java if you want to quickly prototype an app for your enterprise ... but the usability and UI for the average end user, never mind the install process, is terrible. Most people go to native platform code for that final bit of polish (IF that polish is needed for your target market).</p>

<p>I don't have much to say on the locked platform aspects: you make your choices. In some ways, writing native apps for *any* platform is a level of lock in. That is, shouldn't we rail against OS X native only apps in the same way?</p>

<p>And here we finally come to the punchline hinted at by the title. For desktop operating systems, there are now a couple of site specific browsers (SSBs <a href="http://en.wikipedia.org/wiki/Site_Specific_Browser">[wikipedia link]</a>): you enter in the URL of a website / webapp and it is bundled into a separately clickable "application" that you can run like any other native program on your desktop. I use <a href="http://fluidapp.com">Fluid</a>, based on a WebKit engine, and there is also <a href="http://labs.mozilla.com/projects/prism/">Prism</a>, based on a Mozilla engine.</p>

<p>So, somewhere between widgets and full blown native applications, can an SSB engine for mobile operating systems reign supreme? Bubley's summarized thoughts on this are:</p>

<blockquote>
<p>…for <em>many</em> applications, Mobile Web will be the way to go, for ease of development, cross-platform support, rapid update and so on.</p>

<p>But for some the most <em>important and demanding applications</em>, there will still be a need for native development, even if it comes with a dose of pain.</p>
</blockquote>

<p>The mobile web, with advanced, compliant browsers available on smartphones like the iPhone or various Nokia phones, <strong>is</strong> the Internet. Various UI niceties and formatting to fit the screen factor aside, this is regular ol' HTML and AJAX, no new platform to learn here.</p>

<p>So, I'm looking forward to "Fluid for iPhone" or "Prism for Series 60": I can think of a web app developer or three that would be VERY interested in exploring a potentially very quick way to have apps on these smartphone platforms, without the full pain of native app writing. Actually, paging <a href="http://www.handimobility.ca">Handimobility</a> -- there might be a very nice business in there...</p>
<!--break-->
