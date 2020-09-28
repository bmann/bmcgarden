---
title: 'So, if all goes well, I am posting this from iA Writer'
date: 2020-05-14T13:39:19.233-07:00
category:
- Blog
tag:
- micropub
- iAWriter
- IndieKit
- IndieAuth
---
So, if all goes well, I am posting this from @iAWriter. I saw the news from [Manton’s post that this works with @MicroDotBlog](https://www.manton.org/2020/05/13/ia-writer-adds.html). Micropub as a posting API is picking up!
<!-- more -->
It initially didn't work:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">this is great. Saw the news from 
@mantonsblog that you've got Micropublish support.<br />
<br />
Tried it with my custom endpoint, and you're not requesting "create" or "media" scopes https://indieweb.org/scope</p>&mdash; Boris Mann (@bmann) <a href="https://twitter.com/bmann/status/1260639598419550208">May 13, 2020</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Reading further into the IndieAuth spec, scope is not required. If you have a token, then "create" scope is the default minimal scope.

I had to [patch IndieKit](https://github.com/paulrobertlloyd/indiekit/issues/222) (which is the micropub server I run to publish here) to get this working. But it did work!

This posts full length Article (aka Blog) posts by default, not microblog sized posts, which probably makes sense. Worst case, I can come in and remove the title and add a "social" tag and it would turn into a social post.

Finally, this isn't just about Micropub, but rather the success of [IndieAuth](https://indieauth.com/). We had @aaronpk come on to our [Fission Thursday video chat and we talked about this](https://talk.fission.codes/t/indieauth-indielogin-and-all-the-indiewebs-with-aaron-parecki/629).

I can run my own site with my own identity, and a third-party app like iAWriter can ship support for standards, and all of a sudden I have my choice of apps, without having to give up control of my data or my identity. Yay!
