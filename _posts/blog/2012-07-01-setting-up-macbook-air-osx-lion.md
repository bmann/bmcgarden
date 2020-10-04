---
layout: post
title: "Setting up a new MacBook Air plus Lion"
description: "Why I got the 11inch Air, must-have apps, and setting up Ruby"
categories:
- Mac OS X
- How To
tags:
- OS X Lion
- Ruby
- MacBook Air
- Evernote
- Byword
- Dropbox
---

I've long used [Norse Mythology](http://www.akasha.demon.co.uk/norse.htm) to name my computers. The tiny but powerful 11" Macbook Air got named after _Skidbladnir_, Freyr's collapsible ship.
<!-- more -->
## Why I got the 11" Air

I was looking for a home computer. One that would sit on my desk and be used for personal projects and some gaming. I wanted something low cost but that would handle anything I threw at it.

I was considering a Mac Mini or an iMac as my non-laptop choices. Having a laptop means being able to use it for personal travel as well, although that was not a huge factor in making the decision.

The Mac Mini came very close, but the graphics card seemed a little weak. When thinking about using FaceTime or Skype, I realized that I'd also have to invest in a separate webcam, which was one too many strikes against the Mini.

The iMacs are great machines to have sitting on your desk. You need to get higher end versions to get the "better" graphics card, but they are all great choices. The more I looked at the different iMac configurations, the knowledge that there was an upgrade somewhere not too far away for the entire iMac line up meant it wasn't the right choice.

So it was back to looking at laptops. I knew I didn't need a fully tricked out machine, and that I had a 22" monitor sitting at my desk, so screen size wasn't an issue. I also have a large 1TB external drive, so lots of storage wasn't important either.

With all that, the [MacBook Air 11"](http://www.apple.com/macbookair/specs.html) ended up being a great choice. I bumped up the memory to 8GB and decided to spring for the faster i7 processor, and I think it's going to be a great machine. Being able to write this post with the machine on my lap on a crowded 257 bus headed to Horseshoe Bay just underlines what a nice portable machine this is.

## Apps

I mainly do email, Internet, photo processing, and some web development tinkering with my personal machine.

I've had a BootCamp partition and run Windows on my last couple of my machines, pretty much exclusively to run [Steam](http://store.steampowered.com) and Windows-only games. Since I've got Diablo 3 to suck up what little gaming time I have, I'll keep this machine Windows free for the moment.

Most of the desktop apps I end up installing over time are mainly for experimentation – few of them seem to stick. I expect this trend to continue, although I think that "local" clients – either through sync or APIs – will appear more often as well.

The first couple of must have desktop apps that I've installed are:

* Evernote - all my notes are here, available on all devices
* [Byword](http://bit.ly/bywordapp-bmann) - since switching my blog over, I've experimented with different ways of writing Markdown; Byword has been great, especially in full screen mode, for long form writing
* [Dropbox](http://db.tt/ntZKNydx) - I'm lucky enough to have just over 7GB of free space. Aside from photos and code repos, all of my files are here.

My long time favourite basic programmer's text editor is [Smultron](http://www.peterborgapps.com/smultron/). It's now gone closed source and available in a [classic version](http://itunes.apple.com/us/app/smultron/id408831307?mt=12&ls=1) and a Lion-only [4.x version](http://itunes.apple.com/us/app/smultron-4/id450194894?ls=1&mt=12). I'm thinking of attempting another try at learning & committing to a real UNIX-y editor. For now, emacs (the [AquaMacs version](http://aquamacs.org/)) is what I'll try.

## Command Line

Ruby and Jekyll / Octopress are the first things I need to get up and running on the command line so that I can get this blog post published ;) As well as setting up a new machine, this is my first time on OS X Lion, so it was interesting to see what I had to do to get my development environment up and running.

* Create / copy over <code>.bash_profile</code> to my home directory
* If you've already installed XCode, then run Preferences > Downloads, click on Components and install the command line tools
* Otherwise, just install [OS X GCC Installer](https://github.com/kennethreitz/osx-gcc-installer) (which you may need for certain code builds regardless)
* Install [Homebrew](http://mxcl.github.com/homebrew/), then edit <code>.bash_profile</code> to include <code>export PATH="/usr/local/bin:$PATH"</code>
* Install newest Ruby <code>brew install ruby</code>, then edit <code>.bash_profile</code> to include <code>export PATH="/usr/local/Cellar/ruby/1.9.3-p194/bin:$PATH"</code>
* Install Jekyll <code>gem install jekyll</code>
* Install Octopress - follow the [docs](http://octopress.org/docs/setup/); I have the source already in DropBox, so just need to install the various dependencies via <code>gem</code>. You may have trouble installing <code>rb-fsevent</code>, in which case you'll need this [magic incantation](https://github.com/thibaudgg/rb-fsevent/issues/26#issuecomment-4050279): <code>sudo xcode-select -switch /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/</code>
* I'm hosting on Heroku, so I also needed <code>gem install heroku</code>

That's it for the first couple of hours with the new machine. I'm sure there are some Lion-only apps and features that I need to dive into. Trackpad gestures + Mission Control + multiple desktops on this small screen is great so far.

*I'm very new to Ruby still – I ended up installing _rbenv_ to manage different versions, but I don't know that I'll even need to get into that