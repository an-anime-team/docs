---
title: "NixOS"
lead: ""
weight: 72300
toc: true
---

## Enable Cachix

It is recommended that you set up Cachix before the installation as not have to compile the launcher yourself.
You can do so by running
```sh
nix-shell -p cachix --run "cachix use ezkea"
```

Or alternatively in a declarative way by appending the following to your `configuration.nix`
```nix
{
  nix.settings = {
    substituters = [ "https://ezkea.cachix.org" ];
    trusted-public-keys = [ "ezkea.cachix.org-1:ioBmUbJTZIKsHmWWXPe1FSFbeVe+afhfgqgTSNd34eI=" ];
  };
}
```

## Installation

Add the following to your `configuration.nix`.
```nix
let
  aagl-gtk-on-nix = import (builtins.fetchTarball "https://github.com/ezKEa/aagl-gtk-on-nix/archive/main.tar.gz");
in
{
  imports = [
    aagl-gtk-on-nix.module
  ];

  programs.an-anime-game-launcher.enable = true;
}
```

Then install the launcher by running:
```
nixos-rebuild switch 
```

Alternatively, you can install the launcher using [home-manager](https://github.com/nix-community/home-manager) by adding the following to your `home.nix`.
```nix
let
  aagl-gtk-on-nix = import (builtins.fetchTarball "https://github.com/ezKEa/aagl-gtk-on-nix/archive/main.tar.gz");
in
{
  home.packages = [ aagl-gtk-on-nix.an-anime-game-launcher ];
}
```