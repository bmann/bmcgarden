--- 
layout: post
title: Instructions for 10.2.x (Jaguar)
created: 1043343840
categories:
- Mac
- How To
- OS X
- FTP

---
Sorry folks -- I wish I had a good answer here, but I've spent a couple of hours fiddling with trying to get this working, with no success so far.

There are essentially two workarounds:
<ol>
<li><strong>Create a user account to be used only for FTP</strong><br />
Need to lock down account so it can't see the rest of the system, can't logon to the command line, etc.</li>
<li><strong>Use a different FTP server</strong><br />
This means installing a separate FTP server to be used for anonymous FTP. It would have its own permissions system, and would have to run on a custom port (unless you disabled Apple's built-in FTP, which is already using the standard FTP port).</li>
</ol>
