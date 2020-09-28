---
layout: post
title: "Setting up OS X Mavericks with Homebrew, Cask, and rbenv"
description: "Automating new system setup"
image:
  feature: 2014/homebrew_bottlecaps_daveshea.jpg
  credit: Dave Shea
  creditlink: https://www.flickr.com/photos/mezzoblue/6171620368/in/photostream/
categories:
- Mac OS X
- How To
tags:
- Ruby
- Homebrew
- rbenv
- Mavericks
- Node.js
---
You've got a freshly built OS X Mavericks 10.9 system and it's time to start loading up the usual apps you use and setup your development environment.

Luckily, there are lots of great developer tools for automating this task.

I learned some new tricks (e.g. Homebrew Cask) from [Tadej Murovec's post](https://coderwall.com/p/y1dqra). And, my [Macbook Air is now 2 years old](/setting-up-macbook-air-osx-lion/) and all the command line tools / versions have changed, so I needed to re-document this for myself.

## App Store

Your first stop is the App Store, where you can visit the Purchases tab and re-download items you've bought.

You're going to need Xcode[^1] for your development environment (and it's a big download), so get it going.

 * Xcode
 * Evernote
 * Tweetbot
 * Keynote
 * Pages
 * Slack
 * Byword

I used to use NeoOffice, which has now [moved to the App Store](https://itunes.apple.com/us/app/neooffice/id639210716?mt=12&uo=4). I will likely end up paying $30 and buying it.

Also: launch and sign in to Evernote right away. If you have a lot of info in Evernote, it will need to download and cache a lot of metadata (for me it was 4GB).

## Xcode

In Xcode[^1], under the main Xcode menu, select _Open Developer Tools > More Developer Tools_. This will open a browser load the [Apple developer site](https://developer.apple.com/downloads/index.action?name=for%20Xcode%20-).

[^1]: If you don't need all of Xcode, you can now just run this on the terminal: <code>xcode-select --install</code>

Download command line tools & install them.

## Homebrew

[Homebrew](http://brew.sh/) lets you manage and install a number of command line development tools. Copy and paste the [one liner listed on the home page](http://brew.sh/) to download and get it running.

To check if everything is OK after it's installed, you run this:

``brew doctor``

## Homebrew Cask

[Homebrew Cask](http://caskroom.io/) is a new add-on to Homebrew that lets you install Mac apps from the commandline as well. I'm just getting started with it and am still learning.

``brew install caskroom/cask/brew-cask``

## Mac Apps

Here are the apps you can use Cask to install. You can run ``brew cask search`` to see if a desktop app is available.

Get Dropbox installed right away so it can start syncing your files in the background as well.

I'm actually starting to do more experimentation with [Barrucada's Copy.com](https://copy.com?r=QR3QTg), a very similar competing service. One of the interesting differences is simple [company accounts](https://www.copy.com/companies).

[Use my link to signup for Copy and both of us will get an extra 5GB »](https://copy.com?r=QR3QTg)

``brew cask install dropbox``

``brew cask install google-chrome``

I have a couple of games that I've purchased directly, but most I buy and install via Steam.

``brew cask install steam``

OmniGraffle is still my go-to tool for professional diagraming, from marketecture to wireframes and site maps.

``brew cask install omnigraffle``

I switched off of Sublime Text and am trying [Atom](http://atom.io).

``brew cask install atom``

## Heroku Toolbelt

[Heroku Toolbelt](https://toolbelt.heroku.com/) is what you'll need to manage your Heroku apps.

``brew install heroku-toolbelt``

## Postgres.app

Heroku are also the maintainers of [Postgres.app](http://postgresapp.com/), a Mac-friendly Postgres database install.

``brew cask install postgres``

_When run, it will want to move itself to the Applications directory_

You're still going to want to install the command line version of Postgres, since other apps want the libraries it installs with.

``brew install postgres``

## Ruby

Now it's time for the rubys! I use _rbenv_ as my Ruby version manager, so I start there.

``brew install rbenv``

``brew install rbenv-gem-rehash``

``brew install ruby-build``

Now install a newer version of Ruby and set it as the default.

``rbenv install 2.1.2``

``rbenv global 2.1.2``

Update the gem system and install the Rails / Ruby basics.

``gem update --system``

``gem install bundler jekyll rails``

## Node

Compared to the drama of getting a local Ruby environment up and running, Node seems to still be a lot simpler.

``brew install node``

### Update January 2015

These instructions work just fine on Yosemite as well.

I removed the Homebrew one-liner, since it has changed in the mean time, and added the footnote about the Terminal commmand for Xcode.

I've also finally gotten around to maintaining some [dotfiles](https://dotfiles.github.io/), which I keep in Dropbox and symlink into my home folder.
