---
layout: post
title: 'More Flickr export & photo experiments'
categories:
  - How To
tags:
  - Flickr
  - Cloudflare
  - IPFS
  - photos
  - "Web 2.5"
  - Web3
  - barcamp
  - Roland Tanglao
comments: true
excerpt: "Experimenting with various services for dealing with my Flickr export backup and moving photos around, resulting in documenting a grab bag of cloud services, protocols, articles and other research."
---

My last post was about [dealing with my Flickr photo exports and experimenting with them in Jekyll](/flickr-exports-jekyll/). Now that I've got the zip files all backed up in Google Drive, I started looking at getting them all in one spot. Ideally, this would happen without having to download, unzip, and then move again somewhere else.

As well, I currently auto-upload photos from my phone to Dropbox, and then as Dropbox fills up (I don't have a paid account), I archive them elsewhere -- in my Google Drive account (paid for, runs my personal email, holds my main working GDoc files) or OneDrive (paid, the "family" account, includes 1TB of storage, my "long term" archive / backup).

Right now, this is mainly a purely archive function. I'm not organizing the photos. They're not available online anywhere unless I put them on my blog here or [wiki](https://wiki.bmann.ca).

On to the snippets of research!

---

## Storing (and serving) photos from Amazon S3

I realized that 20GB of photos -- that is, at full resolution -- today would only cost about 50 cents per month (2.5 cents per GB). That's perfectly reasonable to effectively pay forever. And way cheaper than the ~$10 per month of Dropbox or comparable paid plans.

I already have ```images.bmann.ca``` that I've used on and off, and I [wrote about how to archive photos from iOS to S3](/archiving-photos-ios-amazon-s3) previously.

This means using the centralized Amazon S3 service as long term storage. As I move to IPFS, the files still need to be "stored" somewhere.

Using S3 with my own domain name, I get "regular" web URLs that I control. Importing the photos to IPFS will give each file a permanent content address -- essentially a "native" Web3 address to reach them at. And, I can move where the files are stored, like storing them on a home server, or even on my phone.

## Zapier for Dropbox to Amazon S3

A Zapier Premium account [supports Amazon S3](https://zapier.com/apps/amazon-s3). Unfortunately, they don't currently support the Canada Central zone, so this doesn't actually work at the moment.

I was testing automating my Dropbox auto-uploads to my own S3 account. This is definitely a good option, and probably better than the apps I researched before.

## MultCloud Cloud Drive Syncing

The next thing I found was [MultCloud](https:://multcloud.com). It lets you connect multiple different cloud services.

!['Multcloud Services'](/images/multicloud_screenshot.png)

I was pleasantly surprised that it actually supports Flickr directly! So, although I have all my Flickr exports backed up, it may actually be easier to move them from Flickr to S3 using Multcloud.

The free accounts limit the speed of transfers, doesn't allowing for scheduled transfers, and only supports two kinds of sync -- One Way and Two Way.

It also has an option to delete files from source once they are transferred. So, this is a pretty perfect solution for archiving photos from iOS. I can enable Camera Uploads in Dropbox on mobile, and then periodically use Multcloud to copy them to my S3 account. Other than having to manually trigger the sync, the 50GB of transfer per month of the free account would be more than enough.

Advanced sync modes include:
* Mirror -- target directory has files deleted to keep it the same as the source
* Move -- source files deleted after target transfer
* Cumulative - target directory files are not deleted even if deleted from source
* Update -- target files are deleted, and then everything from source is transferred
* Incremental Backup -- a new subdirectory is created on the target for each source transfer of added / modified files
* Full Backup -- a new subdirectory on the target where the current state of source is synced to on transfer

I don't know enough about the company behind MultCloud to give advice on trusting them long term. You are giving a lot of access to your accounts, that potentially hold a lot of sensitive information. I'm going to use it to shuffle around some files and then disconnect my account authorization.

## RClone

[Rclone](https://rclone.org/) is open source software that calls itself "rsync for cloud storage". It's a command line tool to do various file and directory transfers. I haven't investigated it further, but would use this long term rather than a service like MultCloud.

## MultCloud Flickr to S3 Test

I synced an Album from Flickr to S3 as a test. What better one to use than some history from the beginning of Web2. Here's my original Flickr album for [Barcamp and Mesh in Toronto](https://www.flickr.com/photos/boris/albums/72057594138250222).

The files are now all on my, like this photo of [Roland](https://rolandtanglao.com) at Liberty Cafe ([Flickr original here](https://www.flickr.com/photos/boris/146293250/in/album-72057594138250222/)):

![Roland at Liberty Cafe](https://images.bmann.ca/flickr/Barcamp%20and%20Mesh%20in%20Toronto/Roland%20at%20Liberty%20Cafe.jpg)

The photos are relatively terrible in quality because they were taken with a Nokia 6630 cameraphone. I guess I have to still blame bad composition on me!

Since the metadata export from Flickr is one JSON file per photo -- and in this MultCloud transfer mode I only have the title of the file, not its unique Flickr ID -- there isn't much I can do with this.

## WeServ Image Cache & Resize

I found [weserv](https://images.weserv.nl/) previously, a service that enables on-the-fly image caching and resizing.

Since my ```images.bmann.ca``` S3 bucket didn't have S3 enabled, I was getting mixed content errors on older content in my Netlify builds.

I temporarily went through and just changed to the image source to be served up through weserv:

```html
<img src="http://images.weserv.nl/?url=images.bmann.ca/dropshare/illustrator-bizcards-front.jpg" class="full" />
```

Another third party in the loop isn't great long term, which is why I'm fixing this with Cloudflare.

However, this solves another problem I had identified previously. Over the last 20 years, the digital photos in my archive have gotten bigger and bigger, and embedding the originals in a web page isn't feasible. So, generating thumbnails with weserv

I wonder if there is something photo-specific in IPFS that could link or associate generated thumbnails with an original. I think thumbnail generation is somewhat non-deterministic, meaning unique hashes, meaning different content addresses depending on how the thumbnail was generated.

The [weserv code is open source and available on Github](https://github.com/weserv/images), so you can run your own instance if you need this capability. The team is from [a small Dutch town called Sneek](https://en.wikipedia.org/wiki/Sneek) which I learned from the README on Github :)

## HTTPS for Amazon S3 Buckets with Cloudflare

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Enabling SSL on an Amazon S3 bucket is easier with Cloudflare than it is with Amazon's own tools. There is a ton of room for great tools on lower level systems.</p>&mdash; Boris Mann (@bmann) <a href="https://twitter.com/bmann/status/1081987317517021184">January 6, 2019</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Basic instructions are, transfer your DNS to [Cloudflare](https://cloudflare.com) and change your Crypto > SSL settings to "Flexible" -- and your S3 content should be delivered over HTTPS. You can also set a Page Rule to automatically forward HTTP to HTTPS, but I'm just going to use HTTPS for new content for now.

Here's a [blog post on full S3 bucket setup and Cloudflare](https://wsvincent.com/static-site-hosting-with-s3-and-cloudflare/) if you want to follow some steps.

## IPFS gateway with Cloudflare

I did a little bit of research previously, but other than running a whole cloud server, it's not currently easy to run your own IPFS gateway. Meaning, accessing files on IPFS through a regular web browser at your own domain.

But Cloudflare is [running an IPFS gateway](https://www.cloudflare.com/distributed-web-gateway/#connectingyourwebsite). They let you [connect your own domain with a CNAME](https://www.cloudflare.com/distributed-web-gateway/#connectingyourwebsite), which means you can upload / serve content using IPFS but still have it accessed using your own ```mystuff.example.com```.

A static site generator that is IPFS aware is something I'll be researching. It "works today" with relative URLs, but I think there's an opportunity for more here.

I label this kind of stuff as Web 2.5 -- using "regular" DNS, browsers, and standard web requests to access decentralized web content.