--- 
layout: post
title: Google Friend Connect paves over your site and plonks down a social network
created: 1229412591
categories: 
- Web 2.0
tags:
- distributed social networking
- Farmstead Wines
- Google
- Google Friend Connect
- Jim Pick
- OpenSocial
- Redanyway
- Twitter
- Social Media
---
<p>Since my <a href="http://www.bmannconsulting.com/archive/redanyway-a-distributed-social-network/">post on Redanyway</a>, I've gone a few steps further into experimenting with <a href="http://www.google.com/friendconnect/">Google Friend Connect</a>.</p>

<p>Basically, it allows you to drop in a members system / social network onto any site. It doesn't need to be a CMS or a dynamic system at all, since it consists of just some Javascript that gets inserted wherever you like. You create a new network / site at the Friend Connect home, and then go on to upload a couple of files to your server. Select some widget options, copy and paste code, and you've got a place where visitors to your site can join your site's network.</p>

<p>Now, as opposed to creating yet-another-profile, visitors use their (presumably existing) Google Account to login. Google Accounts have Profiles attached to them (since about December 2007, although it's only recently that they are being talked about more). Here's my <a href="http://www.google.com/s2/profiles/106678119088828437419">Google Profile</a>.</p>

<p>There aren't really any built in &quot;friends&quot; in your everyday Google Account / Profile (in fact, in Google Reader it's really hard -- I enjoy <a href="http://www.brendonwilson.com/blog/2008/06/06/google-reader-anti-social-software/">Brendon Wilson's rant on this</a>), so you can also activate several other networks to automatically connect with &quot;friends&quot; from those systems. Twitter and Plaxo are two that I experimented with. Orkut is also supported ... but when was the last time you signed into Orkut?</p>

<p>Twitter does that oh-so-lovable enter your username and password trick that leaves me feeling more than a bit queasy, but since I have a good size network, it seems pretty useful. You can then post to Twitter from within the widget to invite other people to join the network you've just entered. Plaxo does the better looking remote authentication and works just fine ... except I don't really use Plaxo all that much anymore.</p>

<p>OK, so now you're a &quot;member&quot; of a local &quot;network&quot;! What next? Well, on to the world of &quot;Social Gadgets&quot;. There are ratings and a comment wall, and also support for OpenSocial apps. The OpenSocial apps are, I guess, the interesting part of this in the future, sort of allowing bridging of different data with mashups unique to the members on your own site. Except there's not much there today. Comments and ratings are fairly uninteresting when dynamic sites powered by Drupal or WordPress either do these things out of the box or can add them easily with a couple of plugins.</p>

<p>But....I'm not completely down on this system. In fact, I've been talking to <a href="http://farmsteadwines.com">Anthony of Farmstead Wines</a>, who is a heavy Twitter user, about adding Friend Connect to his website. He can use his large Twitter network to build a social network around his website. It doesn't do a lot of interesting things *today* ... but you can already see how member profiles on Google Maps and other mashups will be trivial to implement in the future. Adding full network functionality to his website would cost a lot of money and time if needing to be &quot;built in&quot; directly, whereas the Friend Connect route lets Anthony build his network today, centered around the permalink of his own website (as opposed to some other system like ye old Ning).</p>

<p>I've included a Google Friend Connect network widget and wall widget after the jump. <a href="http://jimpick.com">Jim Pick</a> has also created one for the <a href="http://vanbase.jpick.user.dev.freebaseapps.com/">Vancouver Freebase</a>.</p>

<p>Will you be adding Google Friend Connect to your site? Do you find it useful? Where is this heading?</p>

<!-- Include the Google Friend Connect javascript library. --> <script type="text/javascript" src="http://www.google.com/friendconnect/script/friendconnect.js"></script>  <!-- Define the div tag where the gadget will be inserted. -->
<div id="div-1229409770016" style="border: 1px solid rgb(204, 204, 204); width: 400px;">&nbsp;</div>
<!-- Render the gadget into a div. --> <script type="text/javascript">
var skin = {};
skin['HEIGHT'] = '400';
skin['BORDER_COLOR'] = '#cccccc';
skin['ENDCAP_BG_COLOR'] = '#e0ecff';
skin['ENDCAP_TEXT_COLOR'] = '#333333';
skin['ENDCAP_LINK_COLOR'] = '#0000cc';
skin['ALTERNATE_BG_COLOR'] = '#ffffff';
skin['CONTENT_BG_COLOR'] = '#ffffff';
skin['CONTENT_LINK_COLOR'] = '#0000cc';
skin['CONTENT_TEXT_COLOR'] = '#333333';
skin['CONTENT_SECONDARY_LINK_COLOR'] = '#7777cc';
skin['CONTENT_SECONDARY_TEXT_COLOR'] = '#666666';
skin['CONTENT_HEADLINE_COLOR'] = '#333333';
google.friendconnect.container.setParentUrl('/' /* location of rpc_relay.html and canvas.html */);
google.friendconnect.container.renderMembersGadget(
 { id: 'div-1229409770016',
   site: '16140604763994025116'},
  skin);
</script>
<p>Below is the Google &quot;Wall Gadget&quot; -- it lets you post comments and post YouTube links. The scope of this wall is the &quot;entire site&quot; -- you can make one of these that apply to a particular page or a unique id.</p>
<!-- Include the Google Friend Connect javascript library. --> <script type="text/javascript" src="http://www.google.com/friendconnect/script/friendconnect.js"></script>  <!-- Define the div tag where the gadget will be inserted. -->
<div id="div-1229410260056" style="border: 1px solid rgb(204, 204, 204); width: 400px;">&nbsp;</div>
<!-- Render the gadget into a div. --> <script type="text/javascript">
var skin = {};
skin['BORDER_COLOR'] = '#cccccc';
skin['ENDCAP_BG_COLOR'] = '#e0ecff';
skin['ENDCAP_TEXT_COLOR'] = '#333333';
skin['ENDCAP_LINK_COLOR'] = '#0000cc';
skin['ALTERNATE_BG_COLOR'] = '#ffffff';
skin['CONTENT_BG_COLOR'] = '#ffffff';
skin['CONTENT_LINK_COLOR'] = '#0000cc';
skin['CONTENT_TEXT_COLOR'] = '#333333';
skin['CONTENT_SECONDARY_LINK_COLOR'] = '#7777cc';
skin['CONTENT_SECONDARY_TEXT_COLOR'] = '#666666';
skin['CONTENT_HEADLINE_COLOR'] = '#333333';
skin['DEFAULT_COMMENT_TEXT'] = '- add your comment here -';
skin['HEADER_TEXT'] = 'Comments';
skin['POSTS_PER_PAGE'] = '10';
google.friendconnect.container.setParentUrl('/' /* location of rpc_relay.html and canvas.html */);
google.friendconnect.container.renderWallGadget(
 { id: 'div-1229410260056',
   site: '16140604763994025116',
   'view-params':{"scope":"SITE","features":"video,comment"}
},
  skin);
</script>

<p>So far, I continue to be underwhelmed. Come on Google, ride on top of OpenID, and plug this directly into a site's existing user account system...</p>

<p><strong>Update:</strong> <a href="http://jimpick.com">Jim Pick</a> left a comment that went so far as <a href="http://blip.tv/file/1583359/">including a screencast showing OpenID support in Google Friend Connect</a>. So, my bad, Google Friend Connect <strong>does</strong> support OpenID directly. More correctly what I meant with my closing commentary was that, rather than logging into Google's infrastructure, that this should be tied into my sites existing account system. Which already supports OpenID.</p>
