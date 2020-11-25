---
title: CLI
tags:
    - unix
    - cli
---
Various Command Line Interface tips and tricks

Some of the things at [[Ubuntu]] are Ubuntu Linux specific, some of them will work on other systems, including in the MacOS Terminal.

## lsof

`lsof -i :8080`

Will list what's running on port 8080.

Looking up the process ID (PID) means you can get more info, or `kill [PID]` to shut it down.


See also: [Daniel Miessler's An lsof Primer (2019)](https://danielmiessler.com/study/lsof/)