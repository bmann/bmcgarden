--- 
layout: post
title: Enabling Anonymous FTP
created: 1040517000
categories:
- How To
tags:
- OS X
- FTP
- Mac


---
There are two versions of this. One is valid only for pre-10.2 systems, and there is actually no complete solution yet for 10.2.x systems.

First, a little background. FTP stands for "File Transfer Protocol". As opposed to HTTP (Hyper-Text Transfer Protocol), FTP is optimized for transmitting files. Better FTP servers and clients have support for things like resumable downloads, a key factor if you're downloading very large files and/or have a slow or unstable Internet connection.

Through the Sharing panel in System Preferences, you can enable/disable FTP access to your system. By default, Mac OS X does not allow "anonymous" FTP. That is, every user who connects to your system using FTP must sign in with a user name and password. Anonymous FTP allows anyone to log on to your system, although generally with very restrictive permissions as to what they can do.

There are two solutions to allowing people without accounts on your system. One is to create a regular user account that is used only to offer FTP access, and distribute the user name and password. This has the drawback of being a fairly high security risk, since this is a fully privileged account on the system.

The other solution is to enable anonymous FTP, which is what (hopefully) this set of instructions will help you do. Anonymous FTP has its own set of security problems, but careful use of permissions and a <code>chroot</code> environment can minimize this.
