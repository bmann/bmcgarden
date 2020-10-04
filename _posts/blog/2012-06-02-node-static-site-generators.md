---
layout: post
title: "Node based static site generators"
description: "A review of available node.js based tools"
categories:
- Web Development
- Blogging
tags:
- Octopress
- Markdown
- Node.js
- Harp
- static site generator
---
My first experience with node.js was following the ['hello world' tutorial on the front page](http://nodejs.org), which I then extended to experiment with writing in Markdown and creating HTML pages on the fly. Not quite a static site generator, but a [fun experiment in learning during the Mozilla Polyglot Hackathon](http://projects.bmannconsulting.com/nodejs-getting-started/).

I'm currently using Octopress to power this site as well as bmannconsulting.com (see my [migration write up](http://www.bmannconsulting.com/archive/migration/)), but one of the things I'd like is the ability to not have to have access to my dev environment in order to publish pages. That is, right now I can create/edit Markdown files anywhere<sup>[1](#markdown-editors)</sup> since my blog source is in Dropbox, but to compile / publish it, I need access to a machine that has the development environment installed.

I am hoping to use a node.js-based static site generator running on Heroku or Nodejitsu to have the best of both worlds. A minimal http server to serve up  the baked HTML static files, plus the ability to connect to a Dropbox folder with Markdown posts in it and bake them on demand.
<!-- more -->
My first stop was to look at the existing node.js-based static site generators. I was looking for something with the simplicity and elegance of Octopress. To me, that means simple, one file posts with included metadata plus simple, as close-to-HTML as possible templating. Here's the list of projects I found, with a few notes on each one.

##[Wintersmith](http://jnordberg.github.com/wintersmith/)

* Source Link: [github.com/jnordberg/wintersmith](https://github.com/jnordberg/wintersmith)
* Last Updated: < 1 month ago
* Pros:
	* Small, discrete code base, including [plugin architecture](https://github.com/jnordberg/wintersmith/wiki/Plugins)
	* Under active development
* Cons:
	* Jade-based templates
	* Written in CoffeeScript

## DocPad

* Source Link: [github.com/bevry/docpad](https://github.com/bevry/docpad)
* < 1 month ago
* Pros:
	* Does a LOT.
	* Under active development
* Cons:
	* Overkill - support for the many templating options plus using CoffeeScript makes it hard to start hacking on

##[Blacksmith](http://blacksmith.jit.su/)

* Source Link: [github.com/flatiron/blacksmith](https://github.com/flatiron/blacksmith)
* Last Updated: ~ 2 months ago
* Pros:
	* Has a generator and a server
	* HTML-based templates
* Cons:
	* Metadata for posts in separate json file & each post in a separate folder
	* _Updated:_ incorrectly stated Jade-based templates - actually uses HTML-based templates

## Scotch

* Source Link: [github.com/techwraith/scotch](https://github.com/techwraith/scotch)
* Last Updated: ~ 3 months
* Pros:
	* Comes with a redis-based cache, but can also compile to static files
* Cons:
	* Needs geddy and redis running
	* Couldn't get it working

## Wheat

* Source Link: [github.com/creationix/wheat](https://github.com/creationix/wheat)
* Last Updated: ~ 6 months
* Pros:
	* Serves files from a git repo
	* Runs the the [howtonode.org](http://howtonode.org) website
* Cons:
	* Couldn't get it running
	* HAML templates

## Petrify

* Source Link: [github.com/caolan/petrify](https://github.com/caolan/petrify)
* Last Updated: 11 months
* Pros
	* Interesting JSON templates
* Cons:
	* Generator only
	* Couldn't get it running (outdated "require path" syntax)

Wintersmith comes closest to being what I want. It's maintained, works well out of the box, and has a minimal codebase. But, the double whammy of being written in CoffeeScript and using Jade-based templates by default makes it a no go. There is a plugin for [Swig templates](https://github.com/paularmstrong/swig), so perhaps I'll keep experimenting with it.

After all of that, none of the existing node.js-based SSGs seem like a great fit for adding Dropbox support for. So, I'm going to attempt to write one myself. To recap what I'm looking for:

* Site generator plus simple server for local previews + easy PaaS hosting
* Minimal, close-to-HTML-based templating
* Single file posts that include metadata
* Easily hackable for node beginners (i.e. not written in CoffeeScript)
* Killer feature will be Dropbox integration where a folder is watched and files are auto-published

I think the on-disk format and general feature set of Octopress is excellent, so a secondary goal will be to try and follow the guidelines of source files & metadata that Octopress supports as much as possible.

If anyone has pointers to code or libraries that might be a good starting point, please leave a comment.

--------------

###<a name="markdown-editors"><sup>1</sup> Markdown editors:</a>

I currently have three different Markdown editors on my iPhone.

* [WriteUp](http://writeup.prasannag.com/) ([app](http://bit.ly/writeup-bmann)): This is the app I started with. Great Markdown and Dropbox support. Cool new feature is support for Versions.
* [Byword](http://bywordapp.com/) ([app](http://bit.ly/bywordapp-bmann)): Focused on distraction free writing in Markdown, and that's it. I'm also using it on my desktop for full screen writing.
* [Writing Kit](http://getwritingkit.com/) ([app](http://bit.ly/writingkit-bmann)): I've just added this app, which features the ability to do research with a built in web browser / search. I'll likely be using this to do research & grab links, and then do the majority of my writing in Byword.

### Update September 8, 2013

<a href="http://harp.io"><img src="/images/harp-logo-dark.png" align="left" style="padding: 10px 10px 10px 0px" /></a>This blog is now running on the [Harp Platform](http://harp.io), which is a node.js-based web server with pre-processing built in, and you upload files via Dropbox. Check out the [open source HarpJS site](http://harpjs.com) if you want to run it on your own. _Disclaimer: I am working with the Harp team and couldn't be happier at using it._


