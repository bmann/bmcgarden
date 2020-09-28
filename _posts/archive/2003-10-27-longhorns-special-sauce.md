--- 
layout: post
title: Longhorn's Special Sauce
created: 1067306640
categories: 
- Microsoft
---
So the <a href="http://msdn.microsoft.com/events/pdc/">Microsoft PDC</a> is now in full swing. Reports are starting to filter back from the mothership, like <a href="http://blogs.it/0100198/2003/10/27.html#a1909">this one from Marc Canter</a>. He seems quite impressed, especially given some <a href="http://radio.weblogs.com/0001011/2003/10/26.html#a5170">earlier posts</a>.

There are lots of technical bits flying around all over the place that will probably be better summarized a week or so from now. I see <acronym title="XML application markup language">XAML</acronym> as the special sauce, the most important thing that was announced. What is XAML? It's <em>XML Application Markup Language</em>. Or at least, that's what it is now -- <a href="http://www.google.com/search?q=XAML&ie=UTF-8&oe=UTF-8">according to Google</a>, it used to be <a href="http://xml.coverpages.org/xaml.html">Transactional Authority Markup Language</a>. But on to Microsoft's XAML: it is XML markup that can define everything from UI to applications.

So, now that this has been revealed, everyone has to ask themselves: what does this mean for [insert-favourite-operating-system]? Read on...
<!--break-->
First of all, it's not like Microsoft has come out with a completely new animal. This is much like <a href="http://www.mozilla.org/projects/xul/" title="XML User Interface Language">Mozilla's XUL</a> -- a markup language that goes beyond HTML to create applications indistinguishable from desktop applications.

Much like Windows-only code in IE (and access to the IE dlls running on Windows), XAML will enable many types of rich media apps...on a Windows desktop. Goodbye, Flash. So now what? What about other platforms? The way I see it, there are a couple of options.

<strong>Write XAML-compatible engines:</strong> basically, applications/extensions/plug-ins/whatever that enable non-Microsoft clients to run XAML code. I imagine that a lot of XAML will have hooks directly into Longhorn, so it may not be possible to duplicate a lot of the functionality. But, if Microsoft has to add XAML support to <a href="http://www.myelin.co.nz/post/2003/10/28/#200310281">older versions of Windows</a>, it might still be feasible.

<strong>Develop a compelling alternative platform:</strong> I really do think this <strong>is</strong> XUL -- albeit with 2 years of development behind it. There may be different types of "XUL containers" (that is, apps that can run/display/interact with XUL code on the desktop), but the most likely candidate is the browser on non-MS platforms...especially since Mozilla can do this today.

Actually, I think both options will go ahead. Just like .NET has <a href="http://www.go-mono.com/">Mono</a> (although neither seem to have gotten very far), there will be a rush to reverse-engineer XAML on alternate platforms. At the same time, XUL development will get a kick in the pants.

I think, perhaps, that someone knew. How else to explain that the <a href="http://weblogs.mozillazine.org/hyatt/archives/2003_10.html#004249">newest version of Safari supports XUL</a>? (just a tiny part, but it's a start). So I think we see that Apple has firmly cast it's vote into support XUL as it's answer. This may very well go back into the Linux/open source world with WebCore (based off of <a href="http://dot.kde.org/1041971213/">Konqueror's KHTML library</a>).

Time to start learning XUL...

Note to Colin: I bet your market value as a coder just shot up at least 50%! (Colin did extensive XUL development at <a href="http://www.oeone.com/">OEOne</a> (now <a href="http://www.bmannconsulting.com/node/view/579">Axentra</a>)).
