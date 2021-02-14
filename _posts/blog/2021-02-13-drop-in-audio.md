---
title: Drop in Audio
date: '2021-02-13T23:34:34-07:00'
categories:
  - Commons
tags:
  - Clubhouse
  - social network
---

I finally signed up for [Clubhouse](https://www.joinclubhouse.com/), the new drop in audio based social network. Mainly, it was so that the flood of invites would stop.[^clubhouseinvite]

[^clubhouseinvite]: Yes, I have invites, yes I'm happy to invite you if you want to try it out.

But my first drop in audio experience was actually with [Soapbox](https://soapbox.social), an app built by some Berlin based friends. I had a great chat with Mike in Chicago, and a few others wandered in and we ended up talking about BBQ sauces. There's also an "audio stories" feature, where you can record messages that followers can listen to. 

Soapbox founder Dean Eigenmann says he wants it to be more like your favourite bar, rather than Clubhouse which he says feels more like attending a conference. The elitism of Clubhouse definitely is another thing that turned me off, but of course that has just made people want to get in even more.

It's great to watch this flood of interest in new social networks. Trying out new features, experimenting, meeting new people. Especially with the pandemic ongoing, it's something that many people want to feel.

I was grumpy about it at one point. I got social network fatigue in the first big wave of social networks in the early 2000s. But it is great to see people being excited about being part of new networks, and learning and trying new things.

What I _am_ grumpy about is that people aren't thinking about the same old issues:
* Whose platform is it?
* Who owns the content?
* Are you building connections and forming groups that you'll have to rebuild from scratch when you leave?

Oh, and as it turns out, the [Stanford Internet Observatory determined](https://cyber.fsi.stanford.edu/io/news/clubhouse-china) that the way data is transmitted means that information about who is talking to who is pretty easy to figure out ... among other concerns about Clubhouse's backend provider potentially even making raw audio data available to the Chinese government...

We've seen an understanding of having your own platform emerge around blogs & newsletters. As an example, [Ghost is a great open source competitor to Substack](https://ghost.org/vs/substack/).

Can we get there quickly with drop in audio? Technology wise: yes. You can even make this work in a web browser: WebRTC lets us do audio (and video) right in the browser.

Feross' [Speakeasy](https://speakeasy.co) lets anyone create rooms, and anyone who drops in is connected into a video chat with others, along with a 5 minute timer to move on to the next person.

Big Blue Button (BBB) is a platform I've been experimenting with, which is a more full featured web conference platform that competes with Zoom, and is open source. The [Meet.Coop](https://meet.coop) collective hosts BBB for you. It has rooms, starts with audio only, and each room can have an invite link. Visitors connect directly through their browser. Boom - you've got drop in audio chat rooms.

Discord servers have great multi-person voice channels, Twilio has long had programmable audio for building these types of experiences, and this [TechCrunch article from back in April 2020 covers a host of other audio first startups](https://techcrunch.com/2020/04/18/clubhouse-app-chat-rooms/).

## Social Networks Aren't About Tech

But of course, social networks aren't primarily about the technology powering them.

After trying out Soapbox ([here's my profile](https://soapbox.social/user/boris)), my friend [Claire Atkin @catthekin](https://twitter.com/catthekin) gave me a demo of what she had learned about Clubhouse so far (she was an early adopter last year). Mute when you're not talking "on stage", "flick" the mute button when you agree with the current speaker (rather than saying anything audible), the 🎉 on your profile means you're new and people will cut you some slack for the first couple of days.

The day after Claire gave me a tour, I went for a walk and decided to explore a little more on my own. I dropped in and "pinged" [Carter Rabasa @crtr0](https://twitter.com/crtr0). Carter was one of the people that had initially invited me and has been having some fun experiences.

We had a good chat about how web-based drop in audio has a real disadvantage us. native mobile app notifications drawing you back in.[^carter]

Carter pointed out that "where your friends are" really drives early network formation. This is a good point, and Clubhouse itself leans into Twitter and Instagram (and your phone's address book of contact phone numbers).

[^carter]: Plus a bunch of other topics, like pandemic & US politics being a downer, Pacific North West snow, DevRel evolution. It was definitely nice that Carter "picked up" and we could just chat for a bit and catch up.

Twitter login for web based drop in audio (or Mastodon or other existing social networks) is key for making it easy to grow your network.

So, can you "own your own drop in audio"? Yes! Just like running a newsletter or a forum, we have the tech. Building your own club takes time - and moderation and welcoming new people and so on. Consider whether your existing community could benefit from adding audio.

Will I keep using Clubhouse? Sure, I'll keep an eye on it and experiment a little, and enjoy the novelty of a new network.

In fact, join me on February 23rd, 9:30am PST / 12:30pm EST / 18:30 CET for a discussion on Decentralized Open Networks. [Find the event on Clubhouse](https://www.joinclubhouse.com/event/PvNo69XP), or register on Luma:

<br /><br />
<a href="https://lu.ma/event/evt-4hubOg6pSTUk3jS" class="luma-checkout--button" data-luma-action="checkout" data-luma-event-id="evt-4hubOg6pSTUk3jS">Sign up for Decentralized Open Networks, Feb 23rd</a>
<script id="luma-checkout" src="https://embed.lu.ma/checkout-button.js"></script>
<br />
I'll also drop a link to some BBB and Speakeasy rooms [on Twitter](https://twitter.com/bmann) to experiment with those platforms.

## Ideas & Links

Drop in Audio for Ghost Members: build a plugin for Ghost that ties into the Members system, and do public or private rooms.

[Speakeasy](https://speakeasy.co) is currently video, make an option to configure rooms to be audio-only

[Big Blue Button](https://bigbluebutton.org/) originally started as. The Greenlight add on [github.com/bigbluebutton/greenlight](https://github.com/bigbluebutton/greenlight) makes for a simpler user interface, which you can [checkout in the Meet.coop demo](https://demo.meet.coop/). It's written in Rails
soap box. Social

[Twilio](https://www.twilio.com/) is the king of programmable audio. Here's a recent [tutorial on building a Twilio Video chat app with React](https://www.twilio.com/blog/build-a-custom-video-chat-app-with-react-and-twilio-programmable-video) -- would be simple for them to make an audio chat tutorial as well. 

[Matrix](https://matrix.org) supports voice and video already, as well as rooms with various permissions. Building a Matrix based drop in audio client is probably the closest fit in terms of having a full stack of social network features already -- and it's already decentralized and federated, where you can run your own home server.

A Discord bot and built in voice channels could probably do something interesting.

I didn't mention [@TwitterSpaces](https://twitter.com/TwitterSpaces), audio chat being built into Twitter directly. I think it will do well, and I'm much more likely to use it, since I think of Twitter as a platform native to the web (as opposed to mobile app). What will they do to add APIs & make it open & programmable?

_Fun fact: this was the first blog post that started out as handwritten pages on my new [[reMarkable]] paper tablet_