---
layout: post
date: '2019-06-10T10:00:14.667Z'
title: iPad Tools
tags: iPad, iOS, mobile, development
categories: "How To"
comments: true
---
I’ve been using an iPad Pro 11" as my daily machine for about 2 months now. Here are some of the tools I've been finding useful.

After using a Chromebook for a year, the thing that made me want to do this is Keynote. My cofounder Brooke and I have been working on one pagers and presentations, and nothing else is better than Keynote.

I mean, I know this. In my career, I’ve been an expert at both PowerPoint and Keynote, but really Keynote is just a pleasure to use. I’m productive, quick, and end up with better presentations.

I mean, I _also_ do stuff like use Markdown in HackMD to create presentations, so don’t take away my geek cred quite yet.

I bought the iPad with the new Apple Pencil, and then separately got a third party case and a Logitech Bluetooth keyboard. The all in one cases from Apple or Logitech didn't seem like a fit for me, and having the keyboard separate means I can get a great kyeboard which is still small, and position it so it's good for typing.

In using the iPad, I’m also looking at it through the lens of using it as a professional creation device. With that in mind, paying for apps that make working easier is a no brainer. And when I say paying for apps, I don't mean 99¢: business apps that are one time purchases can easily charge a lot for the value they deliver.

On the other side, I'm also looking to understand which apps I'm committing to which aren't open source and/or don't use open source protocols. That deserves a blog post of its own.

## Coding Apps for iPad

Aside from lots of email, presentations, and working inside a number of different web apps, my first step was to see about getting the iPad setup for coding. At least, my kind of coding, which is connecting to remote shells, editing some wikis and Jekyll sites via git. 

