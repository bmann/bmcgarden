--- 
layout: post
title: "ollicle: text 2 HTML without the lock down"
created: 1080504248
categories: 
- Web Development
- Drupal
- Personal Publishing
- Drupal
- Drupal
- CMS
---
<blockquote>
Jay Allen points, in his post <a href="http://www.jayallen.org/journey/2004/03/the_cms_and_inline_html">The CMS and inline HTML</a>, to an issue which I have been recently giving some thought as I consider switching between <a href="http://www.bradchoate.com/mt-plugins/textile">Textile</a> to <a href="http://daringfireball.net/projects/markdown/">Markdown</a>.
<cite><a href="http://www.ollicle.com/2004/03/28/text_2_html_without_the_lock_down.html">ollicle: text 2 HTML without the lock down</cite>
</blockquote>

<p>The referenced problem being that if you use a special syntax in a content management system, you suffer from a form of lock-in.</p>

<blockquote>
Readability of the entry would only be hampered in the rare event of revisiting a entry for editing.
</blockquote>

<p>Drupal handles this through the use of filters. Your plain text or plain text plus markup is what is stored in the database, without being permanently transformed. Of course, the issue still remains that you're locked into a particular syntax.</p>

<p>I've actually gotten in the habit of typing in (X)HTML directly. It's certainly not ideal, and absolutely no good for end users, but something like <a href="http://www.drupal.org/project/htmltidy">the HTML Tidy module</a> to check/correct your syntax would be good. There is also <a href="http://www.drupal.org/project/htmlarea">HTMLArea</a>, a WYSIWYG component for Mozilla browsers.</p>
