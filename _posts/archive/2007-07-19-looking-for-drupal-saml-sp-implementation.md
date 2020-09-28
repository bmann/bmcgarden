--- 
layout: post
title: Looking for Drupal SAML SP implementation
created: 1184884736
categories: 
- identity
- SAML
- IdP
- OpenID
- Google Apps
- Drupal
---
<p>At some point I got a ping from someone that was working on a SAML implementation for Drupal. Unfortunately, that was a year ago or more, and trawling my email doesn't seem to surface anything.</p>

<p>So, anyone out there in blog land working on a SAML *SP* (aka client) implementation for Drupal? I have some folks that would like to test interop. Please <a href="/contact">contact me</a> if you've got something.</p>

<p>Related to this is the <a href="http://drupal.org/project/googleauth">Google Apps Authentication module</a>, which lets you use your Drupal database as an authentication source for Google Apps -- the for pay, Enterprise or Education edition. This is a SAML v2.0 IdP implementation as far as I know...</p>

<p>And yes, I'm still a huge OpenID fan. But combining the two standards is even better, since theoretically you could create new Drupal accounts via OpenID, and the Drupal accounts in turn would serve as auth for Google Apps. AKA how to use OpenID with Google :P</p>
