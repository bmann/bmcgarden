--- 
layout: post
title: Stylesheet Wrangling
created: 1060458720
categories: 
- Web Development
- BMC
---
OK. Last post to talk about the changes I've made to the site. Everything should be working and look decent on all browsers, except for IE5/Mac.

The final big change was the addition of JavaScript stylesheet-switchers in the upper right hand corner. It uses cookies to store your preferences. The JavaScript code and description of the method is from an <a href="http://www.alistapart.com/stories/alternate/">ALA article</a>.
<!--break-->
<strong>Default</strong> is Palatino/Georgia, <strong>lucida</strong> is Lucida Grande/Trebuchet MS, and <strong>rightnav</strong> is with blocks on the right but same look as the default.

The beauty of it is that the alternate stylesheets are so easy. Here's the rightnav stylesheet:
<code>@import url("base.css");

#blocks {
  position: absolute;
  right: 10px;
  width: 175px;
  padding-right: 1px;
}

#main {
        margin-left: 0px;
	margin-right: 185px;
}</code>
So, the base stylesheet contains the main look and feel, and then anything can be overridden in the alternate sheet. For the style switching, I could have a completely different look just by not importing the base stylesheet -- this is likely what I will do for IE5/Mac, so that my parents can actually read this thing.
