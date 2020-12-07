---
title: Colophon
---

Historically, a **Colophon** was "a statement at the end of a book, typically with a printer's emblem, giving information about its authorship and printing" (via Google Dictionary).

So, I keep notes on what software and other tools I use, in part as notes to myself.

My [[Blog Colophon]] documents software & changes all the way to 2001.

[[This site was last built: <strong>{{ site.time | date: '%B %e, %Y'}}</strong>::lmn]]
# Current

[[Simply Jekyll]] theme for Jekyll. If you want to run it yourself, I've got some public work around this with the [[Simply Jekyll Template]].

Using [[VSCode]] on my desktop to edit.

Hosting on [[Fission]]. [[Cloudflare]] is powering the DNS and [[Cloudflare IPFS Gateway]].

## To Do

* Look at side / margin notes and just use footnotes everywhere, possibly using [[BigfootJS]]
* Integrate [[Micro.blog]] [sidebar.js embed](https://help.micro.blog/2016/sidebar-js/) on the home page


# Archive

## bmannconsulting garden & gazebo (Sept 2020)

Well, WikiJS didn't last long. The public site is back to running [[Jekyll]], starting from the [[Digital Garden Jekyll Template]] and its custom [[Backlinks]] plugin. 

The public site is the "garden", which is in a `public` folder inside the "gazebo", where I can keep private notes. Stored in a private [[Github]] repo.

Since I have my DNS on [[Cloudflare]], ended up using the [[Cloudflare IPFS Gateway]] to link my site up to where it is hosted on the [[Fission]] platform. Which means the whole thing is on [[IPFS]]. You can [browse the archive 2020 folder](https://bmannconsulting.com/archive/2020/) to see the bare IPFS directories underneath.

I build the site locally and then publish to Fission.

The [[Garden and the Gazebo]] has a write up about the setup and the thinking behind what, why, and how.

## bmann wiki, `bmannconsulting.com` WikiJS (May 2020)

As of May 2020:

- Did some research on Markdown-based flat file / git wikis, thinking about integrating with [my blog](https://blog.bmannconsulting.com)
- After looking at the options, keeping the wiki separate and keeping it as WikiJS still makes sense; this was originaly `wiki.bmann.ca` (which now redirects here) and the bulk of it was food / travel stuff aka [[Duck Ramen Wiki]]
- Imported the [[Jekyll]]-based blog that was at `bmannconsulting.com` into the [[Archive]] including bringing in some trimmed and posterous-era stuff back online

_Still a WIP, and will write up a blog post once things have settled_

## `wiki.bmann.ca` WikiJS (Aug 2018)

As of August 6th, 2018:

- Running on [[WikiJS]]
- Hosted on [[Heroku]], initially installed using the Heroku deployment
- Git is stored in a private [[Gitlab]] repo

## `wiki.bmann.ca` Tiddlywiki (Nov 2016)

- [[TiddlyWiki]], on or around 5.1.13.
- Running on Google AppEngine using Russ Cox's [tiddly](https://github.com/rsc/tiddly) Go server at `wiki.bmann.ca`
- The Favicon is a bowl of Duck Ramen made in Victoria during a Nov 2016 visit: [[Duck Ramen Wiki]]




