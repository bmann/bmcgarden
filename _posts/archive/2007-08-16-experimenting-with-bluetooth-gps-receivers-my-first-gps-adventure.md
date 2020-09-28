--- 
layout: post
title: "Experimenting with Bluetooth GPS Receivers: my first GPS Adventure"
created: 1187257005
categories: 
- Bluetooth
- geolocation
- GEtrack
- GPS
- gps logging
- GPS Photo Linker
- Nokia E61
- Series 60
- TomTom
- Wireless, Cellular, and Mobile
---
<p>So, I went on my first GPS adventure after work tonight. I was talking to <a href="http://www.rolandtanglao.com">Roland</a> about doing something for BarCamp Vancouver 2007, and he reminded me that <a href="http://radio.weblogs.com/0100115/">Cyprien</a> had a Bluetooth receiver to borrow. So, we swung by Cyprien's place and I was off to see if I could find the pieces to make this work. Thanks, Cyprien!</p>

<p>I specifically posted earlier about a <a href="http://bmannconsulting.com/blog/bmann/want-buy-gps-logging-device">simple GPS logging device</a> instead of a Bluetooth receiver. Bluetooth receivers allow you to hook up a PDA or your laptop and do various "on the go" GPS activities, usually involving directions and maps. But, I'm looking for something dead simple that a) just works and b) doesn't mean fiddling with / charging / carrying a bunch of other devices.</p>
<!--break-->
<p>Cyprien's device is a<a href="http://www.expansys.ca/d.aspx?i=141161">TomTom Bluetooth receiver</a> and I have a <a href="http://bmannconsulting.com/tags/nokia-e61">Nokia E61</a>. Next step was to find some logging software -- the Position, Navigator, and Landmark applications on the E61 do communicate easily with Bluetooth receivers...but they don't really do anything. Including logging out of the box seems like a no brainer. In any case, I had already done some research on <a href="http://del.icio.us/borismann/geo+series60">GPS related applications for Series 60</a>, with the listing of <a href="http://www.allaboutsymbian.com/software/all/GPS/">GPS apps at All About Symbian</a> being the most useful.</p>

<p><a href="http://www.mobile-j.de/snipsnap/space/Products/GETrack">GETrack</a> ended up being the simplest application specifically for logging. There are other apps that also do some map integration and so on, but GETrack is optimized for capturing tracks, storing them on your smartphone, and then exporting it to a variety of formats and sending them to your laptop. Perfect. You can get a <a href="http://www.handango.com/PlatformProductDetail.jsp?siteId=1&productId=188408">trial download that logs 50 waypoints from Handango</a>, and you can also buy it for about $14 from there.</p>

<p>So, after downloading and installing GETrack and making it sure it could communicate with the TomTom, I grabbed my camera and went for a walk. The TomTom receiver just has a single button and a flashing green light, and it slipped easily into the pocket of my shorts, after which I ignored it. I found myself spending more time fiddling with the software, trying to make sure it was working, figuring out how often I should log (I set it to 10 seconds, but even that might be overkill while walking), and of course watching to make sure I didn't go over 50 waypoints. All while trying to remember to take some pictures that I could geotag later :P</p>

<p>Once I got things settled I put the E61 in my other pocket and just walked. I ended up with three tracks, each maxed out at 50 waypoints for the trial version of GETrack. Once back at home, I sent the tracks in GPX format (you can choose from several formats, including KML for direct display on Google Maps), and then used <a href="http://oregonstate.edu/~earlyj/gpsphotolinker/>GPS Photo Linker</a> to load in the tracks, and then loaded in the photos I took. This would be the exact same step to import tracks from a simple GPS logger, the tricky part being that unlike Bluetooth, the interfaces aren't standardized, so you need to find the software to get the tracks off.</p>

<p>Finally, here is my <a href="http://www.flickr.com/map/?&user_id=35034346160@N01&fLat=49.264073&fLon=-123.140601&zl=2&min_taken_date=2007-8-15%2000:00:00&max_taken_date=2007-08-16%2000:00:00">GPS adventure walk on my Flickr map</a>. For starters, I should have perhaps taken more photos. Secondly, I messed up the time codes on my first batch. In essence, the time codes are the most important thing. The best way to make sure you're getting it right is to take a picture close to the beginning of your logging, and another one right at the end. Then, look at the time offsets in GPS Photo Linker and adjust the timezone offset until the GPX track timestamps match up with your first / last photos. This doesn't have to be exact, but it should be close.</p>

<p>I manually fiddled with the last batch, matching up track waypoints with photos, and got great results. A good example is <a href="http://www.flickr.com/map/?&user_id=35034346160@N01&fLat=49.264055&fLon=-123.140602&zl=1&min_taken_date=2007-8-15%2000:00:00&max_taken_date=2007-08-16%2000:00:00&map_type=hyb">this shot of Death By Chocolate</a>, where the hybrid map mode let's you see that the distinct roof matches the photo I took.</p>

<p>All in all a pretty good experience, but having to research, install, and then get the software working, plus the potential for difficulties in getting the Bluetooth receiver talking to your logging device (most Series 60 phones should work with GETalk) confirms for me that I just want a GPS logger :P</p>

<p>The nice thing for photowalks and other group events, is that only one person needs to be carrying a logger. Sharing the tracks afterwards will allow anyone to easily geotag their photos.</p>

<p>Lastly, <a href="http://www.gpsvisualizer.com/">GPS Visualizer</a> and <a href="http://www.everytrail.com">Everytrail</a> are two sites I've found where you can upload GPX tracks directly and see them on a map. I'm sure there are others. Whew. That was a complicated tech exercise for such a short adventure :P</p>
