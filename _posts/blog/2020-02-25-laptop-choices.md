---
layout: post
date: '2020-02-25T10:53:12.210Z'
title: Laptop Choices
tags:
  - chromebook
  - ASUS
  - ScreenPad
categories:
  - Blog
---
I've been using Chromebooks for several years, have a desktop iMac and iPad Pro that I use, and am considering a new Windows laptop. Here's what I've learned so far and the general options I'm considering. I would love to hear feedback and opinions on what options others are considering!

## Background Notes and Use Cases

For [work](https://fission.codes) I need a command line terminal and access to a browser.

I've been using a Chromebook for several years (more details below), working with either ChromeOS on the command line, or the new Linux app container support to also install Ubuntu.

I went [iPad-only last year](https://blog.bmannconsulting.com/ipad-tools/), including coding.

Personally, I enjoy being able to cloud game, using [NVidia's GeForce NOW service](https://www.nvidia.com/en-us/geforce-now/). Playing things offline / locally is not really required, but is a nice to have.

I have a desktop iMac at home, but find a laptop that lets me work from anywhere to be most convenient.

I experiment with various Linux-y things, but don't really need or want a Linux desktop as my main interface. I do need a Linux-y command line terminal.

Pricing is in Canadian Dollars $CAD before taxes or shipping, unless I refer to $USD specifically. I'm sure there are all sorts of specials and sales -- shill me your deals!

## Mac Laptop

The default case for me is that I get a Macbook Air. The 11" Air with an i7 processor is still my most favourite laptop ever. It's still in use by my mom after 7 years.

The 13" Macbook Air with 16GB of RAM is either ~$1700CAD with 128GB hard drive or ~$1900 with 256GB hard drive. To align it with other specs below, i5/8GB/128GB or 256GB is what that would look like.

I know I can be productive, have access to one-of-a-kind apps like Keynote, and in general have a very usable machine. I can _also_ dual-boot Windows (would need the larger hard drive for sure). No need to dual-boot into Linux, dev tools work great from MacOS command line.

I don't need the power / expense of a Macbook Pro (never mind keyboards or touchbars). 

Apple closing down what can be installed on MacOS and generally lower quality hardware is one of the reasons to continue exploring. What's my Mac exit plan?

## Chromebook

If I'm going to get a Chromebook, it should be inexpensive. That means -- I see no reason to pay as much as I would for a Macbook Air to get something with less app and software support. Yes, I'm looking at you, Google Pixelbook. Even the "cheaper" Go is $850 to $1800CAD, depending on specs. My target recommendation is $500 - $800CAD to still get enough power and build quality.

I used what was [Wirecutter's Chromebook recommendation](https://thewirecutter.com/reviews/best-chromebook/) for, I think, 3 years? -- the [ASUS Flip C302CA](https://www.asus.com/ca-en/Laptops/ASUS-Chromebook-Flip-C302CA/), an 12.5" laptop. I think I paid around $400CAD for the m3 /4GB RAM / 32GB storage. There are now upgraded versions including one with an Intel m7 processor/8GB RAM/64GB storage that looks to be priced around $800CAD. The version I had with 4GB RAM was a little too minimal for lots of browser tabs (the [Great Suspender Extension](https://chrome.google.com/webstore/detail/the-great-suspender/klbibkeccnjlkjkiokjodocebajanakg?hl=en) helps with this). Using ChromeOS' native command line is efficient, but you will have to be in developer mode to use it. [Chromebrew](https://skycocker.github.io/chromebrew/) is a pretty great experience for having various popular programming languages and command line tools just work. If something is **not** in Chromebrew, there aren't that many others using this option, so you're deep in the bowels of Make files if you can get things working at all.

I upgraded to an [ASUS Flip C434TA](https://www.asus.com/ca-en/Laptops/ASUS-Chromebook-Flip-C434TA/) from the C302, it was ~$800CAD back in October 2019, and I've seen some prices around ~$650CAD recently. The reasons to upgrade were 8GB RAM / faster m3 processor / a USB-A port, and (main reason) because it shipped with an upgraded kernel with support for containers (aka Linux apps aka [Crostini](https://www.reddit.com/r/Crostini/)). 

This means a full container (or multiple containers!) running whatever flavour of Linux you want, visually integrated into the same GUI as ChromeOS. When I got it, the default container was an old version of Debian. [I replaced it with Ubuntu 18](/62009/) and things have been pretty good, other than the "standard" Linux yak shaving of various apps having different packaging needs, font / emoji support for Discord, and some quirks about how apps run in containerized networking.

Fun fact: if you want to run Linux-y-things -- and apps that run in the browser -- an Intel processor is going to have best performance. Android apps tend to be optimized for ARM processors. Aside from a few things here and there, the web app version of services have ended up working better for me than the Android app version.

I've never really used the "flip" aspect of these models btw -- where it's a hinge that you can fully "flip" the machine into tablet mode. ChromeOS and Android app support for "tablet" mode is pretty mediocre, and I haven't found any must have tablet mode apps.

My experience with the ASUS C434 has been just as good as with the C302 previously. People had been waiting for a C302 successor for some time. Apparently others have been having issues with that model, and the **new** recommended successor is the [ASUS Flip C436FA](https://www.asus.com/ca-en/2-in-1-PCs/ASUS-Chromebook-Flip-C436FA/). It doesn't appear to be fully available for sale yet, and is more higher end, with costs looking like $1000CAD.

My full-time usage of a Chromebook that started as an experiment has essentially been proven. I can be productive on a laptop with good build quality and do everything I need to do, especially with the addition of Linux container support (that is technically still in beta). It's about half to a third the price of a brand new Macbook Air.

[Chrome Apps are being killed March 2020](https://www.theverge.com/2020/1/15/21067907/google-chrome-apps-end-support-lune-windows-macos-linux), and Android apps work but are mediocre at best -- so essentially you've got a solid, secure, Linux-based operating system, plus a browser environment that just works.

There are many other Chromebooks. Be extremely suspicious of low prices and the performance on non-Intel processors. I don't know how I feel about [Wirecutter's current HP Chromebook top pick](https://thewirecutter.com/reviews/best-chromebook/) -- I don't have fond memories of HP. ASUS seems to continue making these very solid all metal bodies that I can recommend.

## Windows Laptop

At work, we've got the beginnings of Windows support, but don't have anyone on the team using it full time. After my Chromebook and iPad experiments, should I commit to running a Windows 10 plus [Windows Subsystem for Linux (WSL)](https://docs.microsoft.com/en-us/windows/wsl/about)?

I don't think running Windows is a good idea on low end hardware, so I'm arbitrarily picking $1500CAD as the target pricing range I'm willing to spend.

I've dreaded doing the research on this because Wirecutter doesn't have a "developer friendly laptop that doesn't need to do gaming but isn't underpowered" category. Their top level best laptops page says: ["For most people: The best ultrabook"](https://thewirecutter.com/reviews/best-laptops/#for-most-people-the-best-ultrabook) is probably the closest, and links to an $1100USD Dell as the top pick.

The Dell XPS 13 is around $1600CAD for a very solid i7/16GB RAM/512GB hard drive. The one with Ubuntu installed seems to be called the "New XPS 13"](https://www.dell.com/en-ca/shop/dell-laptops/new-xps-13-laptop/spd/xps-13-7390-laptop/nxps137390i_h6096ce). The [Windows Dell XPS 13 with i7/8GB/256GB](https://www.dell.com/en-ca/shop/dell-laptops/xps-13-laptop/spd/xps-13-7390-laptop/nxps137390i_h704b1e) is around $1500CAD, assuming I want Windows 10 Pro for +$100 (and +$50 for a 512GB hard drive seems a no brainer).

Digging into [Wirecutter's Best Windows Ultrabook recommendations](https://thewirecutter.com/reviews/the-best-windows-ultrabook/), the Budget Pick is an [ASUS ZenBook 13 UX333FA](https://www.asus.com/ca-en/Laptops/ASUS-ZenBook-13-UX333FA/). The version with i5/8GB/256GB looks to be about $1000CAD.

Given my good experience with build quality with my ASUS Chromebooks, I looked at some more ASUS options. The [ASUS ZenBook 13 UX334FL](https://www.asus.com/Laptops/ASUS-ZenBook-13-UX334FL/) has i7/16GB/512GB and comes with two notable features. You can optionally choose a version with a dedicated mobile graphics card, the GeForce MX250. The second is a gimmick, but I kind of love it: the "ScreenPad", where the touchpad is also a screen. Look at this glorious rendering of flipping apps on your touchpad!

![ASUS Zenbook with Screenpad Rendering](/images/2020-02-25/asus-zenbook-screenpad.jpg)

It looks to be about $1600CAD for this version.

I've heard good things about Surface Books, but they seem expensive: start at around $1700CAD for i5/8GB/256GB, and are $2700CAD for i7/16GB/512GB (ouch!). The Surface Pros (more portable, less power) look good as well, and are a little bit cheaper -- but I think also with less power.

The [Razer 13" Stealth Blade](https://www.razer.com/ca-en/gaming-laptops/razer-blade-stealth/shop) with i7/8GB/256GB starts at $1400CAD. With i7/16GB/256GB and a GeForce MX150 it's listed at ~$1600CAD -- in Quartz Pink, which I would totally rock! _(and all those prices seem to be listed with ~$300 - $500CAD discounts at the moment)_

I think that's all the Windows laptops I want to keep digging through :)

## Conclusion

I think I'm going to run the Windows laptop experiment. And the Zenbook with ScreenPad seems to be a good price/performance/build quality/novelty trade off.

Wish me luck, send recommendations on your favourite Windows apps!

I still want to run other experiments like [connecting a RPi4 to my iPad Pro over USB-C](https://www.raspberrypi.org/blog/connect-your-raspberry-pi-4-to-an-ipad-pro/). And [Intel NUCs](https://www.intel.ca/content/www/ca/en/products/boards-kits/nuc.html) seem cool.