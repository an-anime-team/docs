---
title : "Sandbox"
lead: "This article will explain how in-launcher game sandboxing works"
weight: 4220
toc: true
---

### Where to find

1. Open the launcher settings
2. Go to the "Enhancements" tab
3. Open the "Sandbox" sub-tab

### Description

In this tab you can configure the launch of the game inside the [bubblewrap](https://github.com/containers/bubblewrap) sandbox. A similar technique is used in the Flatpak sandbox.

This option will allow you to prevent the game access to the user's personal files. The same happens when you use the launcher in Flatpak format, so this option will be interesting only to people who use the native launcher installation format - RPM, AUR and so on.

### Limitations

- It is known that now the game does not have access to the pipewire/pulsaudio sound session, so you will not be able to hear the sounds inside the game. This will be fixed in future updates.
