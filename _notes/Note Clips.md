Notes on making a cross-tool drag and drop capability. 

What if you could open your [[Digital Garden]] / Second Brain / Spatial Canvas / Notes website in a browser, and open any other web page, and drag and drop content into your own site?
## TiddlyWiki Drag and Drop

[[TiddlyWiki]] has had this as a built in functionality for a long time. Founder [[Jeremy Ruston]] demos it here:

https://www.youtube.com/watch?v=axgRphzRPMU

This showcases two TiddlyWiki websites which are aware of the native “tiddler” format and so can import and drop in tiddler links within those systems. 

## Format

An agreed upon JSON format with a subset of Markdown or similar. 

* URL source
* link if the resource has a link
* Author
* Date clipped 
* Publish date
* Title
* “Note” / clipping body
* Excerpt/ Description with known character limit. Suggestion: 300 to fit within [[ATProtocol]] microblogging lexicon

This might actually be relevant around [[Farcaster#Frames]] too — we should think about these things as social objects. Having [[OpenGraph]] header meta elements would be good when an entire page is being clipped.

Could [[ATProtocol]] Lexicon be a useful definition?

## Interop

Can we make a format and some widget code that enables this for any website?
### Git-based Static Sites

This website is built in the [[Digital Garden Jekyll Template]] with a bunch of my own mostly display customizations. 

Since it’s stored in a git repo on GitHub, it might be possible to accept such a drag and drop and then send it as a PR or an issue where I could accept and merge it. 

### Targets

[[TiddlyWiki]] - can we make an adapter to accept TiddlyWiki and then transform it? A TW plugin could accept (or produce!) a new Note Clips format.

[[TLDraw]]

[[Obsidian]] - don’t know if Obsidian Publish has APIs? Would probably need to be done as a plugin which is slightly less fun than doing it between two web browser windows.

[[Subconscious]] - this is kind of perfect for Noosphere and we should also talk to them about their IPLD structures. 

iOS / Android Share sheet format - what kind of structured data is possible with share sheets?
## Features

Ideally you’re clipping these notes and getting metadata that the source website is giving you, with some minimal set. 

[[Quotebacks]] are a nice display format. 

It would be nice to enable [[transclusion]] but that likely requires the source website to be running something as well. 

A spatial canvas / node view might add something interactive. Kind of like my [[notes]] node view. This would be amazing if you could surf across websites 

Webring vibes?
