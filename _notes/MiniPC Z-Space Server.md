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