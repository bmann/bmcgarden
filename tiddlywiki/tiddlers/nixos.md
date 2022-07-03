---
title: NixOS
---

NixOS Wiki: [Cheatsheet](https://nixos.wiki/wiki/Cheatsheet) - a cheat sheet and rough mapping between Ubuntu and NixOS

---

Fluffy Nuke It: [Installing Essential Software in NixOS](http://fluffynukeit.com/installing-essential-software-in-nixos/) - technically about setting up NixOS for [[Haskell]] development, but does a good job of walking through and explaining how things work.

For example, here's how to install [[git]]:

```nix-env -iA nixos.pkgs.gitAndTools.gitFull```

---