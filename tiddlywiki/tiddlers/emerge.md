---
title: "Using emerge to install packages on ChromeOS"
---
_[[ChromeOS]] is based on Gentoo, which uses the emerge package manager_

Yes, you run the dev_install script. Note: this _will_ delete everything under ```/usr/local``` ([bug where people are screaming](https://bugs.chromium.org/p/chromium/issues/detail?id=255485)).

Also currently buggy: [dev_install fails to install emerge](https://bugs.chromium.org/p/chromium/issues/detail?id=842039#c9)

> Boot the machine and go to a shell (login and go to crosh (ctrl+alt+t) or change to virtual terminal 2 (CTRL+ALT+F2))
>Change to root and initialize the login environment variables:
>```$ sudo su -```
>
> Execute the dev_install script. This script does everything automatically and asks you if you want to install chromeos-dev (it will take a while if you choose to):
>
>```# dev_install [--reinstall if done before]```
>
>Use emerge as usual. For example, to get qemacs install:
>
>```# emerge qemacs```
>
>Done! Now you can emerge any package in chromeos-dev or chromeos-test
>
> https://www.chromium.org/chromium-os/how-tos-and-troubleshooting/install-software-on-base-images:

Also useful:
* Gentoo Cheat Sheet https://wiki.gentoo.org/wiki/Gentoo_Cheat_Sheet