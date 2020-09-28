--- 
layout: post
title: Feedback for Doc Searls' IT Garage
created: 1082746807
categories: 
- Drupal
- Drupal
- Drupal
---
Doc Searls has started using Drupal, so I headed over to <a href="http://garage.docsearls.com">check it out</a>. Because, after all, I need to <a href="http://www.bmannconsulting.com/node/view/1097">track Drupal converts</a>.

I actually started typing this up in a comment entry box in response to <a href="http://garage.docsearls.com/?q=node/view/12">Doc's To-Do list</a>, but it quickly got really long, and probably has some valuable info in it for other people as well. So the following was written addressed directly to Doc:
<!--break-->
Writers: just invite them, and they can start posting. Either to their blog (which can be promoted to the front page, if you so desire), to the story node type, and/or by default placed into a moderation queue to decide whether stories get promoted. You can, of course, have different member roles (perhaps a "Contributor" role) with a different set of permissions.

Separate feeds are available for each blog. I would recommend the <a href="http://www.drupal.org/project/syndicate">syndicate module</a> for more options -- as well as displaying the "front page" feed, it has easy display of URLs to feeds for individual blogs (mine would be <a href="http://garage.docsearls.com/?q=blog/feed/97">here on the garage site</a>). And of course, you can subscribe to a separate feed per topic as well.

The "blogroll" is handled automatically within Drupal. Turn on the aggregator module, add as many feeds as you want. You can check out an example source list (a.k.a. blogroll) at <a href="http://www.urbanvancouver.com/news/source-list">Urban Vancouver</a> (there is a link to an auto-generated OPML file at the very bottom as well). You can also display these on the front page in a block.

Better design: <a href="http://www.streamlinewebco.com">StreamLine</a> does Drupal consulting. Give us a shout if you need some help (we can assist with converting designs with templates and know the ins and outs of Drupal).

Permalist of offsite links: perhaps you mean something like the <a href="http://www.drupal.org/project/weblink">weblinks module</a>?

Featured links: could be handled by just grabbing their RSS feeds, tagging them with a special "featured" keyword, then creating a "Featured" bundle. This bundle can then be set to display on the front page (or wherever -- block display is handled by a PCRE). All available within the aggregator module.

Lastly, it would be great if you turned on the "drupal" module, which will allow login from other Drupal sites (federated identity -- I don't want to have yet-another-account, but had to create one to post this comment). It's TypeKey without the centralization, since the authentication goes back to your "home" site, which might be an account on another group/community site, or it might be your own personal site.

And, of course, clean URLs. This just means uncommenting some lines in your .htaccess file and selecting clean urls from the main <a href="http://garage.docsearls.com/?q=admin/system">admin page</a>.

(Moments later…)

OK, OK, I thought of more things. Turning on avatars (a.k.a. user pictures) and then turning on avatar display in comments is a neat way to have discussions, since everyone's face or icon shows up. This can also be turned on for main posts as well, which is a nice way to (easily, visually) distinguish who is posting.

Also, the best way to keep up to date with what is going on on a Drupal site is <a href="http://garage.docsearls.com/?q=tracker">the tracker</a>. And you can see recent posts by <a href="http://garage.docsearls.com/?q=tracker/97">user</a> as well (might have to update the code -- latest version of Drupal shows comments as well, I believe).
