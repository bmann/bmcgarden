--- 
layout: post
title: "Drupal out of the box: let's make a community"
created: 1244840104
categories: 
- Community in a Box
- Drupal 7
- drupaloob
- install profiles
- OOB
- out of box
- Drupal
---
<p>First off, I need to apologize to @webchick for being called away from the Drupal BoF at <a href="http://openwebvancouver.ca">Open Web Vancouver</a> last night. It was great to have her here to do a run through with @chx1975 of where we're at with Drupal 7.  I was around just long enough to once again raise the issue of what the default install profile will do.</p>
<p>We've come quite far in major core improvements, but we don't have a story for what Drupal is when you do a default install.  What should Drupal do &quot;out of the box&quot;?</p>
<p>There is a placeholder issue for this now: <a href="http://drupal.org/node/483987">#483987 Decide on direction for default install profile</a>.  As I've seen the UX process continue, I still see us focusing on building and constructing. The changes there have been excellent, but I think we're missing an opportunity to have a truly great out of the box experience. My codename for this is &quot;drupaloob&quot;.</p>
<p>The first step is deciding the story for this. WordPress is a blog. We are not a blog. We are a multi user system. Can we turn on a minimal OOB experience that showcases some of our multi user and other strengths? In the words of President Obama, &quot;Yes We Can!&quot;</p>
<p>My personal opinion and outline for this is that we should ship with a &quot;Community in a Box&quot;. I've documented it on <a title="Default install Community in a Box" href="http://groups.drupal.org/node/21013">groups.drupal.org</a>. Regardless of the details of comments on or off, promoted by default, and other finer points, here is my user story for this Community in a Box:</p>
<blockquote> A community site with front page articles, a community blogging section, discussion forums, and shared image galleries.<br />
</blockquote><blockquote>Anyone is welcome to sign up for an account and participate in the forums. After some time in the forums, users are invited to become contributors, and can post blog posts and photos, as well as submit unpublished articles.<br />
</blockquote><blockquote>The blogging functionality is a community multi user blog. It is not meant as one users blog, but rather a large community that can post quick thoughts responding to each other and sharing their ideas. (Note: this is in here because people get confused about &quot;blog&quot; functionality -- this is meant to highlight that having a community blog is not the same as a single user blog, so don't expect to be able to change titles and designs etc. -- your blog posts are in a shared, community space)<br />
</blockquote><blockquote>Editors are around and police the forums, as well as reviewing and publishing articles and other material for the front page.<br />
</blockquote><blockquote>The photo galleries are shared galleries: like the forum and the community blogs, users upload them to share, rather than in their own space. There are weekly suggestions for new gallery categories, and users can also tag photos with whatever they like to mix and match how the photos are grouped. </blockquote>
<p>While I'm piling wishes on top of dreams, I'd even like to use the wizard that has been in core since Drupal 6 to make several parts of this OOB experience optional. That is, right at the beginning, users would have two options.</p>
<p>One would be to do an &quot;express install&quot; that would install everything with the defaults as I've outlined above.</p>
<p>The second would be to engage the wizard and answer a series of questions and options:</p>
<p>Do you want forums? yes/no<br />
Do you want a community blog for contributors? yes/no<br />
Do you want a community photo gallery? yes/no etc.</p>
<p>What do you think? What would you want people to experience when they first install Drupal 7?  <a href="http://groups.drupal.org/node/21013">Edit the wiki</a>, leave comments, or create some patches against <a href="http://drupal.org/project/issues/search/drupal?issue_tags=default.profile">default.profile</a>.</p>
<!--break-->
