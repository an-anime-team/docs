---
title: "Distrobox"
lead: "Distrobox is a container solution that allows you to spin up (nearly) any distribution on top of your own via Podman or Docker"
weight: 71200
toc: true
---

## Install Distrobox

Follow the [official documentation](https://github.com/89luca89/distrobox/blob/main/docs/README.md#installation) for how to install it on your own system.

Just as an example, if you were using an [immutable edition](https://www.fedoraproject.org/silverblue/) of Fedora, you would do the following:
```sh
rpm-ostree install distrobox
```
then reboot into your new deployment to start using it.

## Create a container

We assume you'll want to create an Arch Linux container
```sh
distrobox create \
	--name box-arch \
	--home "$HOME/.local/share/box-homes/arch" \
	--image docker.io/library/archlinux:latest
```

Enter the container and wait for it to complete the initialization, it may take a little while:
```sh
distrobox enter box-arch
```

## Install the launcher

After that follow the [appropriate guide](../../distro-specific/) for the distribution you installed as a container. 

## Patching

Manually patch the game, **substitute `<game_name>` with the actual name of the game** and `<patch_number>` with the latest patch (e.g. game version 3.7.0 -> patch version 370):
```sh
cd "$HOME/.local/share/anime-game-launcher/<game_name>"
sh "$HOME/.local/share/anime-game-launcher/patch/<patch_number>/patch.sh"
```
Open a new terminal with your host shell and edit `/etc/hosts`:
```sh
sudo nano /etc/hosts
```

Paste the output of the `patch.sh` script within `-- Adding analytics servers` and `-- Failed` at the end of the file, it should look something like this:
```
# anime game logging servers (do not remove!)
0.0.0.0 <some-domain>.<com>
```
Finally, from within the launcher, **disable the XLUA patch** option to be able to launch the game.