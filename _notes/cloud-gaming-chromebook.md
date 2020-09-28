---
title: "Cloud Gaming on Chromebooks"
---

# Background

Right now, a number of the cloud streaming services have Android apps, which will run on Chromebooks. TLDR; [Parsec](#parsec) is currently the best option.

## Game Controllers
I have a [Logitech F710](https://www.logitechg.com/en-ca/product/f710-wireless-gamepad), which is a 2.4Ghz wireless gamepad with USB dongle.

My ASUS only has USB-C, so I have a USB + HDMI dongle, and it worked out of the box with Steam Big Picture.

### Logitech F710 Wireless Gamepad, ASUS Flip C302CA, No Man's Sky streaming via Parsec

![Logitech F710, ASUS Flip C302CA, and Parsec streaming No Man's Sky](/uploads/c-3-e-8894-d-15-ac-4-bb-1-8-ff-8-7445284-eb-639.jpeg "Logitech F710, ASUS Flip C302CA, and Parsec streaming No Man's Sky"){.align-center}

## Linux

When Linux apps are supported, I'll report more. It will likely be easier to just use the Android apps for Cloud Gaming, and direct install various games in Linux either natively or through Steam. [GalliumOS](/chromebook/galliumos) supports [Steam as Additional Software](https://wiki.galliumos.org/Additional_Software). There is the fact that Linux apps are optimized for Intel processors, and Android apps are optimized for non-Intel, which will matter depending on what type of Chromebook you have.

# Cloud Gaming Services
For most cloud gaming providers, they probably envision either an Android TV device or Android tablet. But with Chromebooks being able to run Android apps, this means cloud gaming is definitely an option.

## Liquid Sky
* https://gaming.liquidsky.com
* Platforms: Windows, Android ([apk direct download](https://cdn.liquidsky.com/assets/liquidsky.apk)), Mac "coming soon"
* Pricing: one time $14.99 - 25 hours & 200GB / or monthly $29.99 - 100 hours & 500GB; annual $299 - 120 hours & 750GB

I used this on my Mac way back in December 2016 when they had SkyCredits that you could buy and use.

It worked well, but then they stopped supporting the Mac or had Mac problems and in general seemed to revamp the whole system. They are now a subscription service -- sort of.

With $14.99, you buy 3000 SkyCredits. For a Standard PC, you pay 2 credits per minute, and for a Pro PC you pay 4 credits per minute. That works out to 25 and 12.5 hours.

There are a huge number of different ways to pay (including bitcoin!), I think because they use [Xsolla](https://xsolla.com/).

I signed back up to give it a try. The Android app is full featured and much less flaky than Parsec. But, specifically with _No Man's Sky_, which is what I wanted to be playing, there was some bug with the way they stream keyboard + mouse and/or gamepad input that your mining laser would fire continuously and mouse sensitivity was screwy.

After using it again for a while, the one time $14.99 is really the best deal.

## Parsec
* https://parsecgaming.com/
* Platforms: Windows, Mac, Android (beta), Linux, Raspberry Pi
* Pricing: bring your own PC or cloud gaming using Amazon or Paperspace; credit system

Parsec was originally designed to stream from computers you already own. They added cloud gaming with machines from Amazon or Paperspace. You put money on account with Parsec, and then they pay Amazon or Paperspace on your behalf.

The Android app is in beta[^parsecapk]. I've used it for a ton of hours, but it can be flaky - you can't switch out of the app, or resize it, or really do anything, otherwise it will close the streaming session and you'll need to reconnect. Most of the time this just reconnects and you're back to where you were in the PC or game.
Here's their [FAQ on charges for cloud PCs](https://support.parsecgaming.com/hc/en-us/articles/115003113431-How-Does-Parsec-Calculate-The-Price-And-Charges-On-My-Cloud-PC-)

Paperspace will charge you $5 per month for storage and $0.40 an hour for their machines. However, I found their systems flaky lately, and ultimately deleted my Paperspace and switched to Amazon.

On Amazon, storage will be $10 per month. You can pick between a lower end machine at $0.72 - $0.88 per hour or a high end machine at $1.88 per hour.
[^parsecapk]: For various reasons (my Google for Business account), my Chromebook won't install this directly, so I need to [download the APK and install it manually](https://apk-dl.com/parsec/tv.parsec.client).

Amazon has been working very well for me -- but it seems super expensive!

## Vortex
* https://vortex.gg/
* Platforms: Windows, Mac, Android, Chrome, XBox One
* Pricing: $9.99 per month

Only supports selected games. Of their game library, some of them you have to own it in your own Steam library to be able to play it.

_Haven't tried this_

## Shadow
* https://shadow.tech/
* Platforms: Windows, Mac, Android, Linux, iOS (private beta)
* Pricing: $34.95 per month

Other than maybe for premium iOS users, this price point just seems way too expensive?

_Haven't tried this_

## NVIDIA GeForce NOW
* https://www.nvidia.com/en-gb/shield/games/geforce-now/
* Platforms: Windows, Mac, Shield TV
* Pricing: in beta, free with Shield TV

I recently installed this on a Mac and it works great.

I've been using it extensively on Shield TV with my Steam library and it's pretty great.