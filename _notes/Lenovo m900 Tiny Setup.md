---
tags:
  - homelab
---
I’m going to go over a lot of the yak shaving I  did to set up the [[Lenovo M900 Tiny]].

## Different Specs

As noted [[2024-01-19_1306]], I received a different spec. Booting into windows and the overview showed me:

```
Processor Intel(R) Core(TM) i5-6600T CPU @ 2.70GHz   2.71 GHz
Installed RAM 8.00 GB (7.89 GB usable)
```

Looking at the hard drive, it's 1TB.

And my [Amazon order](https://www.amazon.ca/gp/product/B07ZPBDFGD/ref=ppx_od_dt_b_asin_title_s00?ie=UTF8&th=1) was supposed to be "Quad-Core i5-6500T, 16 GB DDR4, 480 GB SSD Intel Graphics, USB WiFi, Windows 10 pro 64 Bit"

There also isn't any Wifi in the one I received.

So, half the RAM, faster processor, twice the hard drive space, and no Wifi. I will probably just keep it, but feels like less RAM will be a challenge.

## Initial Unboxing

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

Download a server image and [unetboot](https://unetbootin.github.io/). Apparently Ubuntu recommends [Rufus](https://rufus.ie/en/) for this.

Burn image to USB key. I ordered a new USB key at the same time as the m900, knowing at least I would need a spare or so for this. 

Attempt to follow instructions on disabling UEFI secure boot. 

## Installing Ubuntu

Researched various Lenovo things. `F12` is what you need to press in order to get into firmware and boot settings.

Selected the USB key to boot from.

Chose the [Ubuntu Server install](https://canonical-subiquity.readthedocs-hosted.com/en/latest/tutorial/screen-by-screen.html)

Got to the storage section and the 750GB unformatted part of the drive wasn't visible. The [server storage guide](https://canonical-subiquity.readthedocs-hosted.com/en/latest/explanation/configure-storage.html#configure-storage) says:

> The installer cannot edit partition tables. You can use existing partitions or reformat a drive entirely, but you cannot, for example, remove a large partition and replace it with two smaller ones.

Went into the help menu and got into the terminal. Thought about it for a bit and looked at some partition formatting links (all of the defaults show a graphical editor), and decided to boot back into Windows.

In Windows, formatted the the 750GB, then booted back into the installer.

Used LVM, made `/` root of 30GB, swap of 20GB, remaining as `/home`

Install was very quick. Named the server `tinyhome`.

There's an option to add SSH keys from Github. Entered my username and it fetched a couple of keys.

Rebooted to Grub menu, then on to commandline login. Can I get it to automatically boot into Ubuntu? It's going to be running headless.

Read some [background on Grub settings](https://ubuntuforums.org/showthread.php?t=1195275). Tried to get it to boot into Ubuntu / last saved OS by default with a short 3 second time out.

`sudoedit /etc/default/grub`

`sudo update-grub`

None of the things I applied and rebooted did anything other than bring me back to a menu with a 30s countdown that defaults to Ubuntu. OK fine!

Moved to living room and rebooted. Had previously set the router to give this device the same IP address.

Logged in with my ssh keys. Success!

Oh oh. Revving, **screaming** fan noises that ramp up and down. Searched a bunch of things, and now...fan noises have gone away.

Need to do more research, because having it screaming in the corner of the living room is not going to be OK.[^livingroom]

[^livingroom]: It's in the living room, because that's where the cable connector for my Internet comes out, and where the router is plugged in.

## Fan Control in Ubuntu

Found page on [controlling fan speed in Ubuntu](https://askubuntu.com/questions/22108/how-to-control-fan-speed). 

```
sensors-detect version 3.6.0

# System: LENOVO 10FLS02D00 [ThinkCentre M900]
# Board: LENOVO 30D0
# Kernel: 5.15.0-91-generic x86_64
# Processor: Intel(R) Core(TM) i5-6600T CPU @ 2.70GHz (6/94/3)

This program will help you determine which kernel modules you need
to load to use lm_sensors most effectively. It is generally safe
and recommended to accept the default answers to all questions,
unless you know what you're doing.

Some south bridges, CPUs or memory controllers contain embedded sensors.
Do you want to scan for them? This is totally safe. (YES/no):

Driver `coretemp':
  * Chip `Intel digital thermal sensor' (confidence: 9)
Driver `nct6683':
  * ISA bus, address 0xa20, Chip `Nuvoton NCT6683D eSIO' (confidence: 9)

To load everything that is needed, add this to /etc/modules:

#----cut here----

# Chip drivers

coretemp
nct6683

#----cut here----

If you have some drivers built into your kernel, the list above will
contain too many modules. Skip the appropriate ones!

Do you want to add these lines automatically to /etc/modules? (yes/NO)
```

Ran `pwmconfig`:

```
/usr/sbin/pwmconfig: There are no pwm-capable sensor modules installed
```

Did some research. Found [this thread](https://github.com/vmatare/thinkfan/discussions/215) with this comment from January 2023:

> On an M900 I had to force the kernel to load the nct6683 driver as stated here: [https://bugs.launchpad.net/ubuntu/+source/lm-sensors/+bug/1858369](https://bugs.launchpad.net/ubuntu/+source/lm-sensors/+bug/1858369)

So apparently I can force a kernel module to load, but getting various permission errors.

```
echo "options nct6683 force=1" >> /etc/modprobe.d/sensors.conf
```

OK, you really do need to be `root`, so `sudo su` it is.

### Fan Screaming

The fans are screaming this morning, so trying this again. This is applied after reboot, running `pwmconfig` now gives some output:

```
Found the following PWM controls:

   hwmon2/pwm2           current value: 243

/usr/sbin/pwmconfig: line 180: hwmon2/pwm2: Permission denied

Giving the fans some time to reach full speed...

Found the following fan sensors:

   hwmon2/fan2_input     current speed: 7017 RPM
```

The fans really are too loud, and 7017 RPM is a lot.

Research links:
* older ubuntu, very extensive <https://ubuntuforums.org/archive/index.php/t-42737.html>
* odroid related <https://forum.odroid.com/viewtopic.php?t=41911>
* archlinux <https://bbs.archlinux.org/viewtopic.php?id=225349>

Running `sensors`:

```
nct6683-isa-0a20

Adapter: ISA adapter

VIN0:             1.42 V  (min =  +0.00 V, max =  +0.00 V)

VIN1:             1.02 V  (min =  +0.00 V, max =  +0.00 V)

VIN3:           704.00 mV (min =  +0.00 V, max =  +0.00 V)

VIN0:             1.42 V  (min =  +0.00 V, max =  +0.00 V)

fan2:           6936 RPM  (min =  500 RPM)

PECI 0.0:        +28.5°C  (low  =  +0.0°C)

                          (high = +99.0°C, hyst =  +0.0°C)

                          (crit =  +0.0°C)  sensor = Intel PECI

PCH CHIP:         +0.0°C  (low  =  +0.0°C)

                          (high =  +0.0°C, hyst =  +0.0°C)

                          (crit =  +0.0°C)

Diode 0 (curr):  +28.5°C  (low  =  +0.0°C)

                          (high =  +0.0°C, hyst =  +0.0°C)

                          (crit =  +0.0°C)  sensor = thermal diode

Diode 1 (curr): +121.5°C  (low  =  +0.0°C)

                          (high = +50.0°C, hyst =  +0.0°C)

                          (crit =  +0.0°C)  sensor = thermal diode

intrusion0:     OK

beep_enable:    disabled

  

acpitz-acpi-0

Adapter: ACPI interface

temp1:        +27.8°C  (crit = +119.0°C)

temp2:        +29.8°C  (crit = +119.0°C)

  

coretemp-isa-0000

Adapter: ISA adapter

Package id 0:  +29.0°C  (high = +84.0°C, crit = +100.0°C)

Core 0:        +26.0°C  (high = +84.0°C, crit = +100.0°C)

Core 1:        +26.0°C  (high = +84.0°C, crit = +100.0°C)

Core 2:        +24.0°C  (high = +84.0°C, crit = +100.0°C)

Core 3:        +27.0°C  (high = +84.0°C, crit = +100.0°C)
```

Temperatures aren't high, but fan2 is at 6900-7000+ RPM.

So kernel driver is <https://www.kernel.org/doc/Documentation/hwmon/nct6683>

Maybe I need to flash BIOS? Found something that relates to [M900 BIOS and fan control issues](https://support.lenovo.com/ca/en/solutions/ht500771-fan-control-issue-thinkcentre-thinkstation)

Checking BIOS under Ubuntu with `dmidecode | less`:

```
BIOS Information
        Vendor: LENOVO
        Version: FWKTBFA  
        Release Date: 06/23/2022
        Address: 0xF0000
        Runtime Size: 64 kB
        ROM Size: 16 MB

System Information
        Manufacturer: LENOVO
        Product Name: 10FLS02D00
        Version: ThinkCentre M900
        Serial Number: XXXXXXX
```

Looks like [updated BIOS from July 2022 is available](https://pcsupport.lenovo.com/ca/en/products/desktops-and-all-in-ones/thinkcentre-m-series-desktops/thinkcentre-m900/downloads/ds105487), but I need to boot back into Windows to apply.

### Fan BIOS Update 

Unplugged everything from the living room and brought it back to plug in monitor and booted into Windows. 

Applied the updated BIOS and grabbed a few other drivers from the Lenovo site. 

Sitting at around 1000 rpm and not really audible when sitting on top of the desk. Brought it back out to the front of the apartment. 

Silent? Can’t hear it? Fingers crossed that fixed it!
## Server Management Install

Decision point: [[Cloudron]] or something else?

Looking at [[Coolify]] again, it needs Debian as the "admin", and also it is still quite a new system. I would probably try the hosted Coolify at $5/month as the admin controller. 

[[Easypanel]] is proprietary, but maybe not that different from [[Cloudron]]?

## Cloudron Install

OK, let's [install Cloudron](https://www.cloudron.io/get.html). It has a [Home Server Installation in the docs](https://docs.cloudron.io/installation/home-server/).

Found my public IP address. Let's see if I can connect to it after a reboot.

Connected via the `home.bmann.ca` "local" DNS setting that I put into the Unifi router settings.

On the Domain Settings screen. Not really sure what to pick here. I guess I can pick either manual or wildcard. Or, I can use Cloudflare API and let it manage parts of `bmann.ca` that are already being managed by [[Commons Computer]] install.

[Cloudron Private DNS settings](https://docs.cloudron.io/networking/#private-dns)

OK, sure, let's go straight to advanced mode and setup some local addresses.

```
local-zone: bmann.ca." typetransparent
local-data: "home.bmann.ca. A 192.168.1.67"
local-data: "my.home.bmann.ca. A 192.168.1.67"
```

Sure, let's setup Cloudflare and see what happens. Make a new API token with access to `bmann.ca`, setup `home.bmann.ca` as the domain, and `my.home.bmann.ca` would be where the panel ends up.

Get an error: `queryNs ECONNREFUSED bmann.ca`, search for cloudron: <https://forum.cloudron.io/topic/2008/queryns-econnrefused-cloudron-intra-example-org>

Doesn't like NoOp either `Unable to detect IPv4. API server (ipv4.api.cloudron.io) unreachable`

OK, none of this is going to work until I port forward. Let's go look at Unifi Router.

Port forwarding for tcp/80 and tcp/443 setup to the internal IP address of the server. Confirm that I can get to the Cloudron setup page from the public address.

## Cloudron Install Part 2

OK, I turned off that Unifi local DNS of `home.bmann.ca`, and undid all of the private DNS settings. Accessing Cloudron from the public IP address, and it is being forwarded to the server.

Now setting this as the domain, with Cloudflare API key. I'm in, Cloudron installed.

Enabling [Dynamic DNS](https://docs.cloudron.io/networking/#dynamic-dns) under Network settings -- Cloudron will use my Cloudflare API key to update the public address if my home connection IP changes.

Setting up backup. [[Commons Computer]] uses my Digital Ocean account, but I recall that I have a [[Storj]] account, which is decentralized file storage. There is a free tier, and even at the paid tier it has 25GB included for free. I upgraded to a pro paid account by sending some STORJ tokens via Ethereum[^tokens].

[^tokens]: went to [Uniswap](https://app.uniswap.org), swapped some Ethereum for 100 STORJ (about $60USD). Sent 50 STORJ to the receiving address Storj gave me, once it was confirmed they credited me 55 STORJ (10% bonus for paying with tokens).

OK, we're up and running. I don't really have a plan for this machine, other than it's _inside_ my home. Let's setup a `home` group for permissions, which just has my `boris` user in it. I might give some other people accounts on Cloudron, but they shouldn't have access to this home group.

I guess I'll start by just creating a [[Surfer]] app running, for static file serving and WebDAV, right at the base domain <https://home.bmann.ca>.

## Custom IPFS App

I’m going to add [[IPFS Self Hosting]] as a custom app. 

