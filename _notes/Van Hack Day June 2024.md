---
tags:
  - Vancouver
  - event
---
Personal notes for [[Vancouver Hack Day]] June event.

Got into [[Z-Space]] around 8:30am, made a coffee
* Printed out more Z-Space visitor wifi QR codes
* Made a [[DWebYVR]] Discord chat qr code
* Added the QR code as an image to the [contact page](https://dwebyvr.org/wiki/Contact)

Did a round of intros of who we are and what people are planning to work on

Settling down to look at [[Lieu]]
* Last updated in March 2022
* Where should I host it? I have [[Portainer]] running on [[Hostinger]]
* Turned off [[AFFiNE]] and [[Ghost]] installs there
* There are a bunch of templats, including a "plain" Ubuntu install

Ubuntu image on Portainer
* access to only administrators
* network - bridge or host? this is a [[Docker]] question
* use the default bridge
* created with name lieu
* using attach in Portainer to get a web-based root commandline
* very minimal Ubuntu installed, but latest system
* What version am I running? [[Ubuntu]] -> noble 24.04 LTS

Create a repo [dwebyvr/localhost_vancouver_webring](https://github.com/DWebYVR/localhost_vancouver_webring)
* check it out locally, clone the `config.toml`
* make a website directory and index.html as the source
* realize that Surfer already installed on [[Commons Computer]] -> [localhost.dwebyvr.org](https://localhost.dwebyvr.org)

Make an index.html file with ULs to have a public source for URLs
* checked into repo
* Manually published 
* File an issue to automate this via GitHub Actions

Made spaghetti lunch to stretch sandwiches 

Made coffee for many people. 

David demo’d [[LoFi]] work he’s doing 

I went off to [[Daylight Computer]] meetup. It was in [[Anjan Katta]]’s parents backyard. 

Came back for end of day demos 
