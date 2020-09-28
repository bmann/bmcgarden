---
layout: post
title: "Best practices for tracking QR Codes"
description: "Cut out third parties and just use Google Analytics"
categories:
- How To
tags:
- Common Craft
- QR code
- Google Analytics
- Boxcar Marketing
- marketing
- analytics
---
My friends at [Common Craft](http://www.commoncraft.com) have a book called [The Art of Explanation](http://artofexplanation.com) coming out this fall, and it will include QR codes. In the book, there are multiple references to Common Craft videos, and Lee wanted to make it easy for people to go from reading a page in the book and then easily viewing the referenced video. These QR codes link to the explanation videos on their website. Since there is only one chance to get the codes right before they get printed, we talked about different ways to generate & track QR codes<sup>[1](#qrcode-explained)</sup>.

<!--more-->

## Short URLs and QR Codes

I've used a handful of link shortening and QR code generating services in the past, so we looked at which of them might be appropriate for generating codes and tracking. Link shortening services offer statistics on how many people have clicked on a link, which is a way to get tracking information even if you don't own the domain you are linking to (and thus don't have access to the analytics).

Many link shortening services also generate QR codes. Since the QR codes are generated based on the short URL, this also means that you can edit the link that the QR code points to after the fact. Useful if you have some QR codes in the wild in a permanent form (posters, t-shirts, books, etc.), but you want to link to different destination URLs over time.

There are two big downsides to using short URLs. One is relying on a third-party service, and the second is to add one more step between the QR code and the link you want people to actually end up on. If you are going to rely on a third party service, then you should at least use your own domain name. Then, even if the service goes down, you can run your own redirects, rather than risk having your QR codes break<sup>[2](#futureproof-urlshortener)</sup>.

Lastly, while not really a downside, you're not really tracking the the QR code, but rather the short link. This means if you use the link anywhere else publicly, you won't necessarily be able to tell the difference between someone clicking on the link vs. scanning the QR code.

Here are three link shortening / sharing services that also create QR codes from those links:

### bit.ly

While [bit.ly](http://bit.ly) has recently changed quite a bit, it is the original URL shortener that many people still use today. Using your own domain used to be a pro service, but is now free. You can go to the advanced tab of your bitly settings and [set your custom domain](https://bitly.com/a/custom_domain_settings).

Getting QR codes out of bitly is done by appending <code>.qrcode</code> to the end of any bitly URL. More details in the [bitly documentation](http://dev.bitly.com/qr_codes.html). Note: it looks like [you can't redirect your root domain](http://bitly.com/pro/help#root) unless you're using Bitly Enterprise<sup>[3](#bitly-enterprise)</sup>.

### Short Switch

[ShortSwitch](http://shortswitch.com) is a simple custom URL shortening service where the only option is to use your own domain. It starts at free for 1 user and 15 links per month, with the first paid plan being $4 / month for a single user account.

Each link you shorten also generates a QR code, and you can edit the URL the short link points to after the fact.

### awe.sm

While [awe.sm](http://awe.sm) does shorten links, it's design and strength is in social share tracking. It does [generate QR codes](http://blog.awe.sm/2011/08/26/create-qr-codes-with-awe-sm/), but these are done through the [Google Charts API](https://developers.google.com/chart/infographics/docs/qr_codes).

The basic account is $19 / month for a single user, and is definitely something you want to look at to get data on your social media conversion. Looking at it in more detail, it's not the right solution if you are looking for QR-code related tracking, although it can be used to do it.

## QR Code Tracking

The previous tools and the technique of creating short URLs with QR codes generated from those is more about tracking the links than tracking the QR codes. There are different ways to "track" the usage of QR codes directly.

### Esponce

[Esponce](http://esponce.com) was a tool that [Lee](http://leelefever.com) had found that is specifically designed to track various uses of QR codes. Under the covers, it actually does create it's own short links for tracking links, but Esponce also supports generating and tracking different kinds of content, such as contacts, phone numbers, geo locations, etc.

Looking closer, Esponce uses its own domain for the short links it creates. This means that you need to either trust that Esponce will be around for a while, or to pay for a white label solution at $600+ per year so you can use your own domain for link shortening.

Still, there are lots of interesting features in this platform, and the white label solution could be very interesting for agencies that want to offer these sorts of services in house.

### Tracking using Google Analytics

The solution we finally settled on was to track QR code usage by using Google Analytics. 

Using the [Google Analytics URL Builder](http://support.google.com/analytics/bin/answer.py?hl=en&answer=1033867), you can build. For Lee & Common Craft, the QR codes are going to be in a [printed book](http://artofexplanation.com), so we fill the builder out as follows:

* Campaign Source: <code>book</code>
* Campaign Medium: <code>qrcode</code>
* Campaign Name: <code>NameOfVideoBeingLinked</code>

The generated URL will then look something like this:

<code style="padding: 5px;">http://www.commoncraft.com/video/wikis?utm_source=book&utm_medium=qrcode&utm_campaign=wiki</code>

Once you've built your URL, you can use any QR code generator to create your QR code. Be careful __not__ to use one that generates the code based on a short link, since the whole point is to remove that step completely. I recommend the [ZXing generator](http://zxing.appspot.com/generator/), which is also great for things other than URLs<sup>[4](#zxing)</sup>.

Now, when you use these QR codes out in the field, you know that people visiting your website using that URL are definitely coming from a scan of that QR code. If you continue to follow this pattern for all of your QR codes, you can run different campaigns and then build reports in Google Analytics to slice and dice in different ways.

The advantage of this approach is that you are not relying on a third party service of any kind. You need to generate QR codes once (which are always the same for the same URL) and they will work forever. As well, since you're likely using Google Analytics to do reporting on your website traffic in any case, you can do all of your reporting including QR tracking in one place.

## Why use QR codes?

I'm going to skip the long discussion of why-or-why-not to use QR codes. I think they have their place, and if you do use them, you should have tracking in place. I think the same goes for social media, and link shorteners and some of the tools I've mentioned above can help you figure out which of your channels are working for you.

Many people have suggested that educating people about QR codes is a waste, and that we should rather focus on just displaying web addresses directly. I'm personally fascinated by QR codes because they are one of the few tools that are available to us to link the "real world" with online. They work today, and let us experiment while Google Goggles, NFC, and other more elegant solutions become widely adopted by the mass market.

Hat tip to [Monique at Boxcar Marketing](http://boxcarmarketing.com) who put us on the right track, and in general is a Google Analytics Jedi Master.

---------

## Footnotes

<sup><a name="qrcode-explained">1</sup>QR Codes Explained:</a>&nbsp;If you want an easy way to explain QR codes, check out [Common Craft's video explanation](http://www.commoncraft.com/video/qr-codes).

<sup><a name="futureproof-urlshortener">2</sup>Future Proof URL Shortener:</a>&nbsp;Dave Winer wrote about using meta-refresh to [run your own future proof "static" URL shortener](http://scripting.com/stories/2009/04/27/adjixHasABreakthroughIdeaI.html). Phil Windley has a more [detailed write up using a Perl script and the correct Apache settings](http://www.windley.com/archives/2012/07/my_own_url_shortener.shtml).

<sup><a name="bitly-enterprise">3</sup>Bitly Enterprise:</a>&nbsp;[Bitly Enterprise](http://www.bitlyenterprise.com/) is a completely different level of tool, with pricing starting at $995 / month.

<sup><a name="zxing">4</sup>ZXing:</a>&nbsp;The [ZXing project](http://code.google.com/p/zxing/) (pronounced "Zebra crossing") is an open source project for encoding and decoding barcode images of all kinds. You can [use the generator online](http://zxing.appspot.com/generator/) to create QR codes that support all kinds of content, including "just" URLs. There is also code available for you to use in any custom application where you need to generate or decode barcodes.
