I’m going to go over a lot of the yak shaving I  did to set up the [[Lenovo M900 Tiny]].

This is going to sit right next to my [[Unifi Dream Machine]] router plugged in via Ethernet, which is right at the front of our apartment. There’s a portable monitor there, but it only has USB-C as video input. 

This m900 has two DisplayPort connections and…a VGA connector. Maybe I can use my old projector as a screen? But no, I don’t have a female VGA cable, just male-to-male. Maybe this USB B (projector side) to USB-A will …just work if I plug it in?

What kind of adapters do I have? Should I plug it into the TV temporarily???

I had to take it into my back office (which only has wireless and this only has Ethernet) to plug it into the DisplayPort of my monitor. 

I’ll unplug the monitor from the USB-C KVM Switch (because I’m only going to have modern machines that all have USB-C, right), and also get my desktop keyboard and mouse out of the switch and directly into the m900.

I’m booting into Windows and it wants the Internet.

OK, can I plug it into my MacBook Air and bridge into its wifi? My USB-C adapter dongle doesn’t have Ethernet. Does the one I gave to Rachael have Ethernet? It does!

Is this even going to work? (searches for Mac Internet Sharing) Yes this is built into System Preferences -> Sharing. Do I know which interface this Ethernet adapter is? No, just enable them all.

OK, it works!

Now we have various times of ignoring all the Microsoft upsells and ask for information (this is Windows 10 Pro) and we get to a desktop. I have a Microsoft Account with some paid family plan stuff so I’m in.

Updates, turn on Remote Desktop. Let’s see if this works? It does not, because of the Ethernet to Mac sharing wifi, the m900 is double NAT-d.

Read some stuff about dual booting Ubuntu and Windows. Actually I search for it - in Microsoft Edge so I guess this is Bing - and it gives me sort of a ChatGPT interface with the answer. The links go to the most horrendous ad-filled pages but I kind of squint at the info. 

I don’t really need Windows on here but let’s keep it around just in case. Shrink the C partition to 200GB, leaving 750GB for Ubuntu. The wording in this dialog is bad. “Shrink by” is asking you how much smaller. “Shrink to” would make more sense to me. 

Download a server image and unetboot. Apparently Ubuntu recommends Rufus for this.

Burn image to USB stick. I ordered this at the same time as the m900, knowing at least I would need a spare or so for this. 

Attempt to follow instructions on disabling UEFI secure boot. 

NIGHT