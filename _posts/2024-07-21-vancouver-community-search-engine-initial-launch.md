---
title: Vancouver Community Search Engine Initial Launch
date: 2024-07-21T12:50:57
categories:
  - Community Search Engine
tags:
  - Vancouver
  - DWebYVR
---
Thanks to [[Graham Fleming]], we've got an initial launch of a Vancouver Community Search Engine. Visit [search.dwebvancouver.org](https://search.dwebvancouver.org) to search local community people, organizations, events, communities.

It will return "internal" results first, that appear on the websites of the links that have been submitted. Toggle to outgoing links to see content that matches your search that local resources link to.

Right now, it's just a customized install of [[Lieu]] running things. Here's how it works:

* there is a website at [localhost.dwebvancouver.org](https://localhost.dwebvancouver.org) that is the webring or directory listing of the web pages that are the source for the crawled pages[^design]
* people can add their personal websites and other links by [making PRs to the index.html on Github](https://github.com/DWebYVR/localhost_vancouver_webring/tree/main/website)
* that page gets built and published to Github Pages whenever changes are made
* Graham got Lieu deployed on [[Railway]], which is what runs [the search page and queries](https://search.dwebvancouver.org)
* We still have some work to do to schedule re-indexing of links in the webring

You can try the search here by using this form. There are relatively few sources so far, and my site has the most content on it, so you're likely to find a page here for now.

<form method="GET" action="https://search.dwebvancouver.org">
	<p style="margin-bottom: 10px;"><input type="search" minlength="1" required="" name="q" placeholder="Your search query here" id="search" size="50"></p>
	<button type="submit" style="padding: 2px 10px">Search the Vancouver Community</button>
</form>

Design, indexing, the way search results are displayed and many other things can be improved, but we've got something to onboard people with for now.

[^design]: Yes, the design is bad / unreadable :) There's an [issue filed](https://github.com/DWebYVR/localhost_vancouver_webring/issues/3) if you'd like to get involved with some logo / brand and actual design of what a browseable directory of Vancouver resources should look like. Let me know!
## Search is broken

I've written a bit about what a [[Community Search Engine]] is and have been refining the idea, and need to test it with actual communities.

The basic premise is that the search experience for _users_ has been in decline for several years. Ever more SEO'd content and ads, less relevance and quality results for search users.

So you ask your friends for recommendations. And maybe you use social media for that. But social media is in precipitous decline, mostly happening on corporate owned platforms with opaque algorithms and more paid ads. 

So what if we started collecting resources from our friends and communities? From acquaintances to people from your communities of interest, you have some known factors of recommended by people.

## Add yourself and your Vancouver resources

The next step is to get people to add themselves, their Vancouver organizations and resources. You can do that by [adding your personal links to the index.html file](https://github.com/DWebYVR/localhost_vancouver_webring/tree/main/website).[^github]

[^github]: This is a fairly technical barrier today -- making a pull request in Github. [Here's an issue to make it available to less technical users](https://github.com/DWebYVR/localhost_vancouver_webring/issues/12).

Ideally, this will become a useful resource to search and browse, which is really about an intent: what should I use for accounting software in Canada? Can anyone recommend a lawyer? What home lab gear are you using?

My own site here is only tangentially about Vancouver -- I'm _in_ the regional community, but have pointers to resources everywhere. Of course, my [[FoodWiki]] has tons of Vancouver references that could be useful: I haven't added it as a link yet.

I'll leave discussions about browsing and serendipity for another time. There are some ideas of how to include social posts from Twitter, Mastodon, or ATProtocol, or subscribe to RSS feeds, in a way to surface "new" content over time, as well as evergreen search over resources.

Please add yourself, and let me know what you think about community search engines.