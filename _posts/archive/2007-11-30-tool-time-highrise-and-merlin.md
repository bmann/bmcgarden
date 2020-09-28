--- 
layout: post
title: "Tool time: Highrise and Merlin"
created: 1196419334
categories: 
- Highrise
- 37signals
- Merlin2
- project management
- Raincity Studios
- LDAP
- Web 2.0
---
<p>In <a href="http://www.raincitystudios.com">joining forces with RCS</a> and going from 7 people to 22 people, I'm diving back into tools and process. It's actually quite enjoyable, and I've got some partners in crime that it's been fun to work with.</p>

<p><a href="http://highrisehq.com/">Highrise</a> is something that I'm warming to. Ostensibly it's a contact management tool, but it also does CRM and task management. I like it because it gets rid of giant CC chains in keeping multiple people "in the loop" -- you just BCC the dropbox in Highrise and everyone can follow along, including grabbing attachments sent in email and so on.</p>

<p>But, it wouldn't be a 37 Signals product if it didn't have certain infuriating things about it. Well, maybe not infuriating, but it just leaves me scratching my head. Number one is having to hit "edit" to add an email to a Case (why isn't there just a nice big "Add to Case" button like there is for other activities?). The other is lack of LDAP. Adding LDAP support so that I could easily use my local mail client to get access to all shared contacts just seems a no brainer. I keep wondering when Gmail will do something like this (or, at least, a Plaxo-like "sync" functionality).</p>

<p>Oh, right, and it lets me add new contacts with email addresses that are duplicates of existing contacts. Yeah, there are a couple of things that bug me about it :P</p>

<p>Anyway, on a whole, Highrise is a plus. Lead tracking and pre-project business communications (contracts, scoping, hiring, etc.) are going to be its main tasks, plus "soft" tasks -- e.g. follow up with so-and-so, review this contract, give me your thoughts, etc. I call out soft tasks specifically because there is ALSO Basecamp which has to dos (but not dated to dos, which Highrise does do...oh 37S, how you confuse me and leave me in a puddle of love/hate...). Wonder to what use we can put <a href="http://developer.37signals.com/highrise/">the API</a>.</p>

<p>The other tool is <a href="http://merlin2.net/>Merlin2</a> -- a Mac project management app that <a href="http://www.puregin.org">Djun</a> and I had settled on previously. Scoping, estimating, budgeting, resource allocation -- seems to do a pretty decent job in a nice intuitive way. I keep thinking it would be great to hook it directly into <a href="http://trac.edgewall.org/">trac</a> so you can easily get high level overviews of tasks. This MUST be scriptable in some way, but would need some dedicated time to sit down and work through...</p>

<p>Oh, and what the heck, while we're naming tools, don't forget about <a href="http://unfuddle.com/">hosted SVN / ticket tracking with Unfuddle</a>. I think our trac install is going to go away and be replaced by per-project hosted Unfuddle (for easy hand off to clients -- main uses are developer-granularity tickets and client bug reporting) and an internal Drupal-based wiki/doc repository for the wiki component.</p>
<!--break-->
