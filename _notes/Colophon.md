---
tags:
  - BMC
---
## October 2024

Turned off publishing to [[Fission]]. Just plain old Github Pages now.
## January 2024

The site is still powered by [[Digital Garden Jekyll Template]]. Using [[Obsidian]] to edit on desktop and mobile, with git for syncing. Obsidian wikilinks are compatible with the Jekyll template processing. The only manual thing is that image links need to be relative Markdown links rather than wikilinks.

[[notes|Notes]] are slowly building. Links marked with `[[` wikilinks still point to the old [[LogSeq]] notes site, which is slowly being imported.

Added in a [[Journal]] section and a journal post type.

Made a journal feed linked at [[feeds]]. As of January 15th, 2024, am using [[Fedica]]'s RSS cross-posting features to post those feeds.

To Do: [[BMC]]

### Archive of 2023

Removed blog posts going back to 2012 and pre-2012 archive. They are available via a snapshot at [2023.bmannconsulting.com](https://2023.bmannconsulting.com).

Published via [[Fission]] Github Action, and then grabbed the [[IPFS]] hash `bafybeidfdwz5tak24oukds2hrf3xahl5rp5by4a6idwv2ucsmo6uaafgoa` and used [[Cloudflare]] IPFS Gateway to keep it around.

## July 2023

Trimmed blog & archive posts out of [[LogSeq]] and moved them into [[Digital Garden Jekyll Template]]. Notes, running [[LogSeq]], have moved to <a href="{{ site.notes_url }}">{{ site.notes_url }}</a>. Wikilinks that don't have local links link out to the Notes site. Sidebar tags for blog posts also link out to the Notes site.

The most recent 5 blog posts appear on the home page. The [blog index](/blog/) goes back to the 2012 migration, with previous posts in the [archive](/archive/).

[[Seeds]] is a page that provides an entry way into my Notes site.

There is a [Backlog](https://notes.bmannconsulting.com/#/page/bmc%2Fbacklog) of things in progress.

This site is published to [[IPFS]] using [[Fission]] Github Actions.

## Time Passes

End of December 2022, poured the whole site into [[LogSeq]]. There is an archived [snapshot of 2022 Simply Jekyll](https://2022.bmannconsulting.com).

## September 2020 Simply Jekyll

[[Simply Jekyll]] theme for Jekyll. If you want to run it yourself, I've got some public work around this with the [[Simply Jekyll Template]].

Using [[VSCode]] on my desktop to edit.

Hosting on [[Fission]]. [[Cloudflare]] is powering the DNS and using [[Cloudflare IPFS Gateway]].

Source code is public on Github at [bmann/bmcgarden](https://github.com/bmann/bmcgarden). [[Connecting to the Agora]] as of jan 24th, 2021.

Changed fission app from `ancient-aquamarine-metalic-princess.fission.app` to `bmcgarden.fission.app` and updating Cloudflare.

Switched over Notes and Links pages to use `modified`. Added Git Links to the Links page. Disabled the jekyll last_modified plugin, which never seemed to work in any case.

## July 2020 Archive Import

The long(er) form content from the (original) `blog.bmannconsulting.com` has all been imported here as an [archive](../archive/).

I swapped that blog domain to Micro.blog and that's where I post photos and short content, and sort of more non tech bloggy content. Yes, there is a [colophon there too](https://blog.bmannconsulting.com/colophon).

## May 2020

This blog is currently powered by [Jekyll 4](http://jekyllrb.com) hosted on [Netlify](http://netlify.com). Netlify builds the site from a private git repo on Github.

I write short [social posts](https://blog.bmannconsulting.com/archives/social/) on my phone via [micropub](https://blog.bmannconsulting.com/tags/micropub/). There are a variety of [micropub clients](https://indieweb.org/micropub-clients) you can browse on the IndieWeb site. The [Indigenous native app for iOS](https://indieweb.org/Indigenous_for_iOS) works most reliably.

I also use [Quill](https://quill.p3k.io/docs) as a <abbr title="Progressive Web App">PWA</abbr> on my phone. It also works great for all kinds of posts on desktop browsers too, including a first draft of long posts.

Long posts are most often finalized in [VS Code](https://code.visualstudio.com/) and published via git.

Full size images are uploaded and stored in git. Various thumbnail sizes are generated on the fly via [images.weserv.nl](https://images.weserv.nl/).

[All the Best Recipes](https://allthebest.recipes) are where the long form food / cooking posts go, although I often share them via links and images posted as social posts here.

My [@bmann Instagram](https://instagram.com/bmann) I manually post to, either a variant of a social post I've already made here, or on the All the Best Recipes site. I cross post to Facebook from Instagram. My "rule" is no posting pictures to Instagram until they've been put somewhere permanent under my control. There is also an [@allthebestrecipes Instagram](https://instagram.com/allthebestrecipes), because really I need more places to post about food.

I'm now running [paulrobertlloyd's IndieKit](https://paulrobertlloyd.github.io/indiekit/) micropub server, and tweaking the display, feeds, and cross-posting to [Micro.blog](https://micro.blog/boris), which in turn posts to [my @bmann Twitter account](https://twitter.com/bmann).

You can visit [my micropub server](https://bmann-indiekit.herokuapp.com) to learn more about it. The post types that I have special display and treatment for are:

* Article -- long form posts in the Blog category by default
* Note -- the vast majority of short posts, often with images attached
* Bookmark -- so I can keep my bookmarks local
* Reply -- because I wanted to support it for leaving comments on other people's posts. This is also the RSVP type, which I've just added extra support for

The others work, I just haven't coded special treatment for them, so they likely don't display correctly.

Turned off `jekyll-feed` plugin to have Jekyll generate a custom [RSS feed](/feed.xml), because of the way I customize different kinds of micropub posts.

<hr />

## Previous Editions

### Jekyll 3 on Netlify (Minimal Mistakes)
August 2018 - May 2020

I write on my phone or my Chromebook. On the Chromebook, [Caret](http://thomaswilburn.net/caret/) is a text / coding editor I use. The [Netlify CMS](https://www.netlifycms.org) lets me edit in a browser.

Short form links get sent to Twitter and/or shared on the [Frontier Community](https://community.frontierfoundry.co)[^deprecatedff]. My [Tumblr](http://tumblr.bmannconsulting.com) is rarely used. Tweets are archived at [tweets.bmannconsulting.com](http://tweets.bmannconsulting.com).

[^deprecatedff]: The Frontier Community Discourse site got turned into [All the Best Recipes](https://allthebest.recipes). I might re-use it for comments again in the future, for now have Webmentions turned on.

tldr; the Netlify CMS doesn't support drafts on Gitlab, so put things back on Github.

Also moved to [Michael Rose's Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/). Fighting with nokogiri on the Chromebook means no emoji. This meant posts have a slightly different default layout again: ```sed -i 's/layout: posts/layout: single/' *.md```.

Netlify CMS is technically still installed, but rarely used.

**In September 2018**, I  [added a bunch of IndieWeb and Micropub interfaces](https://blog.bmannconsulting.com/micro-blog-jekyll-micro-pub-and-indie-web/) and created social posts and bookmarks.

While [OwnYouGram](https://ownyourgram.com/) was working, I posted to [my @bmann Instagram](https://instagram.com/bmann), and those posts would automatically be republished on this site.

Somewhere around this time frame, JSON feeds were added at [micro.json](/micro.json), [micro-bookmarks.json](/micro-bookmarks.json), and [feed.json](/feed.json), and syndicated to [Micro.blog](https://micro.blog/boris), which I pay to re-publish on other networks. Briefly they went to LinkedIn, now mainly get sent over to Twitter.

**In May of 2019**, I [added a Webmentions server](https://blog.bmannconsulting.com/run-your-own-web-mentions/).

### Jekyll 3 on Netlify
June 2018 - August 2018

Most writing happened on Medium after November 2014 across various company publications, with the [medium.bmannconsulting.com](http://medium.bmannconsulting.com) subdomain being the one where permanent posts end up. I should probably get around to getting a Medium download so I have them.

To upgrade, I did some yak shaving.

I created a new Gitlab [borismann](http://gitlab.com/borismann) and imported from Bitbucket. I connected Netlify to it, but it failed to build. Digging in, I created a new branch <code>2018-reboot</code> and deleted the <code>Gemfile.lock</code>, and edited <code>Gemfile</code> to use Jekyll 3, a newer Ruby, and nuked the rack stuff. <code>bundle install</code> got things going.

There is some nonsense with the file watching not working, so <code>bundle exec jekyll serve --no-watch</code> was needed.

The default post type is now "posts", which meant replacing across all files [using sed](https://unix.stackexchange.com/questions/112023/how-can-i-replace-a-string-in-a-files/112024#112024): <code>sed -i 's/layout post/layout: posts/' *.md</code>.

<code>layout: none</code> used for the feed and sitemap is now <code>layout: null</code>.

Yay! It builds. Edit CNAME to point at Netlify. Enable HTTPS.

While I was at it, I also migrated the [bmannconsulting main archive](https://www.bmannconsulting.com) to Netlify as well.

### Jekyll 2 on Heroku
August 2014 - November 2014

This blog is powered by [Jekyll 2](http://jekyllrb.com) hosted on [Heroku](http://heroku.com). I'm using [Andy Croll's RackJekyll instructions and buildpack](http://andycroll.com/2014/01/19/serving-a-jekyll-blog-using-heroku/) so that the site is generated on the server.

I'm increasingly a fan of static site generators for content-focused publishing projects. I've written both a [presentation on static site generators](/ssg-lightning-talk) and an overview of [node.js-based generators](/node-static-site-generators).

The design is [GPLv2 licensed, So Simple by Michael Rose](http://mademistakes.com/articles/so-simple-jekyll-theme/).

The comments are powered by [Disqus](http://disqus.com). All comments are welcome, although I reserve the right to tell you to go post your thoughts in your own space somewhere.

Tweets to new stories are scheduled using [Buffer](https://bufferapp.com/) and published on my [@bmann](http://twitter.com/bmann) account.

The domain _bmannconsulting.com_ is over a decade old. [NameCheap](http://namecheap.com) is the domain registrar and DNS host, and is still my recommendation for new domain registrations.

Posts are typically written in Markdown with [Byword](http://bit.ly/bywordapp-bmann) on a Macbook Air or iPad Mini. Code for the site is edited with [Atom](https://atom.io/).

My writing here tends to be long form (1000+ words) original pieces, aside from aggregation-plus-commentary of embedded [Storify](http://storify.com) content. For example, this piece on [the Microsoft Surface launch](/reactions-microsoft-surface). The content is also rarely personal, mainly focusing on tech-related subjects.

Short form link blog content is at [links.bmannconsulting.com](http://links.bmannconsulting.com), and is powered by [Postachio](http://postach.io), an Evernote-powered blogging platform. I wrote about [link blogging with Postachio](/postachio-link-blogging).


### HarpJS on Harp Platform
April 2013 - August 2014

This blog is running on the [Harp Platform](http://harp.io), a lightweight web server with pre-processing built in, with files uploaded via my own Dropbox account. Also check out the [HarpJS](http://harpjs.com) open source project.

The design is a [CC-BY licensed HTML5 template called Striped](http://html5up.net/striped/), which uses the [skel.js](http://skeljs.org/) front end framework to make the site responsive.

Tweets to new stories are hand-posted using [Tweetbot](http://tapbots.com/software/tweetbot/), although the RSS feed is also syndicated using [dlvr.it](http://dlvr.it) to various places, including [@horse_eboris](http://twitter.com/horse_eboris).

Code for the site is edited with [Sublime Text](http://www.sublimetext.com/).

### Octopress on Heroku
April 2012 - August 2013

I archived my main site to Octopress-generated flat files on Amazon S3, and moved this site to Octopress on Heroku. I wrote up the details of the [migration from Drupal 6 to Octopress and Amazon S3](http://www.bmannconsulting.com/archive/migration/).

For both sites, the entire source was / is in my own Dropbox account, so that I could create drafts and edits on any machine. This site was also in a private git repo on Bitbucket. I still needed to have the entire Ruby / Octopress build chain available on some machine to create new entries.

### Posterous
January 2010 - April 2012

I split off my blog into it's own subdomain. I selected Posterous because I liked built-in comments, and in general it felt more suited to long form writing than Tumblr did. Being able to cross-post back to my main Drupal site so that I would have a copy of the content was also great.

### Drupal (various versions 3.x - 6.x)
November 2002 - April 2012

For the last period, the site was hosted on [Omega8](http://omega8.cc), which specializes in managed Drupal hosting on top of the Aegir mass hosting system. The actual database / content stretched back many versions of Drupal, through a variety of content re-organization and hosting changes.

Comments from this period are currently offline.

### HTML, Pmachine, & Early Experiments
December 2001 - 2003

Bits and pieces of static HTML and various PHP scripts, including [Pmachine](http://en.wikipedia.org/wiki/EllisLab) as a personal blog that ran concurrrently with installs of PHPNuke and later my Drupal site.

