---
title: "Fedora Rawhide"
lead: ""
weight: 72410
toc: true
---

## OBS package

Our launchers are packaged on the [OBS](https://build.opensuse.org/), you have to add their repository with dnf:
```sh
sudo dnf config-manager --add-repo https://download.opensuse.org/repositories/home:Maroxy:AAT-Apps/Fedora_Rawhide/home:Maroxy:AAT-Apps.repo
```

and then install one:
```sh
sudo dnf install an-anime-game-launcher
```