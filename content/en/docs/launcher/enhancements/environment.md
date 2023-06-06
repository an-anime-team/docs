---
title : "Environment"
lead: "This article will explain how in-launcher environment variables manager works"
weight: 4230
toc: true
---

## Where to find

1. Open the launcher settings
2. Go to the "Enhancements" tab
3. Open the "Environment" sub-tab

## Description

The environment settings allow you to change the startup command of the game and to specify environment variables. They can be useful for advanced users who are sure of what they are doing.

Environment variables and game command have special "keywords" which will be replaced by other values before starting the game - for example the word `%command%` will be replaced by the game starting command. You can use these to create more complex commands.

## Available keywords

### Common

The keywords available both in the game command field and in the values of environment variables.

| Keyword | Value | Example |
| - | - | - |
| `%launcher%` | Path to the launcher folder where its data is stored | `$HOME/.local/share/anime-game-launcher` |
| `%build%` | Path to Wine build (where folders `bin`, `lib` and so on are stored) | `$HOME/.local/share/anime-game-launcher/runners/lutris-GE-Proton8-7-x86_64` |
| `%prefix%` | Path to Wine prefix | `$HOME/.local/share/anime-game-launcher/prefix` |
| `%game%` | Path to the folder where the game is installed | `$HOME/.local/share/anime-game-launcher/game` |
| `%temp%` | Path to the temporary directory used by the luncher | `$HOME/.local/share/anime-game-launcher` |

### Game launcher

Keywords available only in the field with the game launch command.

| Keyword | Value | Example |
| - | - | - |
| `%bash_command%` The part of the game starting command containing the Wine executable file, as well as additional utilities like `gamemoderun` | `gamemoderun 'HOME/.local/share/anime-game-launcher/runners/lutris-GE-Proton8-7-x86_64/bin/wine64'` |
| `%windows_command%` | The part of the game starting command containing the Windows parameters. Mainly the path to the `.bat` file which runs the game and the `-window-mode exclusive` or `-screen-fullscreen 0 -popupwindow` parameters if the corresponding settings are selected | `launcher.bat -window-mode exclusive` |
| `%command%` | Full command to start the game | `%bash_command% %windows_command%` |

The final command, which executes the launch of the game, is built in the format `bash -c "%command%"`. It can be seen in the file `debug.log` - as well as the list of environment variables used to start the game.

You can use built-in Wine utilities to test the game's start command - for example, specify `%bash_command% winecfg` as a start command. This way you can quickly find errors in the command and not wait for the launch of the game itself.
