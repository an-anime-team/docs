---
title: "openSUSE Tumbleweed"
lead: ""
weight: 72420
toc: true
---

## OBS package

Our launchers are packaged on the [OBS](https://build.opensuse.org/), you have to add their repository with zypper:
```sh
sudo zypper ar -f https://download.opensuse.org/repositories/home:Maroxy:AAT-Apps/openSUSE_Tumbleweed/home:Maroxy:AAT-Apps.repo aatrepo
```

and then install one:
```sh
sudo zypper install an-anime-game-launcher
```