[[MiniPC PL63]] got wiped and Ubuntu Server installed. 

The interface for partitioning drives, now with Logical Volume Manager, is just as confusing as ever. It sets aside 100GB for a default install and leaves the bulk of the drive empty. 

The import keys from GitHub experience is really nice. 

Jonno had previously setup a VLAN to be a DMZ where the Z-Brain server is running. 

Configured the MiniPC to be on that same network. It routes through a UniFi 4 port Switch. Had to also configure the port that it plugs into on the switch to automatically route that VLAN rather than the default one. Otherwise the machine is on the default VLAN and gets an IP from there. 

Much searching of network interface commands. `networkctl` is installed by default and the one you want. 

Port forwarding is configured on external IP address to forward to the internal DMZ IP address. We still have one public IP address available. 

Tested ssh from all IP addresses, internal and external, all worked. 

Did a test install of one click [[Ghost]] install. Still need to config Mailgun settings and also figure out how to access / edit the volume where content / templates are. 

Probably also need to look at S3 Storage and backup options. I’ll continue using my [[Storj]] account. 

Default domain routing. Need to map [[BringYourOwn.Computer]] as the default domain for it. 