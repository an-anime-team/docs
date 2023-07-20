---
title: "Gentoo"
lead: ""
weight: 12200
toc: true
---

## Ebuild

Make sure that `app-eselect/eselect-repository` and `dev-vcs/git` is installed.  
After that add the launcher's overlay.
```sh
eselect repository add the-anime-team git https://github.com/an-anime-team/gentoo-ebuilds.git
```

And sync the repository.
```sh
emaint sync -r the-anime-team
```

Finally, emerge the launcher by running:
```sh
emerge --ask games-misc/an-anime-game-launcher
```
