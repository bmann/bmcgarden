## What version of Ubuntu am I running?

[Ask Ubuntu](https://askubuntu.com/questions/686239/how-do-i-check-the-version-of-ubuntu-i-am-running)
* [official page](https://help.ubuntu.com/community/CheckingYourUbuntuVersion) says  `lsb_release -a` - listed on Description line
* `hostnamectl` - listed on Operating System line
* `cat /etc/*release` - DISTRIB_RELEASE or DESCRIPTION