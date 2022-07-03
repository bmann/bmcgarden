---
title: Ubuntu
---

# Add a user to sudo group

`usermod -aG sudo <username>`

# Count files recursively in a directory

`find <directory> -type f | wc -l`

Also suppress permission denied errors:

`find <directory> -type f 2> /dev/null | wc -l`

# Reference Articles

## Installing node / yarn on Ubuntu 18

https://linuxize.com/post/how-to-install-yarn-on-ubuntu-18-04/

* For nodejs, `sudo apt-get install nodejs` gets you node8 (which is old)
* So, need `curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -`
* which leads us to yarn `curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list`
* `sudo apt-get update && sudo apt-get install yarn`
* `sudo apt-get install -y nodejs`