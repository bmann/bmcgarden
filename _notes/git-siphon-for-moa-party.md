---
title: Git Siphon for Moa Party
date: 2021-02-13
tags:
    - Moa Party
    - feature
    - agora
---

This is a feature write up for [[Moa Party]].

My [[agora]] is stored in Git as a series of Markdown files, and I have some process for adding, editing, and publishing those notes. The [[Anagora]] server automatically ingests and publishes my agora directly from a Git interface.

A [[siphon]] is a way of ingesting content into an agora. By using git directly, anything that can post to git can be ingested.

Since Moa Party already supports Twitter and Mastodon cross posting, it is also a good candidate to add a git siphon to: posts made to Twitter or Mastodon, as well as being cross posted according to settings, can also be siphoned into the git repo that contains a person's agora notes.

## Connecting to a Git Repo

As a user, I go to moa.party and connect a git account. Gitlab / Github will be the two initial targets, since we have users who have their agoras on both.

The server then has credentials which allow to post on behalf of the user to a single repo.

## Posting to a Daily Log

Rather than posting tweets as notes, we want to add posts to a Daily Log. 

If no Daily Log exists for the current day, create it with correct name and front matter, and write the current post to the top of it.

If it does exist, append the current post to the bottom of the file.

* preference text field: path to daily logs folder, default `_posts/journal`
* preference text field: format of daily log files, default `[YYYY-MM-DD.md]`
* preference text field: front matter settings

Look at [[IndieKit]] for ideas on templates and how this is done. This can get moderately complicated.

Something like:
```html
<article name="TIMESTAMP">
<p>POST CONTENT GOES HERE<br />
<br />AND ANOTHER LINE<br />
<br />AND [[WIKILINKS]] GET LINKED<br />
</p>
<!-- Images at bottom -->
<img src="https://example.com" />
<!-- I have a better example of Twitter posting, we do want to include at least time, timezones are tricky -->
<cite>8:00PM<a href="https://twitter.com">#</a></cite>
</article>
```

The output is then a page with each post in chronological order for the day.

## Filtering Options

A siphon isn't really cross posting, so the filtering options are different. We'll need to think through these options and how they interact with the core cross-posting filter options.

* Toggle yes/no (radio button?): Send all posts to Git; if "no", show other checkboxes:
* Only post if [[wikilinks]] are included
* Only post if there is a link or image included
* Only post if global hashtag is included

Zero or more checkboxes can be checked, and each checked rule must be satisfied.

eg.

```
This is a sample [[Moa Party]] post that will end up in Git for my digital garden https://github.com/bmann/bmcgarden #moa
```

This post would get posted even if all the checkboxes were checked -- includes a wikilink, has a link, and uses the global hashtag