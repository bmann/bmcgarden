---
link: https://daily.co
tags:
  - video
  - saas
  - app
  - devtools
  - webrtc
---
A developer platform for real-time voice and video.

Lets you build Zoom clones, 1000s of participants, recordings, etc.

Powers the [[Cal.com]] video.

## Daily Video Links for Google Calendar with Zapier
I'm using my own Daily API key to power the video meetings in my self hosted [[Cal.com]] at `cal.commonscomputer.com`. This works great, but I can't use it for ad hoc events that aren't scheduled through Cal.

I made a quick Zap on [[Zapier]] that adds a Daily video room to a calendar event.

1. Add the string `(DailyCo Video)` to a calendar event title. The Zap searches for events that match this string
2. Daily creates a new room that starts when the event starts and ends when it's scheduled to be over
3. Re-edit the event to add in the generated room link into location / description

![Screenshot of Zapier](/assets/2024/daily-google-cal-video-link.png)

This doesn't totally seem to be working. Ideally, I'd like something like the [Zoom for Google Calendar Extension](https://workspace.google.com/marketplace/app/zoom_for_google_workspace/364750910244) but powered by my own Daily API key.