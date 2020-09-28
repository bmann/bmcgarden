---
layout: post
date: '2020-01-27T16:18:36.422Z'
title: 'Photo Backup for Geeks, iOS and S3 Revisited'
tags:
  - photos
  - ios
  - mobile
  - Fission
  - "Amazon S3"
  - Flickr
categories:
  - Blog
slug: photo-backup-for-geeks-ios-s3
---
I wrote a blog post back in 2017 about my [method of archiving iPhone photos to Amazon S3](https://blog.bmannconsulting.com/archiving-photos-ios-amazon-s3/). Today, I had someone ask me about what my current workflow is, since _The Archivist_ iOS app doesn’t work any more.

I use the Dropbox app to sync photos from my iPhone, and then periodically use [Multcloud](https://www.multcloud.com/) to copy the photos to my own Amazon S3 bucket. Multcloud is fine, but completely handing over your cloud login credentials to a service like this isn't great.

And then I don’t do anything with them, so they really are just backup at this point.

I'm calling this post "for Geeks", because most people will just use a paid iCloud, Google, or Dropbox account and be done with it.

Here are some further thoughts on photo sharing related items:

---

I [linked](https://blog.bmannconsulting.com/61957/) to [Ferdy Christant's The rise, fall and resurrection of Flickr](https://ferdychristant.com/the-rise-fall-and-resurrection-of-flickr-ca1850410ee1) which does a great job of defining some tiers of photo sharing:

* Tier 0, Personal local storage: _"source" material on your local computer or smartphone_

* Tier 1, Personal online storage: _"backup" storage, such as Dropbox or iCloud, not for sharing_

* Tier 2, Public online sharing: _this is the tier I'm interested in for self-hosting under my own domain name_

* Tier 3, Exposure and community: _amateur and professional sharing on a larger platform for distribution, from Instagram to Twitter and everything else in between_

* Tier 4, Portfolio: _for professional usage_

_Notes added by me_

It is overly focused on amateur-to-professional photographers, and I don't really agree with the conclusion about shuffling physical hard drives. Given the expense, time, manual nature, and general complexity, I believe that paid cloud backups -- or multiple clouds -- is going to be a better solution for anyone other than professional photographers.

---

My most prolific photos (that I actually share publicly) are probably still food and cooking pictures. Since I run [allthebest.recipes as a Discourse forum](https://allthebest.recipes), photo uploading from mobile works quite well.

---

I am in the midst of updating my blog with a Micropub endpoint that supports media uploads ([IndieKit](https://github.com/bmann/indiekit)), so I can easily upload photos for short blog posts. It supports multiple photos, I'll need to add some "gallery" styles so they display nicely.

---

Dropshare, mentioned in the original post, [supports S3](https://dropshare.zendesk.com/hc/en-us/articles/115003135729-How-to-set-up-Amazon-S3), but you can only upload one photo at a time, otherwise it will compress multiple files and upload a single Zip file. So not ideal for albums.

---

My company, [Fission](https://fission.codes), is going to be launching **Fission Drive**, which will provide end-to-end encrypted files and support for public web hosting and apps. I'm looking at support for Dropbox sync directly. People really liked my post on [exporting from Facebook to Fission](https://blog.fission.codes/exporting-your-facebook-photos-to-fission/) so that's another app to consider.
