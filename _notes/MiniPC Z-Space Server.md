## September 9th, 2024

I'm probably going to pave over this server again!

Had been looking at [[Unraid]] as a good baseline, including the way it can host Windows VMs.

### Ventoy

Found [[Ventoy]] and am going to attempt to pave over the Corsair 2TB USB-C NVMe drive I have.

Used `wget` to download the ventoy stuff and unpack it. None of the web gui stuff will work ATM because we have the server in a DMZ and I don't remember it's internal alternate IP address.

`networkctl status` is great for looking at all your network settings.

![screenshot of networkctl status command](/assets/2024/networkctl-status.png)

To get a list of disks / partitions under Ubuntu, use `lsblk`:

```
sudo lsblk -o NAME,FSTYPE,SIZE,MOUNTPOINT,LABEL
```

OK, Ventoy installed. I thought [[Unraid]] would have an ISO, but the whole point is to have bootable USB, so they don't support that. I guess I'll go buy a USB key for this!

### Unraid
Going to try out [[Unraid]].

Bought 2x [Lexar JumpDrive D400 128GB](https://www.lexar.com/product/lexar-jumpdrive-dual-drive-d400-usb-3-1-type-c/) from London Drugs and used the MacOS installer.

Spent like 20 minutes trying to get it to boot with various settings on [[MiniPC PL63]], found various hints on forums that turning off ASUS Fast Boot makes things works.

It also helps if you didn't accidentally swap the empty USB key for the formatted one!

Actually getting Unraid installed was pretty much all automatic. I ended up buying a basic license for it, and am now poking around the web interface.

It looks like a very robust system, BUT, I don't think it's a good fit for the [[MiniPC PL63]], which only has Thunderbolt 4 as expansion. The Unraid devs strongly recommend against USB-C connected storage.

Their home page has this very interesting [LincStation N1 NAS](https://www.lincplustech.com/products/lincstation-n1-network-attached-storage) as one example, listed at $399USD.
## August 1st, 2024

[[MiniPC PL63]] got wiped and Ubuntu Server installed. 

The interface for partitioning drives, now with Logical Volume Manager, is just as confusing as ever. It sets aside 100GB for a default install and leaves the bulk of the drive empty. 

The import keys from GitHub experience is really nice. 

Jonno had previously setup a VLAN to be a DMZ where the Z-Brain server is running, on `192.168.1.x`. 

Configured the MiniPC to be on that same network. It routes through a UniFi 4 port Switch. Had to also configure the port that it plugs into on the switch to automatically route that VLAN rather than the default one. Otherwise the machine is on the default VLAN and gets an IP from there. 

Much searching of network interface commands for Ubuntu. `networkctl` is installed by default and the one you want. 

Port forwarding is configured on external IP address to forward to the internal DMZ IP address. So, we only open ports (22, 80, 443) that we want to let through to the server. We still have one public IP address available. 

Tested ssh from all IP addresses, internal and external, all worked. 

Installed [[Coolify]] by generating a public/private key pair and copying the private key to authorized keys in the root account of the machine. Used the external public IP address and Coolify connected and installed everything else remotely.

Did a test install of Ghost, which worked, and used Coolify's default temp domain thing. Need to map [[BringYourOwn.Computer]] as the default domain for it. 

Probably also need to look at S3 Storage and backup options. Trying to use my [[Storj]] account -- but this mostly only works for backups, as it doesn't support public files.

---
I mapped BYOC domain and couldn't get anything working. The dreaded "too many redirects" no matter what I did. You have to set [[Cloudflare]] encryption settings to "Full", and then everything will start working.

Succeeded at a test install of [[Docmost]], a new-to-me wiki package that looks pretty good.