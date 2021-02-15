---
title: WikiJS
git: https://github.com/Requarks/wiki
link: https://wiki.js.org/
date: 2020-09-28
modified: 2021-01-24
---

_[[Wiki]] software built on [[NodeJS]]. Has great [[Deploy To Heroku]] support_

* Home page https://wiki.js.org/
* OpenCollective Donations https://opencollective.com/wikijs
* Github https://github.com/Requarks/wiki
* Deploy via Heroku https://github.com/Requarks/wiki-heroku

An open source, modern and powerful wiki app built on Node.js, Git and Markdown. Can be maintained through a git repo (public or private, Github, Gitlab, etc) with standard git commits, as well as allowing edits through the front end, which writes back to the git repo.

Runs this site!

## Tips

### Keyboard Shortcuts

<kbd>CMD</kbd> + <kbd>S</kbd> on Mac (and iOS with external keyboard) will save the page you are working on.

### Footnotes

Uses [Markdown-It footnotes](https://github.com/markdown-it/markdown-it-footnote)

```
Here is a footnote reference,[^1] and another.[^longnote]

[^1]: Here is the footnote.

[^longnote]: Here's one with multiple blocks.

    Subsequent paragraphs are indented to show that they
belong to the previous footnote.
```

#### Inline Footnote

```
Here is an inline note.^[Inlines notes are easier to write, since
you don't have to pick an identifier and move down to type the
note.]
```

## Bugs

### Task list items break all other formatting

https://github.com/Requarks/wiki/issues/1908

```
- [ ] Task list [link](/path/to/page)
- [ ] Task next https://example.com
- [ ] Task the **third**
```

(I can't show this live because it screws up formatting for the whole rest of the page)

### Moving files in Git

https://github.com/Requarks/wiki/issues/1358

Still trying to confirm this as I mass edit my files locally in git. May be "fixed" if I know which cache button to purge.

---

## Wish List

### Wiki-linking of pages

Some way to indicate that a page doesn't exist yet, so that you can come back and create it. `[[Double Square Brackets]]` might get used, or really, just single `[square brackets]` which might be more native 

Also, a global list of linked-to-but-not-created pages. I don't know what the common term for this is.

### Tag-linking

#tips links to the [tips tag](/t/tips) automatically.

([Discourse](/software/discourse) does this for categories and tags)

### Global link count

Count and store all of the external links. Have a page that shows all of the external links, how many times they are linked from a page

### Backlinks

Show backlinks to pages that link to the current page

### OEmbed support

Rich embeds of links

### Check off "checkmark" lists without full page edit

You can make checkmark lists, but you have to go into full edit mode to "check them off". Either a separate permission, or just link it to page permission and allow checking them off through the front end.

Global view of all un-checked and checked checkmarks, filterable by tag.

### Allow for in-page view / edit of frontmatter

Currently, front matter is written back correctly to the git repo, but you need to use the UI to edit all of the options.

As an option, enable the ability to display the frontmatter inline.

For reference, the frontmatter includes:

```
---
title:
description:
published: true
date: 2020-05-20T04:02:00.507Z
tags: comma, separate, can use spaces, even
---
```

### Mobile Editing Interface

Probably not going to happen with the full app, but there **is** a GraphQL endpoint.

The project itself could ship with `/m/`, with a mobile optimized interface. Specifically for editing, adding notes, etc.

Syncing the entire git repo to your phone and searching / editing that "works", too :)

### RSS Feed

A feed of (public) updates

Bonus: per-tag feeds, per-"folder" feeds

### Auto-save mode

I have several pages that I keep open, and edit over time, especially my worklog pages. Default to an auto-save mode, which saves automatically (at the very least, locally to the DB).

