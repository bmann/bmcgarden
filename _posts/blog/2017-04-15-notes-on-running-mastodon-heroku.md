---
title: Notes on running your own Mastodon instance on Heroku
date: '2017-04-15T15:34:34-07:00'
tags:
  - Heroku
  - Mastodon
---

Darren Barefoot kicked off a <a href="https://www.facebook.com/dbarefoot/posts/10155060142235600" data-href="https://www.facebook.com/dbarefoot/posts/10155060142235600" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">discussion on Facebook</a> asking if people wanted to run Mastodon locally:

> Who wants to help me set up a Mastodon instance for Vancouver-related stuff? I’ll provide the moral support, promotion and pay for hosting if someone wants to do the hard technical bits.
> Or maybe that’s the wrong vector. Maybe we should set up an NGO tech and digital instance. Or maybe both?

I responded that maybe everyone should run their own instance:</p>

<img class="graf-image" data-image-id="1*IWD5lyPAqw8NibZPfvHDNA.png" data-width="479" data-height="376" src="https://microblog.bmannconsulting.com/uploads/2020/c339a4e9e1.jpg">

Does it make sense for a community or group to run their own install? As much as I love open source, running an entire software stack securely — and not losing everyone’s data because you don’t have good backups — is a big job. I tend to discourage people from running their own software, instead mapping a domain name to Medium or Tumblr.

Quoting myself:
<blockquote name="a11d" id="a11d" class="graf graf--pullquote graf-after--p">From my point of view, anything with an API that I can map my own domain to meets the bar of a resilient service <a href="https://medium.bmannconsulting.com/self-hosting-doesnt-help-more-people-self-publish-b6bde64d2bcb" data-href="https://medium.bmannconsulting.com/self-hosting-doesnt-help-more-people-self-publish-b6bde64d2bcb" class="markup--anchor markup--pullquote-anchor" rel="noopener" target="_blank">Self-hosting doesn’t help more people self-publish</a>
</blockquote>

Kind of contrary to that, I wrote a response to <a href="https://hackernoon.com/mastodon-is-dead-in-the-water-888c10e8abb1">Mastodon is Dead in the Water</a> saying that people should <a href="{% link _posts/blog/2017-04-09-run-your-own-mastodon-instance.md %}">run their own Mastodon instance</a>.

I was still in Toronto at the time, and actually got Mastodon setup using just the browser on my phone with the <a href="https://github.com/tootsuite/documentation/blob/master/Running-Mastodon/Heroku-guide.md">Deploy to Heroku button</a>. This is a feature of Heroku I love, and I’ve created several of these buttons of my own to help people get apps up and running.

This Easter weekend (it took me a solid half a day yesterday) I finally did the work to fully setup a Mastodon instance. I set one up for [[Frontier Foundry]] my new venture. I thought we might use it for links and tweet-length commentary for us and our portfolio companies. Or it might just be something to experiment with for a couple of weeks.[[This Mastodon server is no longer around, so it was a relatively short lived experiment.::rmn]]

<img class="graf-image" width="700" height="340" src="https://microblog.bmannconsulting.com/uploads/2020/8831df6ccf.jpg">

My profile on the Frontier Foundry Mastodon instance lives at `mastodon.frontierfoundry.co/@boris`. There’s even an RSS feed for each user which enables interesting re-use — I’ve setup an IFTTT recipe that posts anything from that feed to my Twitter account if it contains the keyword “share”.

## Setting up Mastodon on Heroku

Here are the things you’re going to need to have accounts on / be comfortable working with:

* a domain name and a registrar where you can edit DNS settings: I tend to use [[Namecheap]], while [[Hover]] is my “regular user” recommendation that also happens to be Canadian. Domains tend to be about $10USD per year, although there are also much cheaper ones and specials.
* an Amazon AWS account: accounts are free although you will have to have a credit card attached. The S3 file storage here will cost perhaps $1USD per month at most.
* Heroku account: accounts are free, you’ll need a credit card attached to your account, and I am currently paying what will amount to $14USD per month for hosting

