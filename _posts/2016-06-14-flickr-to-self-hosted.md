---
layout: post
title: "From Flickr to Self-hosted Photos"
date: '2016-06-14T12:34:34-07:00'
excerpt: "A response to Doc Searls on moving on from Flickr to think about self-hosting photos."
categories:
- Blog
tags:
- AWS
- Flickr
- photos
- Dropbox
comments: true
---
_This was originally posted to Medium, as a response to [Doc Searls' post 'Dear Adobe, Please buy Flickr'](https://medium.com/swlh/dear-adobe-please-buy-flickr-4f88dcd16ee0). I'm porting this post to my blog at the very end of 2018, just days before Flickr's acquirer makes changes to free accounts[^smugmug]. I'm in the midst of downloading my archive, and will actually need to deal with this in 2019. Of course, I'm thinking a lot more about web3 solutions and new protocols like IPFS, but there aren't easy answers._

Other than cost, why don’t you want to self-host your pictures Doc Searls?

I still haven’t done much about it, but I very much think my post-Flickr plan will be to self host.

The main problem _has_ been cost, for me.

## Cost of File Storage

I long ago made the calculation that Flickr was a better, more cost effective backup of my full resolution photos, than anything else.

Even at 0.10 per GB, 100GB is $10 per month.

## Cost of Hosting & Maintenance

From hosting a server to pretty much any time spent on maintenance, security updates, and so on, this is really the biggie. Do I have enough interest – or skills! – to confidently host & backup all of my digital photos?

Bandwidth costs could be big as well, especially if you don’t run anti-hot linking on your server.

## Loss of Social

Flickr hasn’t been a social site for me in a long time. I run Disqus (another third party…) across several sites and could see myself using it for photos as well. Or cross posting (some? all?) to Tumblr or Instagram or Twitter.

Part two of social is perhaps the simple Public/Friends/Family/Private permissions that Flickr has. I think for my photos, I’d end up going all public. Password-protected album sharing would be nice to have, but not critical.

## A Formula for Self Hosted Static Photos

I think I know pretty well the tool chain of services and features.

### Amazon S3

Static website hosting of all my photos with a public web facing interface on my own domain.

Web friendly thumbnails in various sizes. This saves on cost.

Interactive elements through JavaScript and third party services as desired / needed. Disqus for comments, Algolia for search, Mapbox for maps, etc.

### Amazon Glacier

Long term backup of original / full resolution images. Lowest cost.

Needed: Admin interface for selecting and requesting retrieval of batches of images.

### Dropbox

Photo syncing from your phone or desktop.

Nice to have: multiple people syncing to the same Dropbox folder.

### Photo Router

This is where some chunks of custom code come in.

Running a whole server of your own where you have to maintain the entire stack from operating system updates to web server defeats the purpose of making this simple, low cost, and low maintenance.

Some of this code could be running on Heroku, or even better, AWS Lambda functions fired as needed.

---

So, how this would work is as follows:

1. Take photos on your phone, or plug your camera into your computer. Dropbox automatically syncs all photos
1. Your Photo Router gets notified of new photos by the Dropbox API. It creates thumbnails and copies the originals to Amazon Glacier. Your photos are published to your static website.
1. You have an interface to work on albums, metadata, tags, privacy, etc. Technically this is managing your static website, so this might be done simply in Markdown / YAML (like Jekyll), or a separate Photo Editor chunk of code that helps manage your static website.

Of course, #3 is where all the complexity is. Can someone write code that does these things (not that hard) AND make it easy enough for web tinkerers to self-host on Heroku or AWS (this is the hard part)?

## Do I still care about photos?

I feel like I’ve written some variant of the above maybe half a dozen times.

I haven’t actively taken photos and edited and posted them for years. Part of that is the move to iPhone only pictures, but part of it feels like with the vast mass of photos, I care less about each individual one.

Regardless, at some point I figure I have enough of an obligation to keep my public photos online to do the Flickr export dance and host all my photos myself.

---

For the record, I think that Wikipedia or the Internet Archive would be much better homes than Adobe. Thinking about the Flickr Commons alone, never mind the people who set permissive licenses on their personal photos, we probably need to be thinking of these digital artifacts as legacies that should be part of a commons.

[^smugmug]: [SmugMug acquired Flickr in April 2018](https://blog.flickr.net/en/2018/04/20/together-smugmug-flickr/). [As of January 8th, 2019](https://blog.flickr.net/en/2018/12/17/important-service-updates-and-dates-to-remember/), free accounts are limited to 1,000 photos / videos. Then, as of February 4, 2019, any items over the 1,000 item limit will be deleted. Interestingly enough, since all of my photos are Creative Commons licensed, it seems they will stay up. Regardless -- it's time to move my photos from Flickr's domain to something that