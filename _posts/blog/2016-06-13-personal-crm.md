---
layout: post
title: Personal CRM
date: '2016-06-13T12:34:34-07:00'
excerpt: "I’ve been once again looking for a personal CRM. Something that gets to do’s out of my inbox, collects data and messages on the people that I’m interacting with, and generally keeps me informed and up to date in my communications. Here's a review of past tools and analysis of my choice."
categories:
- Review
tags:
- CRM
- Highrise
- Streak
- Insightly
- Pipedrive
comments: true
---
I’ve been once again looking for a personal CRM. Something that gets to do’s out of my inbox, collects data and messages on the people that I’m interacting with, and generally keeps me informed and up to date in my communications.

Google is the system that runs my personal and work email accounts & stores my contacts, but it continues to have terrible support for anything other than just storing contacts. And randomly adding someone you email to “My Contacts”.

Apple as well doesn’t do much other than a basic flat file storage of contacts, albeit with some basic linking of contacts stored in different back ends, thus guaranteeing that you’ll have bits and pieces of contact data scattered all over the place.

I call it a Personal CRM, because I want it to work for me, whether I’m freelancing and doing consulting as an individual, working on a community project while I’ve got a day job, or any other combination.

Picking a CRM for your business is a team affair, and balances different needs. What works best for one person?

## All the CRMs
In the past, I’ve used the highly social media integrated Nimble. I’ve used Batchbook for its extensive tagging and custom data fields. I have a Full Contact account, but it really only syncs contacts, and does nothing with messaging or activities.

I recommend Pipedrive as the CRM that startups and small businesses should use for running their sales pipeline. It also has a great NodeJS API if you need to extend it.

Streak is a Gmail plugin that works well in support of raising a round or lightweight mail merge tasks, great for people like me that run their email in the browser on the desktop.

Capsule CRM has a free forever plan, will automatically look up social accounts, and like Batchbook has the concept of custom fields that you can attach to tags.

Insightly. Sigh. Insightly, I really want to pick you. My database-social-graph-loving tendencies love the fact that you can basically link anything to anything, and even define your own relationships between objects (Organization X is the Accelerator of Startup Y, Startup Y is Accelerated By Organization X). But your user interface is pretty terrible, you won’t even do basic mail merge, and you seem to have way too many Projects and Opportunities and Tasks that are overkill for even groups of people, never mind one person. And your mobile app is bad, too. But I still use you for some things, because that link-everything-together is pretty amazing.

Why yes, I do try a lot of tools. And there are even some that I haven’t listed that aren’t terrible. But the list above are all ones that I might recommend for particular use cases. And then there are tools like Airtable, which are excellent for building ad hoc databases or custom data trackers.

## Picking Highrise
I’ve attempted to use Highrise many times over the years. Recently, as the-company-formerly-known-as-37Signals rebranded as Basecamp, they kicked out all their other apps into separate companies. The whole purpose of doing this is so those other apps could get the attention they needed.

It was great to kick the tires on Highrise and realize that their philosophy was a good match for what I wanted out of a Personal CRM:

Your address book doesn’t do enough, CRM software tries to do too much. Stay connected with simple contact management.
Highrise has a free-forever plan that includes 2 users, 250 contacts, 3 cases, and no file storage. The fact that they have a Solo plan clearly means they understand that some people will use them as individuals. I ended up on the Basic plan, because I don’t need more than 10 deals and it’s $5 cheaper than the Solo. None of their plans have per-user fees, showing that it’s designed for smaller groups.

Highrise is not a traditional sales pipeline CRM, which is likely why it makes a good Personal CRM.

It has People and Organizations as Contacts, and you can add Custom Fields to them (which will apply to both kinds of contacts). You can also add different custom fields to Deals. Highrise probably has the most simplistic custom fields compared to the other tools listed above.

Like most CRMs, you can BCC or forward email into Highrise. You can also add Gmail accounts directly to Highrise, and send email directly from within the app. This means that while you’re reviewing your tasks, you can send email to complete that task, without getting drowned in your inbox. I’m going to experiment further with sending business email directly to Highrise. There’s a whole page in the help system on Autoforwarding emails from Gmail »

There’s also the Broadcast mass email tool, which you can use as a lightweight mailing list. I really like Streak’s amazing & easy mail merge, which sends the same-but-personalized message to multiple people, which is a feature I’d like to see in Highrise.

Deals are what I’m using to track / follow up on things that might or might not happen, but that need to come to a close. This could be a consulting gig, a speaking engagement, or confirming sponsorships. Another less obvious use case is for tracking down and confirming speakers for an event.

I’m using Cases as projects. They’re a different kind of container that — unlike a Deal — can be more topical and ever present, and doesn’t need to end. I have a handful of longer term Cases related to mentoring and advising companies, and the rest are projects I need to finish in the next couple of months. I am itching to add a couple more Cases, but that’s likely too much to commit to. This is a good thing!

I’ve always loved Tags. You can slice and dice your Contacts (People and Organizations) in lots of different ways. Company tags will show up on People entries, which is great to see next to each other. I wish that Deals and Cases could be tagged as well, since I’m kind of tag crazy, but especially for a single user, having an easily scannable number of each of those is probably the right way to go.

I mentioned Gmail accounts and email forwarding earlier. Emails are objects within the system that are linked to the people involved, and attachments will be uploaded and included.

Notes are text entries with optional Files attached. They can be placed within Cases or Deals, or attached to People or Organizations.

You can add Comments to both Emails and Notes.

There is a full text search of Emails, Notes, and Comments, another area where I’d love to potentially use Tags rather than hope that the full text search is up to the job. I’m still using Quip as my primary note taking and document creation & collaboration tool, so I’ll continue to use that for “stock” content, and really just use Notes for what they are — short snippets of text that are useful in the moment or as a reminder, not a long term place to store text information.

## Highrise Feature Requests
As I mentioned before, Highrise’s Custom Fields are pretty simple. They recently added pre-defined values — aka dropdown lists — for fields. But really, everything is just a plain text field. There are some nice touches, like if you put a URL like http://example.com into a Custom Field, it will automatically change it into a clickable link when it is displayed.

I’d like to see Custom Fields support People and Organizations. This means the “Referred By” field, for example, becomes a link to the Person or Organization.

As well, multiple entries rather than a plain text field open up interesting relationships. For example, link to multiple People or Organizations with a “Customers” field.

This also solves the problem of only being able to associate a Person with one, current Organization. If you want to track multiple relationships, whether a Person linked through an “Advisor” field, or a “Used to Work At” field continuing previous companies, this opens up that ability.

## Smarter Tools
I’m wanting to commit to a Personal CRM so I can work smarter, not harder. In the world of Contacts, Calendaring, To Dos, and Email, I’m still not getting as much smarts as I want out of my tools.

And of course, it’s all about process. I’m pretty good at Inbox Zero (as of writing, ~10 emails across 3 accounts), and I look forward to Highrise helping me get To Dos out of email even more.

We can talk about agents and AI, but in many cases the reality of the interfaces and the silo-ized data models are still holding us back.