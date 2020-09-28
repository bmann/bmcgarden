--- 
layout: post
title: Being involved in the issue queue as a normal part of development
created: 1280600997
categories: 
- Drupal
tags:
- drush_make
- Development Seed
- patch
- open source
---
<p><a href="http://www.flickr.com/photos/drumm/1427977653/"><img alt="" class="imagecache-thumb lightbox" src="/sites/bmannconsulting.com/files/imagecache/thumb/postimages/1427977653_fee7de8eca_d.jpg" style="margin-left: 10px; margin-right: 10px; margin-top: 10px; margin-bottom: 10px; float: right; " title=""></a></p>
<blockquote>Patches that we write for drupal.org modules are submitted to the issue queue, and we refer to the patch’s location on drupal.org in the make file. This has made us much better contributors to other people projects as it makes being involved in the issue queue a normal part of development, and it encourages us to only patch contrib modules where it’s likely that the patch will be accepted. When a patch gets a review, we make changes, upload a newer version of the patch to drupal.org, and update our make file.</blockquote>
<p>via <a href="http://developmentseed.org/blog/2010/jul/27/drush-make-files-production-drupal-sites">developmentseed.org</a></p>
<p>This is actually a quote from <a href="http://developmentseed.org/blog/2010/jul/27/drush-make-files-production-drupal-sites#comment-5288">Jeff in the comments on the article Drush Make Files for Production Drupal sites</a>, but I thought it was definitely worth highlighting on its own.</p>
<p>In this particular case, using make files actually codifies the decision to integrate closely with contrib modules and actively improve them / add features as needed for a particular project.</p>
<p>I've followed this practice for years, albeit without make files. Patches go in a "patches" directory in version control, with the patch file named with both the name of the module and the node number of the issue on Drupal.org.</p>
<p>An additional process is that if a patch is needed, you run it in the issue queue on Drupal.org, but you also have an internal ticket that links to that issue. You don't close the issue until the patch has been accepted into the mainline of the module. Then you can remove the patch, update the version of the module you're using, and your clients' website is one step closer to easier long term maintenance and updates.</p>
<p>And yes, being involved in the issue queue SHOULD be a normal part of developing Drupal websites.</p>
