---
layout: post
title: 'Flickr Exports in Jekyll'
categories:
  - Web3
tags:
  - Flickr
  - Jekyll
  - Textile
  - IPFS
  - Web3
comments: true
excerpt: "I'm exporting my photos off of Flickr ahead of their limits for free accounts. This is an initial experiment of the export files, and how to display them in Jekyll."
---

The deadline for deletions of photos from free Flickr accounts is early February[^flickrdates], so I've requested the backup of my account[^flickrrequiem].

The two "Account Data" files are 13MB and 5MB each, and are filled with ```photo_#########.json``` files -- one for each photo.

![](/images/flickr_account_export.png)

The photo and video zip files vary in size from ~300MB to ~1GB. I figure that's about ~23GB of photos, total.

My intent is to self-host these photos. Ideally the photos themselves will be have "permanent" addresses on IPFS -- but I'll still want to display them, and ideally with the original Flickr metadata. This will involve an IPFS to web gateway so I can just include the images directly. The folks from [Textile](https://www.textile.photos/) already have a bunch of IPFS tools specifically for photos that I'll be looking into[^textile]. Plus [Cloudflare is running an IPFS gateway](https://blog.cloudflare.com/distributed-web-gateway/) that may come in useful.

Seeing as the metadata has individual JSON files, I figured I'd take advantage of the Jekyll ```_data``` folder feature: any JSON files placed in that special folder are transformed into a special ```site.data.path.to.file``` variable.

I made a folder ```_data/flickr``` and can put the photo JSON files in there, and then loop through ```site.data.flickr``` to access them all.

For now, I'm just going to experiment with dropping a couple of JSON files in there, and manually uploading the related original photos to the Jekyll site as well. From my old Nokia N80 (and Shozu[^shozu]!) the files are ~1.6MB, and from my Canon S5, ~5MB.

[^shozu]: Shozu was an auto photo uploader for early smartphones that [Roland](http://rolandtanglao.com/) and I and many other Nokia phone geeks used.

You can view the [Flickr page](/flickr/) to see the output. Not very exciting, but I'll pull some more photos, perhaps some with lots of comments, and see where I get to.

Among many other issues around dealing with ~14 years of photos, Jekyll doesn't (natively) support paginating data files. This obviously isn't a final solution in any way.

For now, I'm backing up the Flickr zip archives in my Google Drive account, and will be writing more about what I see as an ideal path to getting these photos permanently into Web3, plus a Web2 front end.

Get in touch if you're interested in this as well!

---

Here's the very simple code for [my Flickr page](/flickr/):

```liquid
{% raw %}
{% for photo_hash in site.data.flickr %}
{% comment %}
<!--
* Loops through all the photos_nnnnnn.json files in the _data/flickr folder
* Each is turned into an object "photo"
* The image original is hardcoded to be in the images/flickr folder
* BUG: Geo seems to be very off?
* BUG: license is "null" -- but on Flickr it's clearly CC
* TO DO:
  ** Tags
  ** Comments
  ** Groups
  ** Albums
-->
{% endcomment %}
{% assign photo = photo_hash[1] %}

  {% if photo.privacy == "public" %}
    <div class="{{ include.type | default: "list" }}__item">
      <article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
        <h2>{{ photo.name }}</h2>
        <img src="/images/flickr/{{ photo.original | split: '/' | last }}" style="padding-top: 20px" />
        <p class="archive__item-title" itemprop="description">
        {{ photo.description | remove: "<p>" | remove: "</p>" }}{% if photo.geo %} @&nbsp;<span class="place"><a href="https://www.openstreetmap.org/search?query=#map=14/{{ photo.geo.latitude | divided_by: 1000000.00 }}/{{ photo.geo.longitude | divided_by: 1000000.00 }}">OpenStreetMap</a></span>{% endif %}
        </p>
        <p class="page__date"><strong><i class="fas fa-fw fa-calendar-alt" aria-hidden="true"></i>Photo Taken: </strong> <time datetime="{{ photo.date_taken | date_to_xmlschema }}">{{ photo.date_taken | date: "%B %d, %Y" }}</time></p>
      </article>
    </div>
  {% endif %}
{% endfor %}
{% endraw %}
```

And here's an example photo JSON file. The [original photo page this metadata is related to is still on Flickr here](https://www.flickr.com/photos/boris/2634391576/). Yes, that is a ton of EXIF data!

```json
{
	"id": "2634391576",
	"name": "Killarney Lake",
	"description": "\n - Camera phone upload powered by <a href=\"http://www.shozu.com/?utm_source=upload&amp;utm_medium=graphic&amp;utm_campaign=upload_graphic/\" target=\"_newwindow\">ShoZu</a>",
	"count_views": "53",
	"count_faves": "0",
	"count_comments": "0",
	"date_taken": "2008-07-01 13:04:18",
	"count_tags": "1",
	"count_notes": "0",
	"date_imported": "2008-07-03 09:48:30",
	"photopage": "https://www.flickr.com/photos/boris/2634391576/",
	"original": "http://farm4.staticflickr.com/3008/2634391576_6ab6f1017f_o.jpg",
	"license": null,
	"geo": {
		"latitude": "49696401",
		"longitude": "-123159753",
		"accuracy": "15"
	},
	"exif": {
		"IFD0:Orientation": {
			"full": "IFD0:Orientation",
			"label": "Orientation",
			"value": "Horizontal (normal)",
			"raw_value": "Horizontal (normal)"
		},
		"IFD0:XResolution": {
			"full": "IFD0:XResolution",
			"label": "X-Resolution",
			"value": "300 dpi",
			"raw_value": "300"
		},
		"IFD0:YResolution": {
			"full": "IFD0:YResolution",
			"label": "Y-Resolution",
			"value": "300 dpi",
			"raw_value": "300"
		},
		"IFD0:YCbCrPositioning": {
			"full": "IFD0:YCbCrPositioning",
			"label": "YCbCr Positioning",
			"value": "Centered",
			"raw_value": "Centered"
		},
		"ExifIFD:ExposureTime": {
			"full": "ExifIFD:ExposureTime",
			"label": "Exposure",
			"value": "0.005 sec (1/200)",
			"raw_value": "1/200"
		},
		"ExifIFD:FNumber": {
			"full": "ExifIFD:FNumber",
			"label": "Aperture",
			"value": "f/3.5",
			"raw_value": "3.5"
		},
		"ExifIFD:ISO": {
			"full": "ExifIFD:ISO",
			"label": "ISO Speed",
			"value": "20",
			"raw_value": "20"
		},
		"ExifIFD:DateTimeOriginal": {
			"full": "ExifIFD:DateTimeOriginal",
			"label": "Date and Time (Original)",
			"value": "2008:07:01 13:04:18",
			"raw_value": "2008:07:01 13:04:18"
		},
		"ExifIFD:CreateDate": {
			"full": "ExifIFD:CreateDate",
			"label": "Date and Time (Digitized)",
			"value": "2008:07:01 13:04:18",
			"raw_value": "2008:07:01 13:04:18"
		},
		"ExifIFD:LightSource": {
			"full": "ExifIFD:LightSource",
			"label": "Light Source",
			"value": "Unknown",
			"raw_value": "Unknown"
		},
		"ExifIFD:Flash": {
			"full": "ExifIFD:Flash",
			"label": "Flash",
			"value": "No Flash",
			"raw_value": "No Flash"
		},
		"ExifIFD:FocalLength": {
			"full": "ExifIFD:FocalLength",
			"label": "Focal Length",
			"value": "4.7 mm",
			"raw_value": "4.7 mm"
		},
		"ExifIFD:ColorSpace": {
			"full": "ExifIFD:ColorSpace",
			"label": "Color Space",
			"value": "sRGB",
			"raw_value": "sRGB"
		},
		"ExifIFD:CustomRendered": {
			"full": "ExifIFD:CustomRendered",
			"label": "Custom Rendered",
			"value": "Normal",
			"raw_value": "Normal"
		},
		"ExifIFD:ExposureMode": {
			"full": "ExifIFD:ExposureMode",
			"label": "Exposure Mode",
			"value": "Auto",
			"raw_value": "Auto"
		},
		"ExifIFD:WhiteBalance": {
			"full": "ExifIFD:WhiteBalance",
			"label": "White Balance",
			"value": "Auto",
			"raw_value": "Auto"
		},
		"ExifIFD:DigitalZoomRatio": {
			"full": "ExifIFD:DigitalZoomRatio",
			"label": "Digital Zoom Ratio",
			"value": "1",
			"raw_value": "1"
		},
		"ExifIFD:SceneCaptureType": {
			"full": "ExifIFD:SceneCaptureType",
			"label": "Scene Capture Type",
			"value": "Standard",
			"raw_value": "Standard"
		},
		"ExifIFD:GainControl": {
			"full": "ExifIFD:GainControl",
			"label": "Gain Control",
			"value": "None",
			"raw_value": "None"
		},
		"IFD1:Compression": {
			"full": "IFD1:Compression",
			"label": "Compression",
			"value": "JPEG (old-style)",
			"raw_value": "JPEG (old-style)"
		}
	},
	"groups": [

	],
	"albums": [

	],
	"tags": [
		{
			"tag": "ShoZu",
			"user": "https://www.flickr.com/photos/boris/",
			"date_create": "2008-07-03 09:48:30"
		}
	],
	"people": [

	],
	"notes": [

	],
	"privacy": "public",
	"comment_permissions": "any flickr member",
	"tagging_permissions": "people you follow",
	"safety": "safe",
	"comments": [

	]
}
```

[^flickrdates]: There are a number of [important Flickr dates](https://blog.flickr.net/en/2018/12/17/important-service-updates-and-dates-to-remember/). Theoretically, I will have all my photos over the 1,000 limit deleted. Except those that are CC-licensed, and since I've always licensed them all CC, maybe they will never be deleted? Early February is going to be an interesting ride!

[^textile]: I [tweeted at](https://twitter.com/bmann/status/1079813719729659907) the folks from Textile, who pointed me at their [custom metadata](https://medium.com/textileio/quick-look-textile-files-and-schemas-36e9d131f229). I'll be dropping into their [Slack](https://slack.textile.io) to talk more about this.

[^flickrrequiem]: I'm not mad or upset at SmugMug, the new owners of Flickr. My last uploads to Flickr were from 2 years ago, and I've been experimenting with other solutions since 2012, as evidenced by my write up of <a href="/flickr-question/">The Flickr Question</a>.