---
title: "Anti-Cheat"
lead: "Article related to the HSR's anti-cheat"
description: "Article related to the HSR's anti-cheat"
weight: 3220
toc: true
---

### Basic explanation

The game uses AntiCheatExpert (ACE), which is not natively supported on Linux and is designed for Windows. There is a Windows compatibility layer known as Wine which is designed to allow software written for Windows to run on Linux. But even with Wine, ACE does not work. The only way to get the game to run is to run it without ACE and use some workarounds and tricks to mimic ACE's behaviour.

The game also requires DirectX shared resources, which will probably never be fully supported by DXVK/WineD3D. WineD3D is Wine's implementation of DirectX, translating Direct3D and DirectDraw API calls into OpenGL. DXVK translates DirectX API calls to Vulkan for use with Wine. To allow the game to run, this feature must be forcibly disabled in the game's engine through heavy engineering. This may lead to some graphical glitches.

### Known security issues

TO BE ADDED: Something about lua scripts execution and ring0 access

### Patches

There are two known patches that are used to allow the game to run on Linux:

- ~~`astra`~~ (obsolete, see [First ban wave](#first-ban-wave))
- `jadeite`

### ToS violation

**Using third-party software such as patches and external launchers is illegal according to the Company's Terms of Service**. Therefore, **you may receive a ban**. It is recommended that you use a burner account for the purpose of running the game on Linux.

**Use at your own risk and only if you understand all the possible consequences**.

### History of ban waves

#### First ban wave

At March 25th, 2023, 10:52 AM UTC+8, players on the Asia server who played using the `astra` patch on Linux received a ban on their accounts for "use of third party software". As most accounts were first offenders, they were given one week suspension until June 1st. Later, players from Europe (UTC+1) and America (UTC-5) servers received their bans at their respective local time. A well-known American Linux user also reported on this situation.

The team marked the patch as unsafe three hours into the Asia server ban wave, disabling any attempts of users to automatically patch the game through the launcher. The team then scrambled to find the potential cause that triggered the bans. The team suspects that the Company pushed a Lua script that ran on the client earlier that month to check for modified game files. Potentially, the script also checked for its parent process from which the game is launched. An experimental patch was then developed in a mirror repository and was limited to a handful of testers.

Some testers that were using the experimental patch reported that they received a ban just a few days after the initial wave has concluded. That patch was also deemed unsafe and as of June 9th, 2023 23:55 UTC+8, development of that patch is now halted in favor of a new loader/runtime patcher, `jadeite`.
