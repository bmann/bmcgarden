---
layout: post
title: 'Archiving photos from iOS to Amazon S3'
categories:
  - How To
tags:
  - Amazon S3
  - photos
  - iOS
  - mobile
  - IPFS
  - Flickr
  - AKASHA
  - Web3
comments: true
excerpt: "How To setup an Amazon S3 account and use it to backup photos from your iPhone iOS device directly, all hosted on your own domain."
---

I’ve wanted to have photos that I take – which at this point are all from my iPhone – uploaded to some place under my control. I also want to be able to share them on the web, including embedding them in blog posts.

I also need to export my 13 years of photos on Flickr (I previously [wrote a response to Doc Searls about Flickr & photo management](/flickr-to-self-hosted/)). My long term goal is still to get all of these photos onto a blockchain[^web3].

[^web3]: OK, not photos _on_ the blockchain. Editing this in January 2019, I'll say the goal is to get the photos onto the decentralized web, aka Web3.

I used the [Mediachain deployment page](http://deploy.mediachain.io/) to get my own server up on Digital Ocean. But I’m stuck at the “how do I get files added”. Plus I’m stuck running my own server, and potentially backing it up separately.

With [AKASHA](http://akasha.world/), I have an [IPFS](http://ipfs.io/) server running on my desktop at home. Images added to AKASHA posts get added to IPFS automatically. The AKASHA blockchain is currently a test net, and it doesn’t help get photos from my phone uploaded.

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Screenshot of IPFS peers serving up the pics from my AKASHA post. @valanchee no pins in Africa, I expect you to be first! <a href="https://pbs.twimg.com/media/C4uYk-OUoAAxfrq.jpg:largen">pbs.twimg.com/media/C4uYk-OUoAAxfrq.jpg:large</a></p>&mdash; Boris Mann (@bmann) <a href="https://twitter.com/bmann/status/831926321081044992">February 15, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

So in the meantime, what’s an easy way to upload / archive photos from your iPhone to a domain you control?

The short answer is get an Amazon S3 account, and then use The Archivist and/or Dropshare apps.

The longer instructions are below.

Seeing as the question “how do I make room on my iPhone / backup photos on iCloud” was the first tech question asked me in Uganda, I think a mobile blockchain / IPFS client is something I will continue to explore.

---

This assumes you have an AWS account and that you have your own domain name. I recommend [Namecheap](https://namecheap.com) or [Hover](https://www.hover.com/) for registering domains and hosting DNS.

You’ll also need to create a new IAM user that has full control of S3, and note down the access and secret keys. If you don’t copy the secret key, you can just add a new credential for the user, which will give you a new key and secret.

You can do all of these things through the AWS console.

## Setup a new S3 bucket with the name of the domain you will point at it.

Something like images.example.com.

You can choose a region, and I ended up picking the new Canada / Montreal region.

Lots of S3 apps haven’t been updated to support new regions yet, so this may cause issues for you.

Specifically, Dropshare is supposed to get an update a week or so from when I’m posting this, according to the reply I got from support.

## Setup static web hosting and add a policy

For the properties of the bucket you just created, click the enabled checkbox of the Static Web Hosting section.

You can put in _index.html_ and _error.html_ as the index and error pages. I haven’t done anything with these yet, but you can upload simple HTML pages and have them display whatever you like.

Next you’ll need a policy that allows anonymous users to view images. Under the Permissions section, you can add a policy that looks like [this gist](https://gist.github.com/bmann/fb47baf90dfc276844d1941f30d45711#file-s3-public-bucket-policy-json).

The one line that lists the name of your bucket (images.example.com) is what needs editing to include your value.

While you’re in here, you can see what the Amazon endpoint is, which is listed under the Static Website Hosting section of the properties.

## Map your own domain name

Create a CNAME that points your domain (_images.example.com_) to the Amazon endpoint (mine is ```images.bmann.ca.s3-website.ca-central-1.amazonaws.com```). You’ll need to go into the Advanced DNS management of your registrar to do this.

Now, uploaded images can be accessed through ```images.example.com/path/to/image```[^nohttps].

[^nohttps]: You can't access files over HTTPS with this initial setup, so if you're embedding your images somewhere that does use HTTPS, it will complain about mixed insecure content. It's a long series of steps to get Amazon setup with Cloudfront, so instead just use [Cloudflare](https://cloudflare.com) -- you'll need to use them as your DNS registrar.

## Install and configure apps

You’re basically done at this point as far as backend configuration. There are a variety of desktop tools (e.g. Cyberduck) that will let you browse, upload, and manage files in your S3 bucket. Anything you upload will be publicly available at your own images.example.com domain.

But I want to do this from my phone, and ideally I want it to be relatively automatic, much like Flickr, Google Photos, or Dropbox Camera Uploads.

### Archivist App
* [Facebook Page](https://www.facebook.com/archivist.ios/)
* [$2.79 on iTunes](https://itunes.apple.com/us/app/archivist/id1180291253)

This app was just released at the beginning of December 2016, and it’s pretty close to exactly what I want so I bought it immediately.

I do wish the Archivist would allow an option to configure web hosting and policy settings for you. Maybe another option for size of thumbnails.

You can choose which parts of your camera roll to auto archive. With the policy setup that I’ve recommended, all your photos are public. I have a tendency to take pictures of whiteboards, so you may not want to archive your entire camera roll.

I’m still experimenting since the app is really not designed to be public, but to be an archive. Shares and copies from within the app grab the image for using in other photo apps, not the S3 URL path. But absolutely recommended so far.

### Dropshare
* [getdropsha.re](https://getdropsha.re/)
* [freemium on iTunes](https://itunes.apple.com/ca/app/dropshare-powerful-file-sharing/id932316817?mt=8)

I used Dropshare in the past, and it was good, but you’re uploading one image at a time. It also has a Mac desktop app so you can do uploads from there.

It understands custom domains and can add the direct URL to your upload to your clipboard.

I purchased it previously, but you’ll need a one time $9.99 in app purchase to use S3. As mentioned above, I need to wait for Canada/Montreal region support to properly try it again[^dropshareca].

[^dropshareca]: Dropshare does support the Canada region now. This is a decent way to upload quick individual files, and I continue to use it.

### Owncloud
* [owncloud.org](https://owncloud.org/)
* [free on iTunes](https://itunes.apple.com/ca/app/owncloud/id543672169?mt=8)

Not relevant for what I’m trying to do, but the [Owncloud app seems to do auto photo uploads](https://github.com/owncloud/ios/issues/13). I really don’t like to have to run & maintain (and backup!) my own server, so S3's ability to map your own domain and have an API is a better fit.

---

I’m surprised that there aren’t more simple S3 apps on mobile, but this just underlines that most people don’t care about storing files under their own control. And of those that do, many would give me grief about using S3 rather than running my own server!

## Future directions

Storing the full size images from an iPhone 7 takes up a lot of room. Even at only 10¢ per GB per month, this can add up.

There are options under the Lifecycle properties section of S3 to automate moving items that haven’t been accessed to Glacier, Amazon’s long term archival system. It costs 1/10th of S3, and so is a good fit for backup of originals.

Feels like something the Archivist could add an interface for, but in the meantime I may be able to do this directly.

---

_How do you manage photos on your phone? Do you bother backing them up or storing them somewhere? Is sharing or embedding them on the web even a concern for you? I’d love to hear more about apps, techniques, and other pains and concerns you have about your photos._