---
title : "Sessions"
lead: "This article will explain how in-launcher game sessions manager works"
weight: 4210
toc: true
---

### Where to find

1. Open the launcher settings
2. Go to the "Enhancements tab
3. Open the "Game" sub-tab

### Description

In this tab, you can change in-game settings. So far, only saving the game session is available. Adding more settings is planned in the future.

The game stores information about the account from which you logged into the game in the Windows registry. Launcher [can determine](https://github.com/an-anime-team/anime-launcher-sdk/blob/7e7db30de4c02cf62b58770d2a4ee5ed0337edd4/src/games/genshin/sessions.rs ) this information and save it in a separate file.

When creating a new session inside the launcher, it will copy the information from the necessary Windows registry keys. When you start the game with the selected session, the Wine prefix registry will be updated with the account information that has been saved. Thus, if you deleted the prefix or changed the Wine version to the Proton build (which has its own, isolated prefix), the launcher will restore your session and you will not need to log in to your account again.

After exiting the game, the launcher finds the changes in the registry and updates the saved account information. This way the session will be updated according to your actions in the game.
