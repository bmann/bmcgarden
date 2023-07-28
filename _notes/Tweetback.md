---
---

tags:: #Eleventy, #[[Twitter/Archive]]
github:: https://github.com/tweetback/tweetback/

- Features
	- Each tweet has its own independent URL (with backwards/forwards threading!)
	- Uses [[Tweetback/Canonical]] to resolve other Twitter archives URLs (internal links stay in the archive and don’t link out to Twitter).
	- `t.co` links are bypassed and original hyperlinks URLs are used.
	- Links to users, tweets, non-truncated URLs.
	- Nicer link formatting for links-to-tweets: @username/:id.
	- Support some markdown: I sometimes use `backtick` markdown notation for code in my tweet text. This translates to `<code>` properly.
	- Analytics:
		- See your most popular tweets
		- Who you retweet the most
		- Who you reply to the most
		- Frequently used swear words
		- Top emoji
		- Top hashtags