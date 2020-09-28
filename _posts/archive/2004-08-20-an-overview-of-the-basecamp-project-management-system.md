--- 
layout: post
title: An overview of the Basecamp project management system
created: 1093013638
categories: 
- Web 2.0
- Social Media
- Review
---

<p><a href="http://www.bmannconsulting.com/node/1278#comment-2034">Troy asked</a> for an update on our use of <a href="http://www.basecamphq.com">Basecamp</a>.</p>

<p>Yes, we're keeping it. It's a bit like &quot;project management light&quot;, but this is definitely what is wanted if you don't want to get bogged down in updating some sort of tool, but you do need something to organize multiple people and multiple projects that are going on in parallel. Hit the read more link for the full story.</p>
<!--break-->
<p>Basecamp facilitates keeping communications about a project all in one place by the use of messages, which can be:</p>
<ul>
<li>organized into different, customizable categories</li>
<li>use check marks to specifically notify selected or all project members via email</li>
<li>be associated with and/or complete milestones</li>
<li>Have files attached</li>
<li>be monitored via email updates or by using RSS (more on this later)</li>
</ul>

<p>Before moving on to milestones, let me briefly mention files. They have their own tab with which you can upload files directly without attaching them to a message, but the most common use is to associate them with a message.</p>

<p>Files are actually stored on <strong>your</strong> server, not Basecamp's, which neatly does away with the problem of storage space -- you're free to upload as much as you want, as long as your system has space. This is accomplished by setting up FTP details in the Basecamp system, so that when you upload, you're actually uploading to your own system. For less technical users, this might be a bit of a barrier, but FTP is generally very easy to set up and virtually every web host supports.</p>

<p>They don't currently offer SFTP or WebDav support, but are considering them.</p>

<p>Milestones are the only &quot;dated&quot; item in Basecamp. We use it to track &quot;real&quot; milestones -- when stuff is due, is going live, etc. -- as well as other dated events like meetings. This allows some very easy shared calendar, although specifically focused on projects (it won't show you that the boardroam is booked at 2pm, and in fact doesn't use time at all -- only dates).</p>

<p>As mentioned, messages can be associated with milestones. When creating a message, you can opt to select the project milestones from a drop down list, and then a link to the message will show up organized underneath the milestone. As well, there is a checkbox listed as &quot;This message completes this milestone&quot;, which is a good way of giving a description of how the item was completed without having to separately go and check off the milestone.</p>

<p>As well as being the only dated item, milestones are the only item that can be made the responsibility of someone directly. You can choose to make a company (e.g. YourCompany, YourClient) responsible, or you can choose one person.</p>

<p>To do lists are the third major item in Basecamp. They can also be associated with milestones in the same manner as messages, although they cannot be used to (directly) complete milestones. They are very easy to create, consisting of a title and as many text-based items as you want. Since you can't associate a person responsible with a to do list or individual items, you can use several different strategies. You might have a shared to do list, like &quot;Website Pre-Launch Checklist&quot;, that uses initials beside particular items. Or, you could title the to-do list to include a person's name.</p>

<p>This <em>is</em> a bit awkward -- I'd like the ability to choose to associate people (or not) the same as milestones. The text labelling seems to be working for now.</p>

<p>It does make sense that individual to-do items don't have dates -- if it is something that is required for a specific date, it should be a milestone.</p>


<p>Lastly there are contacts associated with projects. You need to have admin access to create projects and contacts (really, there are only admin users and non-admin users, although how contacts are set up does give you some additional granularity). As part of setting up Basecamp, you set up your company (of which you are obviously a member). Later users are then added as a contact at your company (where they can be listed as an employee or a contractor) or as a contact at a client company. Employees by default have access to any new projects you create (so you must uncheck access for them), while contractors must be manually given access on a per-project basis. Client contacts can only have access to projects which are associated with their company, and can be given read-only access.</p>

<p>So, while the different types of access are quite simple, in practice they tend to be rich enough. The one downside is that usernames are unique per instance of Basecamp. Most people wouldn't see this as a problem, but I am using the system in several companies, so have a different login for each instance. This could easily be solved by making users global, and by keying by your email address instead of a username.</p>

<p>There are two other aspects that I'm going to mention but not go into much detail about. RSS can be used to notify you of any changes -- this can be done on a per-project basis, or for your entire Basecamp instance. There is also iCal support, with one iCal per project that shows milestones in the calendar and the to-do lists as tasks. While it's called iCal like the <a href="http://www.apple.com/ical">tool from Apple</a>, it does also work with Mozilla-based browsers. This includes the newly-released-and-too-early-to-use-seriously <a href="http://www.mozilla.org/projects/calendar/sunbird.html">Sunbird</a>, which is Mozilla's new stand-alone calendaring app, or the <a href="http://www.mozilla.org/projects/calendar/download.html">Calendar extension</a> that works with the full version of Mozilla, Firefox, or Thunderbird on all platforms.</p>

<p>iCal on Mac OS X is the only system on which it's really easy to add a calendar -- I'll go into full setup details for the Mozilla's if people want.</p>

<p>And no, it doesn't integrate with Outlook. This is still the default email application on many users' desktops, even if they don't use an Exchange server. So I'm looking for an easy way to sync/integrate iCal into Outlook.</p>

<p>Whew! Well, that was more a description of the system than a review. We are happy with this &quot;good enough&quot; solution, and will continue using it. And I never did mention the elegant interface, but that's really the point -- it's good enough that it doesn't get in the way of actually using the system. Check the <a href="http://everything.basecamphq.com/">Everything Basecamp</a> site for more information -- it's the &quot;official news and support blog&quot;.</p>

<p>If our thoughts change, I'll post again. In the meantime, here's a link to a <a href="https://secure.basecamphq.com/signup/Free">completely free one project plan</a> -- with no 30 day trial and no credit card required. You can still upgrade at any time.</p>
