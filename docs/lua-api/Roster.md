---
title: "Roster"
tags:
  - Lua-API
---

## Roster {#Roster}
*class*

Contains data about a player

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4572-L4583" target="_blank">source</a>]

**Fields**

- <span id="Roster.name"></span> `Roster.name` `string`
- <span id="Roster.playerID"></span> `Roster.playerID` [`PlayerID`](Aliases.md#PlayerID)
- <span id="Roster.teamID"></span> `Roster.teamID` [`TeamID`](Aliases.md#TeamID)
- <span id="Roster.allyTeamID"></span> `Roster.allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)
- <span id="Roster.spectator"></span> `Roster.spectator` `boolean`
- <span id="Roster.cpuUsage"></span> `Roster.cpuUsage` `number` — in order to find the progress, use: cpuUsage&0x1 if it's PC or BO, cpuUsage& 0xFE to get path res, (cpuUsage>>8)*1000 for the progress
- <span id="Roster.pingTime"></span> `Roster.pingTime` `number` — if -1, the player is pathfinding
