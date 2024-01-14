---
tags:
  - crossposting
  - microblogging
  - platform
---
Website: <https://micro.blog>

A blogging platform that supports [[Micropub]]. 

The core feature is hosting your blog there for $5/month. The $10/month plan adds podcast hosting, video hosting, bookmarks with archiving of bookmarked pages, and sending out posts by email.

It supports aggregating multiple different RSS or JSON Feeds and either importing them into your blog, or just merging them into your Micro.blog feed. 

## Crossposting

Feeds can be cross-posted to different networks, including:

* [[Mastodon]]
* [[Bluesky]]
* [[Medium]]
* [[LinkedIn]]
* [[Nostr]]
* [[Tumblr]]
* [[Flickr]]
* [[Pixelfed]]

The specification of [how cross-posting is configured](https://help.micro.blog/t/cross-posting-to-twitter-medium-mastodon-and-more/85):[^twitter]

> - Short posts without a title, and less than 280 characters, will be sent to Twitter unmodified.
> - Longer posts without a title, but longer than 280 characters, will be truncated with a link back to your microblog.
> - Posts with a title, regardless of length, will be sent to Twitter using the title and a link back to your microblog to read the full post.
> - Up to 4 photos embedded in a post are automatically downloaded and attached to your tweet. Photos should be larger than 200×200, to avoid accidentally cross-posting small buttons and tracking images that some blog systems include.
> - The first link in a post will be appended as a URL to the end of the tweet.

[^twitter]: This is the original write up for Twitter, which is no longer supported.

The newer write up of [how cross-posting works across networks](https://help.micro.blog/t/automatic-cross-posting-to-mastodon-and-other-services/860):

> Certain rules govern how your cross-posted content will appear. For example, on Mastodon:
>
> - Short posts without a title, and less than 500 characters, will be sent to Mastodon unmodified.
> - Longer posts without a title, but longer than 500 characters, will be truncated with a link back to your microblog.
> - Posts with a title, regardless of length, will be sent to Mastodon using the title and a link back to your microblog to read the full post.
> - Up to 4 photos embedded in a post are automatically downloaded and attached to your post. Photos should be larger than 200×200, to avoid accidentally cross-posting small buttons and tracking images that some blog systems include.
> - The first link in a post will be appended as a URL to the end of the tweet.
>
> Similar rules apply for the other services, but with different character length restrictions.

**Note:** It appears that only JSON Feed content works reliably. I have an [ongoing thread where Bluesky rich text isn't syndicating](https://help.micro.blog/t/feed-and-cross-posting-issues/2427), and apparently RSS vs JSON Feed appears to be the culprit.


## ActivityPub

Your Micro.blog account can also be activated as an [[ActivityPub]] account directly.