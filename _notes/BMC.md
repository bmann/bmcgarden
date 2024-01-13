---
---
BMC is short for B. Mann Consulting aka this root domain and related subdomains that are my websites. It's also my short hand for things related to tinkering with this site.

Yes, I registered it in late 2000 and could have picked a way more interesting web address. I'll pick a better one next time.

## To Do

<style>
	li {
		list-style-type: none;
	}
	.task-list-item-checkbox {
		margin-right: 5px;
	}
</style>

- [x] Journal feed: Figure out how to make sure that full path image links are included
- [x] Update front page to have recent journal entries. 
- [x] Display “via” frontmatter [[via]]
- [x] Turn off linking out to notes
- [x] Tags? Something like “if tag same as Note, then link” or “on Note, list all pages with same tag”. Even with a “blank” [[Wiki]] page, you get all the notes tagged with wiki displaying. 
- [ ] Test run of re-importing LogSeq
- [ ] Make a [[Colophon]] feed by looking at Journal entries tagged with `colophon`
- [x] Add a style for `<li>` that have Obsidian `task-list-marker` class
- [x] Change date formatting for journal pages to include / highlight time posted rather than just day
- [ ] Reconsider slugs for journal. Maybe: `YYYY/MMDD/HHmm`.
- [ ] Main journal page will grow forever. Have to figure out daily or monthly pages. Pagination?
- [ ] Look at design from current <https://blog.bmannconsulting.com> for fancy dates 
- [x] Add blog posts to home page 
- [x] Reverse chron sort for journal pages? Or at least home page journal listing?
- [ ] Write code to loop through `aliases` and generate `_redirects` lines (this is a good idea!)

## Feed Affordances

Context for this should be “how is this useful to a Mastodon / Bluesky / etc reader?” - tags help in discovery, link to main article is most useful for reading, if there’s an image include it because it looks nice in the feed.

Or just trim with a link back to the original if you’re including fancy html, code, footnotes, whatever. 

So, operation custom feeds for cross posting is a go.

The [Micro blog formula](https://help.micro.blog/t/cross-posting-to-twitter-medium-mastodon-and-more/85) - first link only, put it at end of post, strip all other links - isn’t working for me. And Bluesky posting of links from custom feeds appears totally broken at the moment.

I want to not have to think about these things while writing. I want to dash off long posts or short posts, and the reader on the receiving networking should have a cohesive post. 

For those with “offsite” links — where I’m sharing an article or product or whatever, with some context and commentary — that link should be right there so readers can click through. 

Ideally the preview of THAT link also shows up nice. 

I’ll include a link back to the Journal post that will be as I have intended it, including edits and updates and any number of links. 

For Mastodon I have 500 characters to work with. So I can probably fit a few other links in there. 

For Bluesky, 300. At best room for one main link. 

If the link header is filled out, include it. 

If not, link back to the journal post. 

Always include the first image. 

If tags are filled out, include them at the end of the Mastodon post. 

I’ll make a feed for Mastodon and a feed for Bluesky with different character limits.

The journal feed will stay as it is — should work fine for feed readers already. 

Huh. If I keep using [[Micro.blog]] for crossposting, it means that each journal post will appear twice. Is it “fair” to just use it for crossposting? 

Ok, experiment with [[Fedica]] paid service. Could actually do that BEFORE making a custom feed, but I think the affordances are a good idea. 

- [ ] Journal feed: consider linking back to the actual journal entry. ~~Hmm, or maybe appending a hashtag like `BMCJournal` for context~~
- [ ] Journal feed: do tags-as-hashtags and append them
- [ ] Journal feed: do something special if link exists and append it

