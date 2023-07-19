---
title: "Flatpak"
lead: "Flatpak is a distribution-agnostic packaging format that makes it easy to install apps and control their access to your system"
weight: 71100
toc: true
---

## Install Flatpak

Follow the [official documentation](https://flatpak.org/setup/) for how to install it on your own system.

## Installing the launcher

Enable our repository:
```sh
flatpak remote-add --if-not-exists --user launcher.moe https://gol.launcher.moe/gol.launcher.moe.flatpakrepo
```

And install one of the launchers, for example "An Anime Game Launcher":
```sh
flatpak install launcher.moe moe.launcher.an-anime-game-launcher
```