---
title: BlinkShell
---

Command line terminal shell for [[iOS]] and [[iPadOS]]. Optimized for using with [[Mosh]].

* website https://blink.sh/
* github https://github.com/blinksh/blink
* twitter https://twitter.com/blinkshell
* discord https://discord.gg/ZTtMfvK

---

Curtis McHale: [Downloading files on a server with Blink Shell on iOS](https://curtismchale.ca/2019/09/23/downloading-files-on-a-server-with-blink-shell-on-ios)

> The scp implimentation in Blink doesn't handle recursive transfers, we need to create a single file to transfer.

> Before you can use scp in Blink to transfer your file you need to log in to your server using ssh2. Evidently regular ssh in Blink loads an esdsa key which scp doesn't recognize. To get the rsa key loaded you need to use ssh2 which scp does recognize.

So, run `ssh2 YOURHOST` first, accept the server, and then you can `scp` to that host like this:

```scp YOURHOST:/path/to/file```

This will download the file and put it in your (local) Blink folder, accessible through the Files app on iOS.