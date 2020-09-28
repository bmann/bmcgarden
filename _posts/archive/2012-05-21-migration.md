---
title: Migration
---

The first post -- [[Welcome to B Mann Consulting]] -- on this site running [[Drupal]] was November 9th, [[2002]]. The next post was asking for a [[Dream CMS]]. I don't think I've found it with [Octopress](http://octopress.org), but I'm having fun learning the ins and outs.

As of May 21st, I've migrated the bulk of the BMC site to Octopress, and am hosting it directly on Amazon S3. The source Drupal site is still up and running at [Omega8.cc](http://omega8.cc), which is still my recommendation for managed Drupal hosting that is relatively low on custom code (e.g. custom theme + a couple of modules or an install profile). [Pantheon](http://www.getpantheon.com) or one of [Acquia's](http://www.acquia.com) hosting options are probably your best bet for larger scale custom Drupal web-app hosting.

<!-- more -->

I setup the Amazon S3 hosting some time ago, using [a couple of blog articles](http://links.bmannconsulting.com/how-to-install-configure-octopress-on-a-mac-and-host-your-static-website-on-amazon-s3-1) to configure an Amazon S3 bucket to serve up HTML pages directly, and to modify Octopress to include a rake command that deploys directly to S3.

Exporting the posts in Drupal to Octopress-compatible files was both difficult and easy. I fiddled around trying to get a proper local install that would work with the Jekyll / Ruby mysql gems and such. Long story short, here's what you need to do:

1. Export your Drupal database (e.g. via [Backup & Migrate module](http://drupal.org/project/backup_migrate))
2. Install mysql on your local machine - I used [Homebrew](http://mxcl.github.com/homebrew/)
3. Import your database - create a local database and import your exported one
4. Run the Jekyll Drupal migrator
```ruby -rubygems -e 'require "jekyll/migrators/drupal"; Jekyll::Drupal.process("database", "user", "password")'```

Here is the modified Jekyll drupal.rb migrator I used. I've removed the refresh / redirect related generation on nodes, and I've added pulling tags / categories from Drupal:

<!-- gist 2766017 -->

Note that this is for Drupal 6. See [walkah's write-up](http://walkah.net/blog/new-year-new-blog/) and [drupal.rb](https://github.com/walkah/walkah.net/blob/master/_import/drupal.rb) for getting this to work in Drupal 7.

You'll now have all of your posts in the `_posts` folder (in my case, over 2200 of them over 10 years!). I did all this in a "clean" Jekyll codebase, and then just copied the posts over into the Octopress install I already had running / deploying to S3.

I have lots of cleanup to do, but I've had lots of "collateral damage" over the years of moving between Drupal versions and hosts — meaning I've already left a trail of tears and broken links in my wake. I spent some time cross-posting between Posterous and my BMC Drupal site, so there is likely to be some back and forth shuffling.

I intend for this site to serve the following purposes:

* a front page that showcases / points to active content: currently, this is [my blog](http://blog.bmannconsulting.com), [link blog](http://links.bmannconsulting.com), and [recent Twitter posts](http://twitter.com/bmann)
* a long term archive of content
* special projects: I currently have a couple of pages hanging out on the blog, but this will likely be a better home

With Flickr starting to look a bit wobbly, I'm going to look at hosting images here directly as well, but that's for future exploration.

### Update July 24, 2014:

I moved off of Octopress and onto "plain" [[Jekyll]], using the [So Simple Theme](http://mmistakes.github.io/so-simple-theme/). I'm using [Dploy](http://dploy.io) connected to a [[Bitbucket]] private git repo to maintain the generated site on [[Amazon S3]].
 