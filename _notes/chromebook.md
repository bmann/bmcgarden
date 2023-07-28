---
title: Chromebook
---

I'm a fan of Chromebooks because they are what I used to love about my Macbook Air 11": small, powerful, computers with long battery life. In addition, they also happen to be pretty inexpensive -- a very good machine starts at $600CAD.

# ASUS Flip C302CA

I bought this new ASUS Chromebook in early 2018, because [The Wirecutter told me it was the best one](https://thewirecutter.com/reviews/best-chromebook/)

# Other Topics

[[Cloud Gaming on Chromebooks]]

# Tips

## Chrome & Android Apps can only Read / Write to Downloads

This means you need to use your _Downloads_ folder like the root of your user system.

* repos -- I made a folder called _repos_ and this is where I clone all my git repositories
* archive -- move stuff in here and either back it up to Google Drive or external SD card periodically

## Increase inotify
Various things that watch files for live reloading will throw errors.

* for ```gatsby develop``` nodejs will throw ```ENOSPC: no space left on device```
* ```jekyll serve``` will have issues, you can also run ```jekyll serve --nowatch```

Run this:

```sudo sysctl fs.inotify.max_user_watches=1048576```

And all should be well.

## Mount user as exec

See [crouton issues](https://github.com/dnschneid/crouton/issues/928)

```sudo mount -i -o remount,exec /home/chronos/user```

# Haskell
```crew install stack```

Works fine, everything else:

```
Unable to load cabal files for snapshot

----
Deleting cached snapshot file: /home/chronos/user/.stack/build-plan/lts-12.12.yaml
Recommendation: try running again. If this fails again, open an upstream issue at:
https://github.com/fpco/lts-haskell/issues/new
----

Unable to parse cabal file for bhoogle-0.1.3.5@sha256:a3393794b22faabeb564c57f4a9506390b6b97b9792c6b4e130f15bf116099fd,1806: NoParse "license" 7
```

From https://docs.haskellstack.org/en/stable/README/:

Ran ```wget -qO- https://get.haskellstack.org/ | sh```

Results:

```
Stack has been installed to: /usr/local/bin/stack

Since this installer doesn't support your Linux distribution,
there is no guarantee that 'stack' will work at all!  You may
need to manually install some system info dependencies for GHC:
  gcc, make, libffi, zlib, libgmp and libtinfo
Please see http://docs.haskellstack.org/en/stable/install_and_upgrade/
Pull requests to add support for this distro would be welcome!

WARNING: '/home/chronos/user/.local/bin' is not on your PATH.
    For best results, please add it to the beginning of PATH in your profile.
```

Added to ```.chromebash```

Running ```crew install gcc make libffi zlib libgmp libtinfo```

Bailed on zlib, others already installed

```stack build```

```
Preparing to install GHC to an isolated location.
This will not interfere with any system-level installation.
ghc-8.4.3...
```

Success!

## Hakyll

https://jaspervdj.be/hakyll/

```stack install hakyll```

Nope!

```
--  While building custom Setup.hs for package basement-0.0.8 using:
      /home/chronos/user/.stack/setup-exe-cache/x86_64-linux/Cabal-simple_mPHDZzAJ_2.2.0.1_ghc-8.4.3 --builddir=.stack-work/dist/x86_64-linux/Cabal-2.2.0.1 build --ghc-options " -ddump-hi -ddump-to-file -fdiagnostics-color=always"
    Process exited with code: ExitFailure 1
    Logs have been written to: /home/chronos/user/.stack/global-project/.stack-work/logs/basement-0.0.8.log

    Configuring basement-0.0.8...
    Preprocessing library for basement-0.0.8..
    hsc2hs: .stack-work/dist/x86_64-linux/Cabal-2.2.0.1/build/Basement/Terminal/Size_hsc_make: runProcess: runInteractiveProcess: exec: permission denied (Permission denied)
```