Next, you may very well need to have a desktop computer setup with Ruby, Node, git, and a full suite of developer tools to be successful in getting everything working.

Reading <a href="https://ashfurrow.com/blog/running-mastodon-on-heroku/">Ash Furrow’s Running Mastodon on Heroku</a> meant that someone had hit many roadblocks ahead of me and figured out some of the workarounds, which was great. The setup I ended up following was two Heroku installs to get the Streaming API working, as per the <a href="https://github.com/tootsuite/mastodon/issues/1119#issuecomment-292816340">comment in this issue by ecmendenhall</a> (thanks Connor Mendenhall!).

I wasted a lot of time setting things up from scratch with a fresh clone of mMstodon, when starting with the Deploy to Heroku and just adding the second streaming server would have probably been a better decision.

The other thing that took a lot of time was setting up the Heroku Mailgun add-on. After you add it, you need to verify yourself, and then take a whole bunch of other steps in both Mailgun and your DNS / MX settings for it to be fully working. Do this right at the beginning.

I’ve still got one piece of troubleshooting / bug to figure out with Amazon S3 settings where S3_BUCKET and S3_HOSTNAME duplicate each other (and even there I’m not going to bother doing SSL with Cloudfront, which means there is a mix of secure content and insecure images).

## Should people run their own software?

In short, the answer is no. The level of expertise — and I’m not even talking digital literacy, I’m talking learned, professional expertise — that someone requires to run, maintains, and secure software is very high.</p>

That’s one of the reasons I run as many things as I can on Heroku. I don’t have to worry about the lower levels of an operating system at all.

Docker is the other newest kid on the block, and Mastodon is setup to work well with Docker. But Docker and various places where you can host docker containers don’t solve the fact that you are still exposed to the entire operating system stack of a server, which is where many security and backup issues lie.

With Heroku, database backups are included, it’s just a snapshot of code and configuration, and Amazon S3 backs up the files automatically, too. Heroku even handles SSL certificates automatically for paid accounts.

The folks building mMstodon are helpful to a point in getting things running on Heroku, but ultimately are focused on maintaining a more traditional software stack that they use for their own development and deployment. I think that going forward, applications need to be designed to be deployed in simpler fashion, with less of a “stack” and more pluggable components.

What would a Mastodon that was designed to be run “serverless” look like?

## Decentralized and P2P apps of the future

I’ve been working a lot with blockchain and other decentralized / P2P applications lately. I wrote about the [Akasha decentralized blogging platform]({% link _posts/blog/2017-02-13-akasha-cross-post-planting-tag-flag-vancouver-bowen-canada.md %}) that runs on the Ethereum blockchain, and I’ve also poked about with [[Beaker Browser]], which runs on [[Dat Protocol]] underneath.

It was a lot of work to setup an instance of Mastodon on Heroku. For someone that has tinkered with open source tech and servers for 15+ years and has a computer science degree.

And with that, I’m still paying a relatively high amount (I don’t think I could justify $15/month or $180 years for just my personal usage), never mind “renting” a domain name from the DNS system. Mastodon works in a mobile web browser or with some iOS or Android apps, but I don’t think I could have completed the entire setup and install from my phone.

[As I wrote before]({% link _posts/blog/2016-08-01-self-hosting-doesnt-help-self-publish.md %}), I think the list of things we need to aim for with these future decentralized apps is:</p>

1. **Publish from a smartphone:** the smartphone will be the only computing device for most of the world going forward. Focus on it.
2. **No server hosting:** fully decentralized / peer-to-peer. There may still be various semi- or fully-centralized services for discovery, naming, trust, or other convenience functions.
3. **No domain names:** let’s not rent our identifiers, and let’s not build financial barriers to anyone “owning” their content online

I’m going to continue exploring in this space. In the meantime, it’s great to see Mastodon bringing a bunch of discussion forward, and for us all to think about federation, decentralization, and what that means for designing interactions.