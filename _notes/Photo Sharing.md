I recently [[2024-03-04_0743|shared that Ente is open sourcing their back end]] and lots of people are asking about what the options for (open) photo sharing. [[Ente]] is a hosted service, but their client software and now their backend software is open source, but it's not really designed for [[Self-hosting]].

I'm calling this photo sharing, but a lot of this ends up looking like sync or backup or related use cases.

For sharing, I'll define that as:
* subsets of photos that are publicly accessible and browseable on the web
* some sort of album / gallery grouping
* permissioned access to groupings
* being able to embed a photo directly on any web page[^photoembed]

[^photoembed]: I'm saying embed rather than e.g. a bare image link, because often those links will generate a lot of bandwidth if direct linked somewhere on the web. Embeds of some kind serve as a glue between wherever the photos are stored and just being able to view them on a web page.

I don't personally have a big need for privately accessible photos. At a small scale, I have this solved in a number of ways, including sending 6 photos over (insert messaging platform of choice). I haven't done a deep dive into what the programs below offer, e.g. shared private albums.

I do think that "many people contributing to a web-accessible, group photo album" is a very interesting use case. Anyone have pointers to options for that?

Here's a list of some of the photo sharing software I'm aware of, and/or use myself[^googlephotos]. I'm not directly recommending any of them, but am interested in those where it is possible to self host / the code is open source / I'm not trapped in a platform.

* [[Ente]] - paid, hosted cloud service and e2ee. Clients and server are all open source.
* [[Photo Prism]] - very full featured self-hosted solution, and also very resource intensive. Has face detection and map geolocation. Open source, but some advanced features require monthly subscription.
* [[Amazon Photos]] - after I exported all of my photos from [[Flickr]], I uploaded them all to Amazon Photos. Free with your Prime membership, but supports only 5GB of videos. You can choose to not sync videos in your camera roll.
* [[Immich]] - labeled as photo backup, this is a self-hosted solution that is installable on [[Cloudron]]
* [[iCloud Photos]] - I currently have a family plan and don't really think about photo storage / sync any more. They are all available on all my devices.

Personally, I'd like to get to [[Forever Photos with Content Addressing]].

[^googlephotos]: I'm not listing Google Photos. I experimented with it, but I don't trust anything like this to Google. And, I could never figure out how to link to ANYTHING in Google Photos in a way that I could actually USE the photos.