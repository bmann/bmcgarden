---
---

alias:: [[Nextcloud AIO]]
github:: https://github.com/nextcloud/all-in-one
tags:: #docker, #opensource

- Notes for my [[Boris Mann/Home Lab]] setup running on [[Mac Mini]]
	- We do want to run it with a reverse proxy https://github.com/nextcloud/all-in-one/blob/main/reverse-proxy.md
	- Notes on running on MacOS https://github.com/nextcloud/all-in-one#how-to-run-aio-on-macos
		- > On macOS, there is only one thing different in comparison to Linux: instead of using `--volume /var/run/docker.sock:/var/run/docker.sock:ro`, you need to use `--volume /var/run/docker.sock.raw:/var/run/docker.sock:ro` to run it after you installed [Docker Desktop](https://www.docker.com/products/docker-desktop/) (and don't forget to [enable ipv6](https://github.com/nextcloud/all-in-one/blob/main/docker-ipv6-support.md) if you should need that). Apart from that it should work and behave the same like on Linux.
		- Also, you may be interested in adjusting Nextcloud's Datadir to store the files on the host system. See [this documentation](https://github.com/nextcloud/all-in-one#how-to-change-the-default-location-of-nextclouds-datadir) on how to do it.
			- > On macOS it might be `--env NEXTCLOUD_DATADIR="/var/nextcloud-data"`
		-