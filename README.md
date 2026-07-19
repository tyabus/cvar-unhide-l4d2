# cvar-unhide-l4d2 [![CI](https://github.com/tyabus/cvar-unhide-l4d2/actions/workflows/ci.yml/badge.svg)](https://github.com/tyabus/cvar-unhide-l4d2/actions/workflows/ci.yml)

This Source Engine plugin reveals all console variables (convars/cvars) that are marked as hidden or development-only. The plugin can also set console variables to arbitrary values, bypassing any hard-coded minimum/maximum. Furthermore, console commands can be 'force dispatched' regardless of whether they are marked as hidden, cheat or development-only.

A list of all console variables/commands that are made available by this plugin can be found in [cvarlist-l4d2.md](./cvarlist-l4d2.md) and [cvarlist-l4d.md](./cvarlist-l4d.md).

> 💡 For VAC safety, you must add `-insecure` to the game's launch options. The plugin will not load without this command-line argument set.

### Supported games

- Left 4 Dead 2
- Left 4 Dead

## Installation

1. **Download the latest release of the plugin**. Choose the correct release for your game and OS: \
   https://github.com/tyabus/cvar-unhide-l4d2/releases/latest
1. **Extract the contents of the ZIP to the game's mod folder.**
   - 📂 `$STEAM\steamapps\common\Left 4 Dead 2\left4dead` for L4D2
   - 📂 `$STEAM\steamapps\common\Left 4 Dead\left4dead` for L4D

   After extraction there should be an `addons` folder in the game folder, e.g. `Left 4 Dead 2\left4dead2\addons\...`
1. **Start the game from Steam.** \
   ⚠ Game client must be launched with `-insecure` in the launch options. If you don't know how to do this, take a look this [Steam Community guide](https://steamcommunity.com/sharedfiles/filedetails/?id=379782151).

## Available commands

If you installed the plugin correctly, you should now be able to use the following commands in the console:

- **cvar_set**: Set the value of a ConVar regardless of its maximum/minimum values
- **cvar_unhide_all**: Unhide all FCVAR_HIDDEN and FCVAR_DEVELOPMENTONLY convars
- **cvarlist_all**: List all ConVars. Syntax: [hidden]
- **dump_netprops**: Dump all network props. Syntax: [table depth = 1]. A table depth of -1 indicates infinite depth.
- **find_all**: Replica of "find". Ignores FCVAR_HIDDEN or FCVAR_DEVELOPMENTONLY flags
- **force_dispatch**: Dispatch a command regardless of any hidden, cheat or developmentonly flags
- **hltv_modevents**: List all HLTV mod events (game events that are recorded in demos).

Also you can add `-autounhide` to the game's launch options to automatically unhide all the hidden convars.