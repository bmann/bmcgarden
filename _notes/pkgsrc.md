---
title: Pkgsrc
---
_NetBSD package manager, 20K+ packages, works on [[ChromeOS]]_

* http://pkgsrc.org
* http://pkgsrc.se - search for packages

## pkgsrc on ChromeOS

Presentation at FOSDEM 2018:
https://docs.google.com/presentation/d/e/2PACX-1vSk7dCv8sNycDkuaHi-vmxZpVjrGLOYbLRXkDW2s9nMrR4a_UGsMsl_GOHi4NOpsOtzpZMp_4U5k7zH/pub?slide=id.p

By https://github.com/bsiegert

1. Bootstrap with [Chromebrew](/chromebook/chromebrew) to get gcc then other packages can be installed from source.

```crew install gcc linuxheaders```

2. Download tarball http://ftp.netbsd.org/pub/pkgsrc/current/

3. Extract in ```/usr/local```

4. Set SH and Run bootstrap

```export SH=/bin/bash```

```cd /usr/local/pkgsrc/bootstrap```

```
./bootstrap \
--unprivileged \
--prefix /usr/local/pkg \
--varbase /usr/local/pkg/var \
--pkgdbdir /usr/local/pkg/pkgdb \
--cwrappers=no \
--prefer-pkgsrc=yes \
--make-jobs=6
```

Currently errors:

```sed: -e expression #15, char 34: e/r/w commands disabled in sandbox mode```

Had this same issue elsewhere (installing emacs), and installed chromebrew's sed version, ```crew install sed```. Didn't work here, likely have to give it the path to chromebrew's sed.