### Working Copy
I have paid for [Working Copy](https://workingcopyapp.com/) on my iPhone, which is an incredible full featured git client that pushes and pulls from other apps on iOS with deep integrations. But I’ve barely used it on the iPad since I found...

### Buffer Editor
I hadn’t heard about [Buffer Editor](https://buffereditor.com/), but decided to give it a try. It’s got Git integration, syntax highlighting, multiple open editor tabs. 

It can open files from many different remote locations, and then save them back to that location.

![](https://images.bmann.ca/blog/IMG_0064-1560040454.PNG)

In writing this up, I just found out that it will open an SSH terminal window, too. Now I just need it to support Mosh.

I don't have much more to write about it, because it pretty much just works. I wrote this article in it and committed it via Git, which then published this blog post.

### Blink Terminal

[Blink](http://www.blink.sh/) is a terminal that runs on your iOS devices. Like, with shell utilities and Python and TeX and Lua even. MoSH support with keys and everything.

And it’s open source. It’s a one time payment. Purchased!

The [home page](https://www.blink.sh) has lots of info and App Store download links. The [GitHub README `blinksh/blink`](https://github.com/blinksh/blink) goes into more detail on what shell programs you have access to.


Here I'm connected to an ubuntu system. Not very exciting, it is a full screen terminal after all!

![](https://images.bmann.ca/blog/IMG_0062-1560040455.PNG)

---

BTW, [MoSH](https://mosh.org) aka "Mobile Shell" is an SSH replacement that’s made for on-the-go connections that never drop. It connects over SSH and then uses a Mosh app that you can easily install on your server.

### Termius
Termius is an SSH/SFTP/Mosh/Telnet client ... and it does a lot more, like [Port Forwarding](https://docs.termius.com/termius-handbook/port-forwarding).

I used it originally on my iPhone, and it recently got an upgrade and a number of Premium / paid subscription features. Without a subscription, your server settings don’t sync between devices. For now, for my purposes, the free / Basic version works just fine.

I am going to do some Port Forwarding experiments, since this may be the final piece in being able to develop on a remote server, which has a preview app running in the browser, which I can then forward to my local iPad? We’ll see!

![](https://images.bmann.ca/blog/IMG_0061-1560040455.PNG)


### Amazon Lightsail VPS with xrdp and Jump Desktop

There are still many apps that are desktop only, especially the crop of decentralized p2p apps I am experimenting with. So along with a remote machine for full shell access, I [installed xrdp for Ubuntu using this article](https://medium.com/@vivekteega/how-to-setup-an-xrdp-server-on-ubuntu-18-04-89f7e205bd4e). This boils down to the following:

```
sudo apt-get install xrdp
sudo apt-get install xfce4
sudo sed -i.bak '/fi/a #xrdp multiple users configuration \n xfce-session \n' /etc/xrdp/startwm.sh
```

The one tweak (once I sorted some username / password issues from creating a new user) was to edit the `/etc/X11/Xwrapper.config` allowed users setting from console to anybody.

[Jump Desktop](https://jumpdesktop.com/) is an RDP / VNC client that lets you connect to these remote desktops, and it even has support for Apple Pencil as a pointing device.

Here's Jump Desktop connected to Ubuntu running Xfce:

![](https://images.bmann.ca/blog/IMG_0063-1560040454.PNG)

The Microsoft RDP client may work for you as well -- it has fewer features, but is free.

_Note: I’m running this on an Amazon Lightsail VPS instance, so you do need to edit firewall settings to allow RDP connections._

## New to Me Apps

Other than coding specific apps, there are a handful of other apps that I've dug into recently.

### iA Writer

I had heard lots of good things about [iA Writer](https://ia.net/writer) but was fine with Byword for Markdown editing for a long time, since it was mainly quick on the go stuff. For longer writing and lots of it, iA Writer is great.

A pleasant surprise was direct support for the [Ghost blogging app](https://ghost.org), which [runs the FISSION blog](https://blog.fission.codes). You can write in iA writer and then push drafts to your Ghost blog.

I’m missing image support, but this will be tricky to integrate. An open source Markdown editor with configurable image file upload support and connections to different systems? Yes please!

Between Joplin and iA Writer as native apps, and Ghost and Discourse in the browser, I’m writing a lot of Markdown. Never mind editing blog posts or wiki pages which are all Markdown too.

### GoodNotes 

I went looking for apps that work with Pencil. I’ve always **wanted** to go all digital with notes and scribbling, and it looks like [GoodNotes](https://www.goodnotes.com/) is the best fit for what I want.

I’ve used it for some personal tasks, like importing a PDF of RPG character sheets, which you can then fill out by writing or typing on top, and re-use infinitely.

Currently GoodNotes syncs automatically using iCloud. I’d love to see it support configurable document storage.

I’d love more recommendations on Pencil-friendly apps that are worthwhile.

### Brave

On iOS, you’re using the same WebKit engine for all browsers, but I still thought it was a good idea to have [Brave on my iPad](https://brave.com/ios/). I do less browser-y things on my iPhone, so just use Safari there. As well, with the iPad SplitView, it means I can have one or both browsers docked into different apps.

Other than committing to different sync / identity systems, it would be interesting to see what the differences for the iOS browser implementations truly are. Anyone have insight on big differences?

### AWS S3 Manager
I’ve been meaning to write about this for a while, so it’s going to get shoved into this iOS apps article :)

I wrote a post a while back about syncing files from iOS to S3. The Archivist was never perfect, and it now crashes on launch on all my devices. Doesn’t look like it’s getting a lot of updates. Dropshare works, but really only for individual files.

I tested a ton of different apps that claimed to work with S3, didn’t have a monthly subscription, and I can’t believe this is the only app that even sort of works, but it does, and if you want to upload files to S3 from your iOS device, this is the one to get: [AWS S3 Manager](https://itunes.apple.com/ca/app/aws-s3-manager/id1352683230?mt=8.)

## A note on Files

Amusingly, while Brooke is all Apple, she doesn’t use iCloud, so Keynote shared editing was a little bit more painful than it needed to be. I did find that you can actually set the default Document Storage for Keynote (and other apps that have implemented this), so you can use any file storage system that hooks into this API. 

![](https://images.bmann.ca/blog/IMG_0066-1560280244.PNG)

So yes, I’m definitely going to have a long discussion with the [Textile](https://textile.io) team about collaborating on an IPFS files plugin for iOS.

## Other Apps

Some of the other apps that I use personally / [at work](https://fission.codes) include: 

* [Tweetbot](https://tapbots.com/tweetbot/): I couldn’t use Twitter without this app. I pay for it whenever they have a paid upgrade, and recently added an in-app "tip"
* [Missive](https://missiveapp.com/): it’s the email client that turns email into a team sport; we use it to share, delegate, copy edit, and comment on email at work. Works really nicely on Chromebooks as well as native apps for desktop and mobile.
* [Joplin](https://joplinapp.org/): a personal notes / to-do app that is meant to be a clone of Evernote, but under your own control. It’s open source, and you bring your own backend to store notes in, which are encrypted with your own keys / password. I use Dropbox to store my files. 
* [Discord](https://discordapp.com/): the community + internal company chat messaging system we’ve settled on. It’s not open source, but it has a full API and features specifically built for access control and moderation. Of course I have every other messaging platform client in the known universe installed as well, but Discord is the one we settled on. I’m looking forward to integration and more long form content on our [FISSION Discourse forum talk.fission.codes](https://talk.fission.codes)
* [GitHawk](http://githawk.com/): open source GitHub client, so you can look through all your notifications, respond, triage issues, and so on, on mobile

## Next

Whether it's a Chromebook or an iPad, I can get work done anywhere. I'm still interested in a new Chromebook in the [ASUS Flip C434 series](https://www.asus.com/ca-en/Laptops/ASUS-Chromebook-Flip-C434TA/). 

With iPadOS being announced, we'll see what direction that takes iPads. With touch, pencil, **and** the ability for external connectivity through USB-C and Bluetooth, there are a lot of options.

I'm inspired by [Ink & Switch's Muse prototype iPad app](https://www.inkandswitch.com/muse-studio-for-ideas.html), while at the same time trying to get basic 1970s terminal functionality on the same device.

Tell me what is and isn't working for you on iPad, and what your favourite apps and workflows are!: