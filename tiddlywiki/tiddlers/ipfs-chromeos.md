---
title: "Running IPFS on a Chromebook"
---
_Running [[IPFS]] on ChromeOS like this is not recommended -- use the built in [[ChromeOS Linux Support]]._

I'm going to assume you already have your [[Chromebook]] in developer mode.

## Install IPFS

Available via [[Chromebrew]]:

`crew install ipfs`

Now you can get started:

`ipfs init`

To run IPFS as a daemon:

`ipfs daemon &`

## IPFS Companion Chrome Plugin
https://chrome.google.com/webstore/detail/ipfs-companion/nibjojkomfdiaoajekhjakgkdhaomnch/

Source on GitHub: https://github.com/ipfs-shipyard/ipfs-companion