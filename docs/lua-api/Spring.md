---
title: "Spring"
tags:
  - Lua-API
---

## Spring {#Spring}
*table*

**Members**

### Spring.CallAsTeam {#Spring.CallAsTeam}
*function*

Calls a function from given team's PoV. In particular this makes callouts obey that team's visibility rules.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2544-L2551" target="_blank">source</a>]

```lua
Spring.CallAsTeam(TeamID, fun(...), [any, ]*) -> any ...
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID) — Team ID.
- `func` `fun(...)` — The function to call.
- `...` `any` — Arguments to pass to the function.

**Returns**

- `The` `any ...` — return values of the function.

### Spring.CallAsTeam (overload 1) {#Spring.CallAsTeam-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2552-L2558" target="_blank">source</a>]

```lua
Spring.CallAsTeam(CallAsTeamOptions, fun(...), [any, ]*) -> any ...
```

**Parameters**

- `options` [`CallAsTeamOptions`](CallAsTeamOptions.md#CallAsTeamOptions) — Options.
- `func` `fun(...)` — The function to call.
- `...` `any` — Arguments to pass to the function.

**Returns**

- `The` `any ...` — return values of the function.

### Spring.GetMetalMapSize {#Spring.GetMetalMapSize}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaMetalMap.cpp#L34-L38" target="_blank">source</a>]

```lua
Spring.GetMetalMapSize() -> integer, integer
```

**Returns**

- `x` `integer` — X coordinate in worldspace / [Game.metalMapSquareSize](Game.md#Game.metalMapSquareSize).
- `z` `integer` — Z coordinate in worldspace / [Game.metalMapSquareSize](Game.md#Game.metalMapSquareSize).

### Spring.GetMetalAmount {#Spring.GetMetalAmount}
*function*

Returns the amount of metal on a single square.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaMetalMap.cpp#L47-L53" target="_blank">source</a>]

```lua
Spring.GetMetalAmount(integer, integer) -> number
```

**Parameters**

- `x` `integer` — X coordinate in worldspace / [Game.metalMapSquareSize](Game.md#Game.metalMapSquareSize).
- `z` `integer` — Z coordinate in worldspace / [Game.metalMapSquareSize](Game.md#Game.metalMapSquareSize).

**Returns**

- `amount` `number`

### Spring.SetMetalAmount {#Spring.SetMetalAmount}
*function*

Sets the amount of metal on a single square.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaMetalMap.cpp#L64-L71" target="_blank">source</a>]

```lua
Spring.SetMetalAmount(integer, integer, number) -> nil
```

**Parameters**

- `x` `integer` — X coordinate in worldspace / [Game.metalMapSquareSize](Game.md#Game.metalMapSquareSize).
- `z` `integer` — Z coordinate in worldspace / [Game.metalMapSquareSize](Game.md#Game.metalMapSquareSize).
- `metalAmount` `number` — must be between 0 and 255*maxMetal (with maxMetal from the .smd or mapinfo.lua).

**Returns**

- `nil`

### Spring.GetMetalExtraction {#Spring.GetMetalExtraction}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaMetalMap.cpp#L83-L88" target="_blank">source</a>]

```lua
Spring.GetMetalExtraction(integer, integer) -> number
```

**Parameters**

- `x` `integer` — X coordinate in worldspace / [Game.metalMapSquareSize](Game.md#Game.metalMapSquareSize).
- `z` `integer` — Z coordinate in worldspace / [Game.metalMapSquareSize](Game.md#Game.metalMapSquareSize).

**Returns**

- `extraction` `number`

### Spring.RequestPath {#Spring.RequestPath}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaPathFinder.cpp#L214-L225" target="_blank">source</a>]

```lua
Spring.RequestPath((integer|string), number, number, number, number, number, number, number?) -> userdata?
```

**Parameters**

- `moveID` `(integer|string)`
- `startX` `number`
- `startY` `number`
- `startZ` `number`
- `endX` `number`
- `endY` `number`
- `endZ` `number`
- `radius` `number?`

**Returns**

- `path` `userdata?`

### Spring.InitPathNodeCostsArray {#Spring.InitPathNodeCostsArray}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaPathFinder.cpp#L265-L271" target="_blank">source</a>]

```lua
Spring.InitPathNodeCostsArray(integer, integer, integer) -> boolean
```

**Parameters**

- `overlayIndex` `integer`
- `sizeX` `integer`
- `sizeZ` `integer`

**Returns**

- `success` `boolean`

### Spring.FreePathNodeCostsArray {#Spring.FreePathNodeCostsArray}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaPathFinder.cpp#L304-L308" target="_blank">source</a>]

```lua
Spring.FreePathNodeCostsArray(integer) -> boolean
```

**Parameters**

- `overlayIndex` `integer`

**Returns**

- `success` `boolean`

### Spring.SetPathNodeCosts {#Spring.SetPathNodeCosts}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaPathFinder.cpp#L342-L346" target="_blank">source</a>]

```lua
Spring.SetPathNodeCosts(integer) -> boolean
```

**Parameters**

- `overlayIndex` `integer`

**Returns**

- `success` `boolean`

### Spring.GetPathNodeCosts {#Spring.GetPathNodeCosts}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaPathFinder.cpp#L371-L375" target="_blank">source</a>]

```lua
Spring.GetPathNodeCosts(integer) -> (boolean|table)
```

**Parameters**

- `overlayIndex` `integer`

**Returns**

- `costs` `(boolean|table)`

### Spring.SetPathNodeCost {#Spring.SetPathNodeCost}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaPathFinder.cpp#L407-L413" target="_blank">source</a>]

```lua
Spring.SetPathNodeCost(integer, integer, number) -> boolean
```

**Parameters**

- `overlayIndex` `integer`
- `costIndex` `integer` — 0-based index in the overlay
- `cost` `number`

**Returns**

- `success` `boolean`

### Spring.GetPathNodeCost {#Spring.GetPathNodeCost}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaPathFinder.cpp#L444-L449" target="_blank">source</a>]

```lua
Spring.GetPathNodeCost(integer, integer) -> number
```

**Parameters**

- `nodeX` `integer` — Heightmap node X coordinate
- `nodeZ` `integer` — Heightmap node Z coordinate

**Returns**

- `cost` `number`

### Spring.SetAlly {#Spring.SetAlly}
*function*

Changes the value of the (one-sided) alliance between: firstAllyTeamID -> secondAllyTeamID.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L887-L894" target="_blank">source</a>]

```lua
Spring.SetAlly(AllyTeamID, AllyTeamID, boolean) -> nil
```

**Parameters**

- `firstAllyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `secondAllyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `ally` `boolean`

**Returns**

- `nil`

### Spring.SetAllyTeamStartBox {#Spring.SetAllyTeamStartBox}
*function*

Changes the start box position of an allyTeam.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L910-L919" target="_blank">source</a>]

```lua
Spring.SetAllyTeamStartBox(AllyTeamID, number, number, number, number) -> nil
```

**Parameters**

- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `xMin` `number` — left start box boundary (elmos)
- `zMin` `number` — top start box boundary (elmos)
- `xMax` `number` — right start box boundary (elmos)
- `zMax` `number` — bottom start box boundary (elmos)

**Returns**

- `nil`

### Spring.AssignPlayerToTeam {#Spring.AssignPlayerToTeam}
*function*

Assigns a player to a team.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L942-L948" target="_blank">source</a>]

```lua
Spring.AssignPlayerToTeam(PlayerID, TeamID) -> nil
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `nil`

### Spring.SetTeamStartPosition {#Spring.SetTeamStartPosition}
*function*

Set the starting position of a team.

If the position argument is outside the team's startbox, the position is clamped.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L969-L979" target="_blank">source</a>]

```lua
Spring.SetTeamStartPosition(TeamID, number, number, number) -> boolean
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `x` `number` — left position (elmos)
- `y` `number` — vertical position (elmos)
- `z` `number` — top position (elmos)

**Returns**

- `success` `boolean` — true if the position was set, false if the teamID is invalid

### Spring.SetPlayerReadyState {#Spring.SetPlayerReadyState}
*function*

Set the ready state of a player.

Use to mark a player (un)ready in the pregame phase.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1002-L1010" target="_blank">source</a>]

```lua
Spring.SetPlayerReadyState(PlayerID, boolean) -> boolean
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `ready` `boolean`

**Returns**

- `success` `boolean` — true if the state was set, false if the playerID was invalid

### Spring.SetGlobalLos {#Spring.SetGlobalLos}
*function*

Changes access to global line of sight for a team and its allies.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1027-L1033" target="_blank">source</a>]

```lua
Spring.SetGlobalLos(AllyTeamID, boolean) -> nil
```

**Parameters**

- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `globallos` `boolean`

**Returns**

- `nil`

### Spring.SetCheatingEnabled {#Spring.SetCheatingEnabled}
*function*

Changes whether activating cheats is allowed.
Note that already activated cheats (e.g. god mode) stay active even if you disallow activating.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1045-L1051" target="_blank">source</a>]

```lua
Spring.SetCheatingEnabled(boolean) -> nil
```

**Parameters**

- `cheatsEnabled` `boolean`

**Returns**

- `nil`

### Spring.SetGodMode {#Spring.SetGodMode}
*function*

Toggles 'god mode', i.e. whether control of teams other than one's own is allowed.
Affects all teams.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1058-L1065" target="_blank">source</a>]

```lua
Spring.SetGodMode(boolean?, boolean?) -> nil
```

**Parameters**

- `controlAllies` `boolean?`
- `controlEnemies` `boolean?`

**Returns**

- `nil`

### Spring.KillTeam {#Spring.KillTeam}
*function*

Will declare a team to be dead (no further orders can be assigned to such teams units).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1085-L1093" target="_blank">source</a>]

Gaia team cannot be killed.

```lua
Spring.KillTeam(TeamID) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `nil`

### Spring.GameOver {#Spring.GameOver}
*function*

Declare game over.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1116-L1125" target="_blank">source</a>]

```lua
Spring.GameOver(AllyTeamID[]) -> integer
```

**Parameters**

- `winningAllyTeamIDs` `AllyTeamID[]` — A list of winning ally team IDs.

Pass multiple winners to declare a draw.
Pass no arguments if undecided (e.g. when dropped from the host).

**Returns**

- `teams` `integer` — Number of accepted (valid) ally teams.

### Spring.SetTidal {#Spring.SetTidal}
*function*

Set tidal strength

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1162-L1167" target="_blank">source</a>]

```lua
Spring.SetTidal(number?) -> nil
```

**Parameters**

- `strength` `number?`

**Returns**

- `nil`

### Spring.SetWind {#Spring.SetWind}
*function*

Set wind strength

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1175-L1181" target="_blank">source</a>]

```lua
Spring.SetWind(number?, number?) -> nil
```

**Parameters**

- `minStrength` `number?`
- `maxStrength` `number?`

**Returns**

- `nil`

### Spring.AddTeamResource {#Spring.AddTeamResource}
*function*

Adds metal or energy resources to the specified team.
Counts as production in post-game graph statistics.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1188-L1196" target="_blank">source</a>]

```lua
Spring.AddTeamResource(TeamID, ResourceName, number) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `type` [`ResourceName`](Aliases.md#ResourceName)
- `amount` `number`

**Returns**

- `nil`

### Spring.UseTeamResource {#Spring.UseTeamResource}
*function*

Consumes metal or energy resources of the specified team.
Counts as usage in post-game graph statistics.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1225-L1235" target="_blank">source</a>]

```lua
Spring.UseTeamResource(TeamID, ResourceName, number) -> boolean
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `type` [`ResourceName`](Aliases.md#ResourceName) — Resource type.
- `amount` `number` — Amount of resource to use.

**Returns**

- `hadEnough` `boolean`

### Spring.UseTeamResource (overload 1) {#Spring.UseTeamResource-1}
*function*

Consumes metal and/or energy resources of the specified team.
Counts as usage in post-game graph statistics.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1236-L1245" target="_blank">source</a>]

```lua
Spring.UseTeamResource(TeamID, ResourceUsage) -> boolean
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `amount` [`ResourceUsage`](Aliases.md#ResourceUsage)

**Returns**

- `hadEnough` `boolean`

### Spring.SetTeamResource {#Spring.SetTeamResource}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1322-L1328" target="_blank">source</a>]

```lua
Spring.SetTeamResource(TeamID, (ResourceName|StorageName), number) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `resource` `(ResourceName|StorageName)`
- `amount` `number`

**Returns**

- `nil`

### Spring.SetTeamShareLevel {#Spring.SetTeamShareLevel}
*function*

Changes the resource amount for a team beyond which resources aren't stored but transferred to other allied teams if possible.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1372-L1379" target="_blank">source</a>]

```lua
Spring.SetTeamShareLevel(TeamID, ResourceName, number) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `type` [`ResourceName`](Aliases.md#ResourceName)
- `amount` `number`

**Returns**

- `nil`

### Spring.AddTeamResourceExcessStats {#Spring.AddTeamResourceExcessStats}
*function*

Records resource excess for a team without moving resources.

The engine normally tracks excess, but if you use `gadget:ResourceExcess`
to handle it manually it's now also up to you to track stats.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1409-L1420" target="_blank">source</a>]

```lua
Spring.AddTeamResourceExcessStats(TeamID, ResourceName, number) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `type` [`ResourceName`](Aliases.md#ResourceName)
- `excess` `number` — Amount wasted this tick.

**Returns**

- `nil`

### Spring.ShareTeamResource {#Spring.ShareTeamResource}
*function*

Transfers resources between two teams.
Transfers directly, without involving AllowResourceTransfer callin.
Approximately equivalent to doing Use and Add for the sender and receiver,
the difference being that it counts to sent/received stats rather than
used/produced in end-game statistics graphs.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1455-L1467" target="_blank">source</a>]

```lua
Spring.ShareTeamResource(TeamID, TeamID, ResourceName, number) -> nil
```

**Parameters**

- `teamID_src` [`TeamID`](Aliases.md#TeamID)
- `teamID_recv` [`TeamID`](Aliases.md#TeamID)
- `type` [`ResourceName`](Aliases.md#ResourceName)
- `amount` `number`

**Returns**

- `nil`

### Spring.SetGameRulesParam {#Spring.SetGameRulesParam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1614-L1620" target="_blank">source</a>]

```lua
Spring.SetGameRulesParam(string, (number|string|boolean)?, losAccess?) -> nil
```

**Parameters**

- `paramName` `string`
- `paramValue` `(number|string|boolean)?` — numeric paramValues in quotes will be converted to number.
- `losAccess` `losAccess?`

**Returns**

- `nil`

### Spring.SetTeamRulesParam {#Spring.SetTeamRulesParam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1628-L1635" target="_blank">source</a>]

```lua
Spring.SetTeamRulesParam(TeamID, string, (number|string|boolean)?, losAccess?) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `paramName` `string`
- `paramValue` `(number|string|boolean)?` — numeric paramValues in quotes will be converted to number.
- `losAccess` `losAccess?`

**Returns**

- `nil`

### Spring.SetPlayerRulesParam {#Spring.SetPlayerRulesParam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1646-L1653" target="_blank">source</a>]

```lua
Spring.SetPlayerRulesParam(PlayerID, string, (number|string|boolean)?, losAccess?) -> nil
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `paramName` `string`
- `paramValue` `(number|string|boolean)?` — numeric paramValues in quotes will be converted to number.
- `losAccess` `losAccess?`

**Returns**

- `nil`

### Spring.SetUnitRulesParam {#Spring.SetUnitRulesParam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1669-L1677" target="_blank">source</a>]

```lua
Spring.SetUnitRulesParam(UnitID, string, (number|string|boolean)?, losAccess?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `paramName` `string`
- `paramValue` `(number|string|boolean)?` — numeric paramValues in quotes will be converted to number.
- `losAccess` `losAccess?`

**Returns**

- `nil`

### Spring.SetFeatureRulesParam {#Spring.SetFeatureRulesParam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1690-L1697" target="_blank">source</a>]

```lua
Spring.SetFeatureRulesParam(FeatureID, string, (number|string|boolean)?, losAccess?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `paramName` `string`
- `paramValue` `(number|string|boolean)?` — numeric paramValues in quotes will be converted to number.
- `losAccess` `losAccess?`

**Returns**

- `nil`

### Spring.CallCOBScript {#Spring.CallCOBScript}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1754-L1761" target="_blank">source</a>]

```lua
Spring.CallCOBScript(UnitID, (integer|string)?, integer, [any, ]*) -> integer ...
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `funcName` `(integer|string)?` — Function ID or name.
- `retArgs` `integer` — Number of values to return.
- `...` `any` — Arguments

**Returns**

- `integer ...`

### Spring.GetCOBScriptID {#Spring.GetCOBScriptID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1814-L1819" target="_blank">source</a>]

```lua
Spring.GetCOBScriptID(UnitID, string) -> integer?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `funcName` `string`

**Returns**

- `funcID` `integer?`

### Spring.CreateUnit {#Spring.CreateUnit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1853-L1870" target="_blank">source</a>]

**See:** [Spring.DestroyUnit](Spring.md#Spring.DestroyUnit)

```lua
Spring.CreateUnit((string|integer), number, number, number, Facing, TeamID?, boolean?, boolean?, UnitID?, UnitID?) -> UnitID?
```

**Parameters**

- `unitDef` `(string|integer)` — UnitDef name or ID.
- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `facing` [`Facing`](Aliases.md#Facing)
- `teamID` `TeamID?`
- `build` `boolean?` — (Default: `false`) The unit is created in "being built" state with zero `buildProgress`.
- `flattenGround` `boolean?` — (Default: `true`) The unit flattens ground, if it normally does so.
- `unitID` `UnitID?` — Request a specific unitID.
- `builderID` `UnitID?`

**Returns**

- `unitID` `UnitID?` — The ID of the created unit, or `nil` if the unit could not be created.

### Spring.DestroyUnit {#Spring.DestroyUnit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1953-L1962" target="_blank">source</a>]

**See:** [Spring.CreateUnit](Spring.md#Spring.CreateUnit)

```lua
Spring.DestroyUnit(UnitID, boolean?, boolean?, UnitID?, boolean?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `selfd` `boolean?` — (Default: `false`) makes the unit act like it self-destructed.
- `reclaimed` `boolean?` — (Default: `false`) don't show any DeathSequences, don't leave a wreckage. This does not give back the resources to the team!
- `attackerID` `UnitID?`
- `cleanupImmediately` `boolean?` — (Default: `false`) stronger version of reclaimed, removes the unit unconditionally and makes its ID available for immediate reuse (otherwise it takes a few frames)

**Returns**

- `nil`

### Spring.TransferUnit {#Spring.TransferUnit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1997-L2004" target="_blank">source</a>]

```lua
Spring.TransferUnit(UnitID, TeamID, boolean?, boolean?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `newTeamID` [`TeamID`](Aliases.md#TeamID)
- `given` `boolean?` — (Default: `true`) if false, the unit is captured.
- `adjustUnitLimit` `boolean?` — (Default: `false`) if true, also transfer the limit slot

**Returns**

- `successfulTransfer` `boolean`

### Spring.TransferTeamMaxUnits {#Spring.TransferTeamMaxUnits}
*function*

Transfer capacity of units from one team to another

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2056-L2068" target="_blank">source</a>]

There are some conditions that must be satisfied for the operation to be successful:
- `transferAmnt` must be lower or equal than the origin team current maxunits (can't transfer limit team does not have available)
- `transferAmnt` must be lower than origin team maxunits - currentunitscount (can't transfer limit if origin team would be already over the limit after transfer)

```lua
Spring.TransferTeamMaxUnits(TeamID, TeamID, integer) -> boolean
```

**Parameters**

- `fromTeamID` [`TeamID`](Aliases.md#TeamID)
- `newTeamID` [`TeamID`](Aliases.md#TeamID)
- `transferAmnt` `integer`

**Returns**

- `successfulTransfer` `boolean` — Whether the max unit limit was successfully transferred.

### Spring.SetUnitCosts {#Spring.SetUnitCosts}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2100-L2105" target="_blank">source</a>]

```lua
Spring.SetUnitCosts(UnitID, table<number,number>) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `where` `table<number,number>` — keys and values are, respectively and in this order: buildTime=amount, metalCost=amount, energyCost=amount

**Returns**

- `nil`

### Spring.SetUnitResourcing {#Spring.SetUnitResourcing}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2229-L2235" target="_blank">source</a>]

```lua
Spring.SetUnitResourcing(UnitID, string, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `res` `string`
- `amount` `number`

**Returns**

- `nil`

### Spring.SetUnitResourcing (overload 1) {#Spring.SetUnitResourcing-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2237-L2242" target="_blank">source</a>]

```lua
Spring.SetUnitResourcing(UnitID, table<string,number>) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `res` `table<string,number>` — keys are: "[u|c][u|m][m|e]" unconditional | conditional, use | make, metal | energy. Values are amounts

**Returns**

- `nil`

### Spring.SetUnitStorage {#Spring.SetUnitStorage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2275-L2280" target="_blank">source</a>]

```lua
Spring.SetUnitStorage(UnitID, string, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `res` `string`
- `amount` `number`

### Spring.SetUnitStorage (overload 1) {#Spring.SetUnitStorage-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2282-L2286" target="_blank">source</a>]

```lua
Spring.SetUnitStorage(UnitID, ResourceUsage) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `res` [`ResourceUsage`](Aliases.md#ResourceUsage) — keys are: "[m|e]" metal | energy. Values are amounts

### Spring.SetUnitTooltip {#Spring.SetUnitTooltip}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2314-L2319" target="_blank">source</a>]

```lua
Spring.SetUnitTooltip(UnitID, string) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `tooltip` `string`

**Returns**

- `nil`

### Spring.SetUnitHealth {#Spring.SetUnitHealth}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2346-L2359" target="_blank">source</a>]

Note, if your game's custom shading framework doesn't support reverting into nanoframes
then reverting into nanoframes via the "build" tag will fail to render properly.

**See:** [SetUnitHealthAmounts](SetUnitHealthAmounts.md#SetUnitHealthAmounts)

```lua
Spring.SetUnitHealth(UnitID, (number|SetUnitHealthAmounts)) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `health` `(number|SetUnitHealthAmounts)` — If a number, sets the units health
to that value. Pass a table to update health, capture progress, paralyze
damage, and build progress.

**Returns**

- `nil`

### Spring.SetUnitMaxHealth {#Spring.SetUnitMaxHealth}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2411-L2416" target="_blank">source</a>]

```lua
Spring.SetUnitMaxHealth(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `maxHealth` `number`

**Returns**

- `nil`

### Spring.SetUnitStockpile {#Spring.SetUnitStockpile}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2430-L2436" target="_blank">source</a>]

```lua
Spring.SetUnitStockpile(UnitID, integer?, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `stockpile` `integer?`
- `buildPercent` `number?`

**Returns**

- `nil`

### Spring.SetUnitUseWeapons {#Spring.SetUnitUseWeapons}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2571-L2578" target="_blank">source</a>]

```lua
Spring.SetUnitUseWeapons(UnitID, number?, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `forceUseWeapons` `number?`
- `allowUseWeapons` `number?`

**Returns**

- `nil`

### Spring.SetUnitWeaponState {#Spring.SetUnitWeaponState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2591-L2597" target="_blank">source</a>]

```lua
Spring.SetUnitWeaponState(UnitID, integer, WeaponState) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `states` [`WeaponState`](WeaponState.md#WeaponState)

**Returns**

- `nil`

### Spring.SetUnitWeaponState (overload 1) {#Spring.SetUnitWeaponState-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2599-L2606" target="_blank">source</a>]

```lua
Spring.SetUnitWeaponState(UnitID, integer, string, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `key` `string`
- `value` `number`

**Returns**

- `nil`

### Spring.SetUnitWeaponDamages {#Spring.SetUnitWeaponDamages}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2727-L2733" target="_blank">source</a>]

```lua
Spring.SetUnitWeaponDamages(UnitID, (integer|"selfDestruct"|"explode"), WeaponDamages) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `(integer|"selfDestruct"|"explode")`
- `damages` [`WeaponDamages`](WeaponDamages.md#WeaponDamages)

**Returns**

- `nil`

### Spring.SetUnitWeaponDamages (overload 1) {#Spring.SetUnitWeaponDamages-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2734-L2741" target="_blank">source</a>]

```lua
Spring.SetUnitWeaponDamages(UnitID, (integer|"selfDestruct"|"explode"), string, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `(integer|"selfDestruct"|"explode")`
- `key` `string`
- `value` `number`

**Returns**

- `nil`

### Spring.SetUnitMaxRange {#Spring.SetUnitMaxRange}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2787-L2792" target="_blank">source</a>]

```lua
Spring.SetUnitMaxRange(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `maxRange` `number`

**Returns**

- `nil`

### Spring.SetUnitExperience {#Spring.SetUnitExperience}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2805-L2812" target="_blank">source</a>]

**See:** [Spring.GetUnitExperience](Spring.md#Spring.GetUnitExperience)

```lua
Spring.SetUnitExperience(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `experience` `number`

**Returns**

- `nil`

### Spring.AddUnitExperience {#Spring.AddUnitExperience}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2824-L2831" target="_blank">source</a>]

**See:** [Spring.GetUnitExperience](Spring.md#Spring.GetUnitExperience)

```lua
Spring.AddUnitExperience(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `deltaExperience` `number` — Can be negative to subtract, but the unit will never have negative total afterwards

**Returns**

- `nil`

### Spring.SetUnitArmored {#Spring.SetUnitArmored}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2845-L2851" target="_blank">source</a>]

```lua
Spring.SetUnitArmored(UnitID, boolean?, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `armored` `boolean?`
- `armorMultiple` `number?`

**Returns**

- `nil`

### Spring.SetUnitLosMask {#Spring.SetUnitLosMask}
*function*

Set visibility status mask for a unit and team

Use this to allow or disallow a unit from having its visibility status
against a certain team updated by the engine.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2931-L2943" target="_blank">source</a>]

**See:** [Spring.SetUnitLosState](Spring.md#Spring.SetUnitLosState)

```lua
Spring.SetUnitLosMask(UnitID, AllyTeamID, (LosTable|LosMask|integer)) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `allyTeam` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `losTypes` `(LosTable|LosMask|integer)` — A bitmask of [LosMask](LosMask.md#LosMask) bits or a
table. True bits disable engine updates to visibility.

### Spring.SetUnitLosState {#Spring.SetUnitLosState}
*function*

Set current visibility status for a unit and team

Note this state will not be persisted if the visibility state is not masked.

Use it to change visibility state, once you set the unit to not receive
engine visibility updates.

A few notes on certain bits:

- `contradar`: True when the unit entered los at some point, remains set
until radar is lost. Useful for tracking the unit type in radar, if you
lost los you still know what unit type that radar dot refers to.
- `prevlos`: True when the unit has entered los at least once, useful for
tracking building locations (controls whether a ghost appears or not in
the location)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2968-L2990" target="_blank">source</a>]

**See:** [Spring.SetUnitLosMask](Spring.md#Spring.SetUnitLosMask)

```lua
Spring.SetUnitLosState(UnitID, AllyTeamID, (LosTable|LosMask|integer)) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `allyTeam` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `losTypes` `(LosTable|LosMask|integer)` — A bitmask of [LosMask](LosMask.md#LosMask) bits or a
table

### Spring.SetUnitCloak {#Spring.SetUnitCloak}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3012-L3030" target="_blank">source</a>]

If the 2nd argument is a number, the value works like this:
1:=normal cloak
2:=for free cloak (cost no E)
3:=for free + no decloaking (except the unit is stunned)
4:=ultimate cloak (no ecost, no decloaking, no stunned decloak)

The decloak distance is only changed:
- if the 3th argument is a number or a boolean.
- if the boolean is false it takes the default decloak distance for that unitdef,
- if the boolean is true it takes the absolute value of it.

```lua
Spring.SetUnitCloak(UnitID, (boolean|number)?, (boolean|number)?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `cloak` `(boolean|number)?`
- `cloakArg` `(boolean|number)?`

**Returns**

- `nil`

### Spring.SetUnitStealth {#Spring.SetUnitStealth}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3061-L3066" target="_blank">source</a>]

```lua
Spring.SetUnitStealth(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `stealth` `boolean`

**Returns**

- `nil`

### Spring.SetUnitSonarStealth {#Spring.SetUnitSonarStealth}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3079-L3084" target="_blank">source</a>]

```lua
Spring.SetUnitSonarStealth(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `sonarStealth` `boolean`

**Returns**

- `nil`

### Spring.SetUnitSeismicSignature {#Spring.SetUnitSeismicSignature}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3096-L3101" target="_blank">source</a>]

```lua
Spring.SetUnitSeismicSignature(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `seismicSignature` `number`

**Returns**

- `nil`

### Spring.SetUnitLeavesGhost {#Spring.SetUnitLeavesGhost}
*function*

Set whether unit leaves static radar ghosts.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3112-L3119" target="_blank">source</a>]

```lua
Spring.SetUnitLeavesGhost(boolean, boolean?) -> nil
```

**Parameters**

- `leavesGhost` `boolean`
- `leaveDeadGhost` `boolean?` — (Default: `false`) leave a dead ghost behind if disabling and the unit had a live static ghost.

### Spring.SetUnitAlwaysVisible {#Spring.SetUnitAlwaysVisible}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3134-L3139" target="_blank">source</a>]

```lua
Spring.SetUnitAlwaysVisible(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `alwaysVisible` `boolean`

**Returns**

- `nil`

### Spring.SetUnitUseAirLos {#Spring.SetUnitUseAirLos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3146-L3152" target="_blank">source</a>]

```lua
Spring.SetUnitUseAirLos(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `useAirLos` `boolean`

**Returns**

- `nil`

### Spring.SetUnitMetalExtraction {#Spring.SetUnitMetalExtraction}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3159-L3165" target="_blank">source</a>]

```lua
Spring.SetUnitMetalExtraction(UnitID, number, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `depth` `number` — corresponds to metal extraction rate
- `range` `number?` — similar to "extractsMetal" in unitDefs.

**Returns**

- `nil`

### Spring.SetUnitHarvestStorage {#Spring.SetUnitHarvestStorage}
*function*

See also harvestStorage UnitDef tag.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3186-L3192" target="_blank">source</a>]

```lua
Spring.SetUnitHarvestStorage(UnitID, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `metal` `number?`

**Returns**

- `nil`

### Spring.SetUnitBuildParams {#Spring.SetUnitBuildParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3207-L3214" target="_blank">source</a>]

```lua
Spring.SetUnitBuildParams(UnitID, string, (number|boolean)?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `paramName` `string` — one of `buildRange`|`buildDistance`|`buildRange3D`
- `value` `(number|boolean)?` — boolean when `paramName` is `buildRange3D`, otherwise number.

**Returns**

- `nil`

### Spring.SetUnitBuildSpeed {#Spring.SetUnitBuildSpeed}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3241-L3250" target="_blank">source</a>]

```lua
Spring.SetUnitBuildSpeed(UnitID, number, number?, number?, number?, number?) -> nil
```

**Parameters**

- `builderID` [`UnitID`](Aliases.md#UnitID)
- `buildSpeed` `number`
- `repairSpeed` `number?`
- `reclaimSpeed` `number?`
- `captureSpeed` `number?`
- `terraformSpeed` `number?`

**Returns**

- `nil`

### Spring.SetUnitNanoPieces {#Spring.SetUnitNanoPieces}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3292-L3302" target="_blank">source</a>]

This saves a lot of engine calls, by replacing: function script.QueryNanoPiece() return currentpiece end
Use it!

```lua
Spring.SetUnitNanoPieces(UnitID, table) -> nil
```

**Parameters**

- `builderID` [`UnitID`](Aliases.md#UnitID)
- `pieces` `table`

**Returns**

- `nil`

### Spring.SetUnitBlocking {#Spring.SetUnitBlocking}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3352-L3363" target="_blank">source</a>]

```lua
Spring.SetUnitBlocking(UnitID, boolean?, boolean?, boolean?, boolean?, boolean?, boolean?, boolean?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `isBlocking` `boolean?` — If `true` add this unit to the `GroundBlockingMap`, but only if it collides with solid objects (or is being set to collide with the `isSolidObjectCollidable` argument). If `false`, remove this unit from the `GroundBlockingMap`. No change if `nil`.
- `isSolidObjectCollidable` `boolean?` — Enable or disable collision with solid objects, or no change if `nil`.
- `isProjectileCollidable` `boolean?` — Enable or disable collision with projectiles, or no change if `nil`.
- `isRaySegmentCollidable` `boolean?` — Enable or disable collision with ray segments, or no change if `nil`.
- `crushable` `boolean?` — Enable or disable crushable, or no change if `nil`.
- `blockEnemyPushing` `boolean?` — Enable or disable blocking enemy pushing, or no change if `nil`.
- `blockHeightChanges` `boolean?` — Enable or disable blocking height changes, or no change if `nil`.

**Returns**

- `isBlocking` `boolean`

### Spring.SetUnitCrashing {#Spring.SetUnitCrashing}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3370-L3375" target="_blank">source</a>]

```lua
Spring.SetUnitCrashing(UnitID, boolean?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `crashing` `boolean?`

**Returns**

- `success` `boolean`

### Spring.SetUnitShieldState {#Spring.SetUnitShieldState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3405-L3412" target="_blank">source</a>]

```lua
Spring.SetUnitShieldState(UnitID, integer?, boolean?, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponID` `integer?` — (Default: `-1`)
- `enabled` `boolean?`
- `power` `number?`

**Returns**

- `nil`

### Spring.SetUnitShieldRechargeDelay {#Spring.SetUnitShieldRechargeDelay}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3443-L3449" target="_blank">source</a>]

```lua
Spring.SetUnitShieldRechargeDelay(UnitID, integer?, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponID` `integer?` — (optional if the unit only has one shield)
- `rechargeTime` `number?` — (in seconds; emulates a regular hit if nil)

**Returns**

- `nil`

### Spring.SetUnitFlanking {#Spring.SetUnitFlanking}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3480-L3488" target="_blank">source</a>]

```lua
Spring.SetUnitFlanking(UnitID, string, number, number?, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `type` `string` — "dir"|"minDamage"|"maxDamage"|"moveFactor"|"mode"
- `arg1` `number` — x|minDamage|maxDamage|moveFactor|mode
- `y` `number?` — only when type is "dir"
- `z` `number?` — only when type is "dir"

**Returns**

- `nil`

### Spring.SetUnitPhysicalStateBit {#Spring.SetUnitPhysicalStateBit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3527-L3532" target="_blank">source</a>]

```lua
Spring.SetUnitPhysicalStateBit(UnitID, ) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `Physical`

**Returns**

- `nil`

### Spring.GetUnitPhysicalState {#Spring.GetUnitPhysicalState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3546-L3550" target="_blank">source</a>]

```lua
Spring.GetUnitPhysicalState(UnitID) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `physicalState` `integer` — Unit's PhysicalState bitmask

### Spring.SetUnitNeutral {#Spring.SetUnitNeutral}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3569-L3576" target="_blank">source</a>]

```lua
Spring.SetUnitNeutral(UnitID, boolean) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `neutral` `boolean`

**Returns**

- `setNeutral` `boolean?`

### Spring.SetUnitTarget {#Spring.SetUnitTarget}
*function*

Defines a unit's target.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3589-L3599" target="_blank">source</a>]

```lua
Spring.SetUnitTarget(UnitID, UnitID?, boolean?, boolean?, boolean?, integer?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `enemyUnitID` `UnitID?` — when nil drops the units current target.
- `dgun` `boolean?` — (Default: `false`)
- `userTarget` `boolean?` — (Default: `false`)
- `dontForceTarget` `boolean?`
- `weaponNum` `integer?` — (Default: `-1`)

**Returns**

- `success` `boolean`

### Spring.SetUnitTarget (overload 1) {#Spring.SetUnitTarget-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3601-L3612" target="_blank">source</a>]

```lua
Spring.SetUnitTarget(UnitID, number?, number?, number?, boolean?, boolean?, boolean?, integer?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `x` `number?` — when nil or not passed it will drop target and ignore other parameters
- `y` `number?`
- `z` `number?`
- `dgun` `boolean?` — (Default: `false`)
- `userTarget` `boolean?` — (Default: `false`)
- `dontForceTarget` `boolean?`
- `weaponNum` `integer?` — (Default: `-1`)

**Returns**

- `success` `boolean`

### Spring.SetUnitMidAndAimPos {#Spring.SetUnitMidAndAimPos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3671-L3682" target="_blank">source</a>]

```lua
Spring.SetUnitMidAndAimPos(UnitID, number, number, number, number, number, number, boolean?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `mpX` `number` — new middle positionX of unit
- `mpY` `number` — new middle positionY of unit
- `mpZ` `number` — new middle positionZ of unit
- `apX` `number` — new positionX that enemies aim at on this unit
- `apY` `number` — new positionY that enemies aim at on this unit
- `apZ` `number` — new positionZ that enemies aim at on this unit
- `relative` `boolean?` — (Default: `false`) are the new coordinates relative to world (false) or unit (true) coordinates? Also, note that apy is inverted!

**Returns**

- `success` `boolean`

### Spring.SetUnitRadiusAndHeight {#Spring.SetUnitRadiusAndHeight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3719-L3725" target="_blank">source</a>]

```lua
Spring.SetUnitRadiusAndHeight(UnitID, number?, number?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `radius` `number?`
- `height` `number?`

**Returns**

- `success` `boolean`

### Spring.SetUnitBuildeeRadius {#Spring.SetUnitBuildeeRadius}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3755-L3761" target="_blank">source</a>]

Sets the unit's radius for when targeted by build, repair, reclaim-type commands.

```lua
Spring.SetUnitBuildeeRadius(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `build` `number` — radius for when targeted by build, repair, reclaim-type commands.

**Returns**

- `nil`

### Spring.SetUnitPieceParent {#Spring.SetUnitPieceParent}
*function*

Changes the pieces hierarchy of a unit by attaching a piece to a new parent.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3775-L3782" target="_blank">source</a>]

```lua
Spring.SetUnitPieceParent(UnitID, integer, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `AlteredPiece` `integer`
- `ParentPiece` `integer`

**Returns**

- `nil`

### Spring.SetUnitPieceMatrix {#Spring.SetUnitPieceMatrix}
*function*

Sets the local (i.e. parent-relative) matrix of the given piece.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3816-L3826" target="_blank">source</a>]

If any of the first three elements are non-zero, and also blocks all script animations from modifying it until {0, 0, 0} is passed.

```lua
Spring.SetUnitPieceMatrix(UnitID, integer, number[]) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceNum` `integer`
- `matrix` `number[]` — an array of 16 floats

**Returns**

- `valid` `boolean?` — whether the matrix can be used for the purpose of defining the piece spatial transformation. Blocks the piece animation, if true.

### Spring.SetUnitCollisionVolumeData {#Spring.SetUnitCollisionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3834-L3867" target="_blank">source</a>]

```lua
Spring.SetUnitCollisionVolumeData(UnitID, number, number, number, number, number, number, integer, integer, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `scaleX` `number`
- `scaleY` `number`
- `scaleZ` `number`
- `offsetX` `number`
- `offsetY` `number`
- `offsetZ` `number`
- `vType` `integer`
- `tType` `integer`
- `Axis` `integer`

**Returns**

- `enum` `nil` — COLVOL_TYPES {
COLVOL_TYPE_DISABLED = -1,
COLVOL_TYPE_ELLIPSOID = 0,
COLVOL_TYPE_CYLINDER,
COLVOL_TYPE_BOX,
COLVOL_TYPE_SPHERE,
COLVOL_NUM_TYPES       // number of non-disabled collision volume types
};
enum COLVOL_TESTS {
COLVOL_TEST_DISC = 0,
COLVOL_TEST_CONT = 1,
COLVOL_NUM_TESTS = 2   // number of tests
};
enum COLVOL_AXES {
COLVOL_AXIS_X   = 0,
COLVOL_AXIS_Y   = 1,
COLVOL_AXIS_Z   = 2,
COLVOL_NUM_AXES = 3    // number of collision volume axes
};

### Spring.SetUnitPieceCollisionVolumeData {#Spring.SetUnitPieceCollisionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3874-L3888" target="_blank">source</a>]

```lua
Spring.SetUnitPieceCollisionVolumeData(UnitID, integer, boolean, number, number, number, number, number, number, integer?, integer?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceIndex` `integer`
- `enable` `boolean`
- `scaleX` `number`
- `scaleY` `number`
- `scaleZ` `number`
- `offsetX` `number`
- `offsetY` `number`
- `offsetZ` `number`
- `volumeType` `integer?`
- `primaryAxis` `integer?`

**Returns**

- `nil`

### Spring.SetUnitPieceVisible {#Spring.SetUnitPieceVisible}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3895-L3902" target="_blank">source</a>]

```lua
Spring.SetUnitPieceVisible(UnitID, integer, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceIndex` `integer`
- `visible` `boolean`

**Returns**

- `nil`

### Spring.SetUnitSensorRadius {#Spring.SetUnitSensorRadius}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3909-L3915" target="_blank">source</a>]

```lua
Spring.SetUnitSensorRadius(UnitID, ("los"|"airLos"|"radar"|"sonar"|"seismic"|"radarJammer"...), integer) -> integer?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `type` `("los"|"airLos"|"radar"|"sonar"|"seismic"|"radarJammer"...)`
- `radius` `integer`

**Returns**

- `newRadius` `integer?` — New radius, or `nil` if unit is invalid.

### Spring.SetUnitPosErrorParams {#Spring.SetUnitPosErrorParams}
*function*

Sets a unit's radar wobble

Controls how much a unit's radar dot will wobble. Note that setting
this above the allyTeam's default wobble may result in the edgemost
dot positions failing to register in ray traces, i.e. things like
native "is under cursor" checks and some Lua interfaces.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3958-L3975" target="_blank">source</a>]

```lua
Spring.SetUnitPosErrorParams(UnitID, number?, number?, number?, number?, number?, number?, integer?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `posErrorVectorX` `number?`
- `posErrorVectorY` `number?`
- `posErrorVectorZ` `number?`
- `posErrorDeltaX` `number?`
- `posErrorDeltaY` `number?`
- `posErrorDeltaZ` `number?`
- `nextPosErrorUpdate` `integer?`

**Returns**

- `nil`

### Spring.SetUnitMoveGoal {#Spring.SetUnitMoveGoal}
*function*

Used by default commands to get in build-, attackrange etc.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L3999-L4010" target="_blank">source</a>]

```lua
Spring.SetUnitMoveGoal(UnitID, number, number, number, number?, number?, boolean?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `goalX` `number`
- `goalY` `number`
- `goalZ` `number`
- `goalRadius` `number?`
- `moveSpeed` `number?`
- `moveRaw` `boolean?`

**Returns**

- `nil`

### Spring.SetUnitLandGoal {#Spring.SetUnitLandGoal}
*function*

Used in conjunction with Spring.UnitAttach et al. to re-implement old airbase & fuel system in Lua.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4035-L4044" target="_blank">source</a>]

```lua
Spring.SetUnitLandGoal(UnitID, number, number, number, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `goalX` `number`
- `goalY` `number`
- `goalZ` `number`
- `goalRadius` `number?`

**Returns**

- `nil`

### Spring.ClearUnitGoal {#Spring.ClearUnitGoal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4065-L4070" target="_blank">source</a>]

```lua
Spring.ClearUnitGoal(UnitID, boolean?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `maneuver` `boolean?`

**Returns**

- `nil`

### Spring.SetUnitPhysics {#Spring.SetUnitPhysics}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4083-L4099" target="_blank">source</a>]

```lua
Spring.SetUnitPhysics(UnitID, number, number, number, number, number, number, number, number, number, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `velX` `number`
- `velY` `number`
- `velZ` `number`
- `rotX` `number`
- `rotY` `number`
- `rotZ` `number`
- `dragX` `number`
- `dragY` `number`
- `dragZ` `number`

**Returns**

- `nil`

### Spring.SetUnitMass {#Spring.SetUnitMass}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4105-L4110" target="_blank">source</a>]

```lua
Spring.SetUnitMass(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `mass` `number`

**Returns**

- `nil`

### Spring.SetUnitPosition {#Spring.SetUnitPosition}
*function*

Set unit position (2D)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4117-L4127" target="_blank">source</a>]

Sets a unit's position in 2D, at terrain height.

```lua
Spring.SetUnitPosition(UnitID, number, number, boolean?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `x` `number`
- `z` `number`
- `floating` `boolean?` — (Default: `false`) If true, over water the position is on surface. If false, on seafloor.

**Returns**

- `nil`

### Spring.SetUnitPosition (overload 1) {#Spring.SetUnitPosition-1}
*function*

Set unit position (3D)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4130-L4140" target="_blank">source</a>]

Sets a unit's position in 3D, at an arbitrary height.

```lua
Spring.SetUnitPosition(UnitID, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `x` `number`
- `y` `number`
- `z` `number`

**Returns**

- `nil`

### Spring.SetUnitRotation {#Spring.SetUnitRotation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4172-L4180" target="_blank">source</a>]

Note: PYR order

```lua
Spring.SetUnitRotation(UnitID, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pitch` `number` — Rotation in X axis
- `yaw` `number` — Rotation in Y axis
- `roll` `number` — Rotation in Z axis

**Returns**

- `nil`

### Spring.SetUnitDirection {#Spring.SetUnitDirection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4187-L4200" target="_blank">source</a>]

Set unit front direction vector. The vector is normalized in
the engine.

**Deprecated:** It's strongly that you use the overload that accepts
a right direction as `frontDir` alone doesn't define object orientation.

```lua
Spring.SetUnitDirection(UnitID, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `frontx` `number`
- `fronty` `number`
- `frontz` `number`

**Returns**

- `nil`

### Spring.SetUnitDirection (overload 1) {#Spring.SetUnitDirection-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4202-L4216" target="_blank">source</a>]

Set unit front and right direction vectors.

Both vectors will be normalized in the engine.

```lua
Spring.SetUnitDirection(UnitID, number, number, number, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `frontx` `number`
- `fronty` `number`
- `frontz` `number`
- `rightx` `number`
- `righty` `number`
- `rightz` `number`

**Returns**

- `nil`

### Spring.SetUnitHeadingAndUpDir {#Spring.SetUnitHeadingAndUpDir}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4242-L4254" target="_blank">source</a>]

Use this call to set up unit direction in a robust way. If unit was
completely upright, new `{upx, upy, upz}` direction will be used as new "up"
vector, the rotation set by "heading" will remain preserved.

```lua
Spring.SetUnitHeadingAndUpDir(UnitID, Heading, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `heading` [`Heading`](Aliases.md#Heading)
- `upx` `number`
- `upy` `number`
- `upz` `number`

**Returns**

- `nil`

### Spring.SetUnitVelocity {#Spring.SetUnitVelocity}
*function*

Set the velocity of a Unit

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4260-L4268" target="_blank">source</a>]

**See:** Spring.SetUnitMoveCtrl for disabling/enabling this control

```lua
Spring.SetUnitVelocity(UnitID, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `velX` `number` — in elmos/frame
- `velY` `number` — in elmos/frame
- `velZ` `number` — in elmos/frame

### Spring.SetFactoryBuggerOff {#Spring.SetFactoryBuggerOff}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4275-L4286" target="_blank">source</a>]

```lua
Spring.SetFactoryBuggerOff(UnitID, boolean?, number?, number?, Heading?, boolean?, boolean?) -> number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `buggerOff` `boolean?`
- `offset` `number?`
- `radius` `number?`
- `relHeading` `Heading?`
- `spherical` `boolean?`
- `forced` `boolean?`

**Returns**

- `buggerOff` `number?`

### Spring.BuggerOff {#Spring.BuggerOff}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4309-L4322" target="_blank">source</a>]

```lua
Spring.BuggerOff(number, number, number?, number, TeamID, boolean?, boolean?, UnitID?, UnitDefID[]?) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number?` — uses ground height when unspecified
- `radius` `number`
- `teamID` [`TeamID`](Aliases.md#TeamID)
- `spherical` `boolean?` — (Default: `true`)
- `forced` `boolean?` — (Default: `true`)
- `excludeUnitID` `UnitID?`
- `excludeUnitDefIDs` `UnitDefID[]?`

**Returns**

- `nil`

### Spring.AddFeatureDamage {#Spring.AddFeatureDamage}
*function*

Apply damage to feature

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4378-L4400" target="_blank">source</a>]

Will trigger FeaturePreDamaged and FeatureDamaged callins.

Won't do anything if paralyze is not zero, the feature is already marked for deletion, or in void.

If health goes below 0 and featureDef is `destructable` the feature will be deleted and
a wreck created.

**See:** SyncedCallins:FeatureDamaged

```lua
Spring.AddFeatureDamage(FeatureID, number, integer?, UnitID?, WeaponDefID?, number?, number?, number?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `damage` `number`
- `paralyze` `integer?` — (Default: `0`) equals to the paralyzetime in the WeaponDef.
- `attackerID` `UnitID?` — (Default: `-1`)
- `weaponID` `WeaponDefID?` — (Default: `-1`)
- `impulseX` `number?`
- `impulseY` `number?`
- `impulseZ` `number?`

### Spring.AddUnitDamage {#Spring.AddUnitDamage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4423-L4435" target="_blank">source</a>]

```lua
Spring.AddUnitDamage(UnitID, number, integer?, UnitID?, WeaponDefID?, number?, number?, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `damage` `number`
- `paralyze` `integer?` — (Default: `0`) equals to the paralyzetime in the WeaponDef.
- `attackerID` `UnitID?` — (Default: `-1`)
- `weaponID` `WeaponDefID?` — (Default: `-1`)
- `impulseX` `number?`
- `impulseY` `number?`
- `impulseZ` `number?`

**Returns**

- `nil`

### Spring.AddUnitImpulse {#Spring.AddUnitImpulse}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4460-L4468" target="_blank">source</a>]

```lua
Spring.AddUnitImpulse(UnitID, number, number, number, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `x` `number`
- `y` `number`
- `z` `number`
- `decayRate` `number?`

**Returns**

- `nil`

### Spring.AddUnitSeismicPing {#Spring.AddUnitSeismicPing}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4485-L4490" target="_blank">source</a>]

```lua
Spring.AddUnitSeismicPing(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pindSize` `number`

**Returns**

- `nil`

### Spring.AddUnitResource {#Spring.AddUnitResource}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4505-L4511" target="_blank">source</a>]

```lua
Spring.AddUnitResource(UnitID, string, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `resource` `string` — "m" | "e"
- `amount` `number`

**Returns**

- `nil`

### Spring.UseUnitResource {#Spring.UseUnitResource}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4534-L4540" target="_blank">source</a>]

```lua
Spring.UseUnitResource(UnitID, ResourceName, number) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `resource` [`ResourceName`](Aliases.md#ResourceName)
- `amount` `number`

**Returns**

- `okay` `boolean?`

### Spring.UseUnitResource (overload 1) {#Spring.UseUnitResource-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4542-L4547" target="_blank">source</a>]

```lua
Spring.UseUnitResource(UnitID, ResourceUsage) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `resources` [`ResourceUsage`](Aliases.md#ResourceUsage)

**Returns**

- `okay` `boolean?`

### Spring.AddObjectDecal {#Spring.AddObjectDecal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4612-L4617" target="_blank">source</a>]

```lua
Spring.AddObjectDecal(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `nil`

### Spring.RemoveObjectDecal {#Spring.RemoveObjectDecal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4630-L4634" target="_blank">source</a>]

```lua
Spring.RemoveObjectDecal(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `nil`

### Spring.AddGrass {#Spring.AddGrass}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4653-L4658" target="_blank">source</a>]

```lua
Spring.AddGrass(number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`

**Returns**

- `nil`

### Spring.RemoveGrass {#Spring.RemoveGrass}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4668-L4673" target="_blank">source</a>]

```lua
Spring.RemoveGrass(number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`

**Returns**

- `nil`

### Spring.CreateFeature {#Spring.CreateFeature}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4689-L4699" target="_blank">source</a>]

```lua
Spring.CreateFeature((string|integer), number, number, number, Heading?, TeamID?, FeatureID?) -> FeatureID?
```

**Parameters**

- `featureDef` `(string|integer)` — name or id
- `x` `number`
- `y` `number`
- `z` `number`
- `heading` `Heading?`
- `teamID` `TeamID?`
- `featureID` `FeatureID?`

**Returns**

- `featureID` `FeatureID?` — returns nil if creation was unsuccessful

### Spring.DestroyFeature {#Spring.DestroyFeature}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4787-L4791" target="_blank">source</a>]

```lua
Spring.DestroyFeature(FeatureID) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `nil`

### Spring.TransferFeature {#Spring.TransferFeature}
*function*

Feature Control

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4804-L4810" target="_blank">source</a>]

```lua
Spring.TransferFeature(FeatureID, TeamID) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `nil`

### Spring.SetFeatureAlwaysVisible {#Spring.SetFeatureAlwaysVisible}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4826-L4831" target="_blank">source</a>]

```lua
Spring.SetFeatureAlwaysVisible(FeatureID, boolean) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `enable` `boolean`

**Returns**

- `nil`

### Spring.SetFeatureUseAirLos {#Spring.SetFeatureUseAirLos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4837-L4843" target="_blank">source</a>]

```lua
Spring.SetFeatureUseAirLos(FeatureID, boolean) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `useAirLos` `boolean`

**Returns**

- `nil`

### Spring.SetFeatureHealth {#Spring.SetFeatureHealth}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4850-L4856" target="_blank">source</a>]

```lua
Spring.SetFeatureHealth(FeatureID, number, boolean?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `health` `number`
- `checkDestruction` `boolean?` — (Default: `false`) Whether to destroy feature if feature goes below 0 health.

**Returns**

- `nil`

### Spring.SetFeatureMaxHealth {#Spring.SetFeatureMaxHealth}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4873-L4879" target="_blank">source</a>]

```lua
Spring.SetFeatureMaxHealth(FeatureID, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `maxHealth` `number` — minimum 0.1

**Returns**

- `nil`

### Spring.SetFeatureReclaim {#Spring.SetFeatureReclaim}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4893-L4898" target="_blank">source</a>]

```lua
Spring.SetFeatureReclaim(FeatureID, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `reclaimLeft` `number`

**Returns**

- `nil`

### Spring.SetFeatureResources {#Spring.SetFeatureResources}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4910-L4920" target="_blank">source</a>]

```lua
Spring.SetFeatureResources(FeatureID, number, number, number?, number?, number?, number?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `metal` `number`
- `energy` `number`
- `reclaimTime` `number?`
- `reclaimLeft` `number?`
- `featureDefMetal` `number?`
- `featureDefEnergy` `number?`

**Returns**

- `nil`

### Spring.SetFeatureResurrect {#Spring.SetFeatureResurrect}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4939-L4947" target="_blank">source</a>]

```lua
Spring.SetFeatureResurrect(FeatureID, (string|integer)?, Facing?, number?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `unitDef` `(string|integer)?` — Can be a number id or a string name, this allows cancelling resurrection by passing `-1`.
- `facing` `Facing?` — (Default: `"south"`)
- `progress` `number?` — Set the level of progress.

**Returns**

- `nil`

### Spring.SetFeatureMoveCtrl {#Spring.SetFeatureMoveCtrl}
*function*

Enable feature movement control.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4975-L4987" target="_blank">source</a>]

```lua
Spring.SetFeatureMoveCtrl(FeatureID, true, number?, number?, number?, number?, number?, number?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `enabled` `true` — Enable feature movement.
- `initialVelocityX` `number?` — Initial velocity on X axis, or `nil` for no change.
- `initialVelocityY` `number?` — Initial velocity on Y axis, or `nil` for no change.
- `initialVelocityZ` `number?` — Initial velocity on Z axis, or `nil` for no change.
- `accelerationX` `number?` — Acceleration per frame on X axis, or `nil` for no change.
- `accelerationY` `number?` — Acceleration per frame on Y axis, or `nil` for no change.
- `accelerationZ` `number?` — Acceleration per frame on Z axis, or `nil` for no change.

### Spring.SetFeatureMoveCtrl (overload 1) {#Spring.SetFeatureMoveCtrl-1}
*function*

Disable feature movement control.

Optional parameter allow physics vectors to build when not using [MoveCtrl](MoveCtrl.md#MoveCtrl).

It is necessary to unlock feature movement on x, z axis before changing
feature physics.

For example:

```lua
-- Unlock all movement before setting velocity.
Spring.SetFeatureMoveCtrl(featureID,false,1,1,1,1,1,1,1,1,1)

-- Set velocity.
Spring.SetFeatureVelocity(featureID,10,0,10)
```

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4989-L5019" target="_blank">source</a>]

```lua
Spring.SetFeatureMoveCtrl(FeatureID, false, number?, number?, number?, number?, number?, number?, number?, number?, number?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `enabled` `false` — Disable feature movement.
- `velocityMaskX` `number?` — Lock velocity change in X dimension when not using [MoveCtrl](MoveCtrl.md#MoveCtrl). `0` to lock, non-zero to allow, or `nil` to for no change.
- `velocityMaskY` `number?` — Lock velocity change in Y dimension when not using [MoveCtrl](MoveCtrl.md#MoveCtrl). `0` to lock, non-zero to allow, or `nil` to for no change.
- `velocityMaskZ` `number?` — Lock velocity change in Z dimension when not using [MoveCtrl](MoveCtrl.md#MoveCtrl). `0` to lock, non-zero to allow, or `nil` to for no change.
- `impulseMaskX` `number?` — Lock impulse in X dimension when not using [MoveCtrl](MoveCtrl.md#MoveCtrl). `0` to lock, non-zero to allow, or `nil` to for no change.
- `impulseMaskY` `number?` — Lock impulse in Y dimension when not using [MoveCtrl](MoveCtrl.md#MoveCtrl). `0` to lock, non-zero to allow, or `nil` to for no change.
- `impulseMaskZ` `number?` — Lock impulse in Z dimension when not using [MoveCtrl](MoveCtrl.md#MoveCtrl). `0` to lock, non-zero to allow, or `nil` to for no change.
- `movementMaskX` `number?` — Lock move in X dimension when not using [MoveCtrl](MoveCtrl.md#MoveCtrl). `0` to lock the axis, non-zero to allow, or `nil` for no change.
- `movementMaskY` `number?` — Lock move in Y dimension when not using [MoveCtrl](MoveCtrl.md#MoveCtrl). `0` to lock the axis, non-zero to allow, or `nil` for no change.
- `movementMaskZ` `number?` — Lock move in Z dimension when not using [MoveCtrl](MoveCtrl.md#MoveCtrl). `0` to lock the axis, non-zero to allow, or `nil` for no change.

### Spring.SetFeaturePhysics {#Spring.SetFeaturePhysics}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5050-L5066" target="_blank">source</a>]

```lua
Spring.SetFeaturePhysics(FeatureID, number, number, number, number, number, number, number, number, number, number, number, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `velX` `number`
- `velY` `number`
- `velZ` `number`
- `rotX` `number`
- `rotY` `number`
- `rotZ` `number`
- `dragX` `number`
- `dragY` `number`
- `dragZ` `number`

**Returns**

- `nil`

### Spring.SetFeatureMass {#Spring.SetFeatureMass}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5073-L5078" target="_blank">source</a>]

```lua
Spring.SetFeatureMass(FeatureID, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `mass` `number`

**Returns**

- `nil`

### Spring.SetFeaturePosition {#Spring.SetFeaturePosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5085-L5093" target="_blank">source</a>]

```lua
Spring.SetFeaturePosition(FeatureID, number, number, number, boolean?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `x` `number`
- `y` `number`
- `z` `number`
- `snapToGround` `boolean?`

**Returns**

- `nil`

### Spring.SetFeatureRotation {#Spring.SetFeatureRotation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5111-L5119" target="_blank">source</a>]

Note: PYR order

```lua
Spring.SetFeatureRotation(FeatureID, number, number, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pitch` `number` — Rotation in X axis
- `yaw` `number` — Rotation in Y axis
- `roll` `number` — Rotation in Z axis

**Returns**

- `nil`

### Spring.SetFeatureDirection {#Spring.SetFeatureDirection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5126-L5139" target="_blank">source</a>]

Set feature front direction vector. The vector is normalized in
the engine.

**Deprecated:** It's strongly that you use the overload that accepts
a right direction as `frontDir` alone doesn't define object orientation.

```lua
Spring.SetFeatureDirection(FeatureID, number, number, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `frontx` `number`
- `fronty` `number`
- `frontz` `number`

**Returns**

- `nil`

### Spring.SetFeatureDirection (overload 1) {#Spring.SetFeatureDirection-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5141-L5155" target="_blank">source</a>]

Set feature front and right direction vectors.

Both vectors will be normalized in the engine.

```lua
Spring.SetFeatureDirection(FeatureID, number, number, number, number, number, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `frontx` `number`
- `fronty` `number`
- `frontz` `number`
- `rightx` `number`
- `righty` `number`
- `rightz` `number`

**Returns**

- `nil`

### Spring.SetFeatureHeadingAndUpDir {#Spring.SetFeatureHeadingAndUpDir}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5161-L5173" target="_blank">source</a>]

Use this call to set up feature direction in a robust way. If feature was
completely upright, new `{upx, upy, upz}` direction will be used as new "up"
vector, the rotation set by "heading" will remain preserved.

```lua
Spring.SetFeatureHeadingAndUpDir(FeatureID, Heading, number, number, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `heading` [`Heading`](Aliases.md#Heading)
- `upx` `number`
- `upy` `number`
- `upz` `number`

**Returns**

- `nil`

### Spring.SetFeatureVelocity {#Spring.SetFeatureVelocity}
*function*

Set the velocity of a Feature

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5179-L5187" target="_blank">source</a>]

**See:** Spring.SetFeatureMoveCtrl for disabling/enabling this control

```lua
Spring.SetFeatureVelocity(FeatureID, number, number, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `velX` `number` — in elmos/frame
- `velY` `number` — in elmos/frame
- `velZ` `number` — in elmos/frame

### Spring.SetFeatureBlocking {#Spring.SetFeatureBlocking}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5194-L5205" target="_blank">source</a>]

```lua
Spring.SetFeatureBlocking(FeatureID, boolean?, boolean?, boolean?, boolean?, boolean?, boolean?, boolean?) -> boolean
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `isBlocking` `boolean?` — If `true` add this feature to the `GroundBlockingMap`, but only if it collides with solid objects (or is being set to collide with the `isSolidObjectCollidable` argument). If `false`, remove this feature from the `GroundBlockingMap`. No change if `nil`.
- `isSolidObjectCollidable` `boolean?` — Enable or disable collision with solid objects, or no change if `nil`.
- `isProjectileCollidable` `boolean?` — Enable or disable collision with projectiles, or no change if `nil`.
- `isRaySegmentCollidable` `boolean?` — Enable or disable collision with ray segments, or no change if `nil`.
- `crushable` `boolean?` — Enable or disable crushable, or no change if `nil`.
- `blockEnemyPushing` `boolean?` — Enable or disable blocking enemy pushing, or no change if `nil`.
- `blockHeightChanges` `boolean?` — Enable or disable blocking height changes, or no change if `nil`.

**Returns**

- `isBlocking` `boolean`

### Spring.SetFeatureNoSelect {#Spring.SetFeatureNoSelect}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5212-L5217" target="_blank">source</a>]

```lua
Spring.SetFeatureNoSelect(FeatureID, boolean) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `noSelect` `boolean`

**Returns**

- `nil`

### Spring.SetFeatureMidAndAimPos {#Spring.SetFeatureMidAndAimPos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5230-L5244" target="_blank">source</a>]

Check [Spring.SetUnitMidAndAimPos](Spring.md#Spring.SetUnitMidAndAimPos) for further explanation of the arguments.

```lua
Spring.SetFeatureMidAndAimPos(FeatureID, number, number, number, number, number, number, boolean?) -> boolean
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `mpX` `number`
- `mpY` `number`
- `mpZ` `number`
- `apX` `number`
- `apY` `number`
- `apZ` `number`
- `relative` `boolean?`

**Returns**

- `success` `boolean`

### Spring.SetFeatureRadiusAndHeight {#Spring.SetFeatureRadiusAndHeight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5281-L5287" target="_blank">source</a>]

```lua
Spring.SetFeatureRadiusAndHeight(FeatureID, number?, number?) -> boolean
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `radius` `number?`
- `height` `number?`

**Returns**

- `success` `boolean`

### Spring.SetFeatureCollisionVolumeData {#Spring.SetFeatureCollisionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5316-L5332" target="_blank">source</a>]

Check [Spring.SetUnitCollisionVolumeData](Spring.md#Spring.SetUnitCollisionVolumeData) for further explanation of the arguments.

```lua
Spring.SetFeatureCollisionVolumeData(FeatureID, number, number, number, number, number, number, integer, integer, integer) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `scaleX` `number`
- `scaleY` `number`
- `scaleZ` `number`
- `offsetX` `number`
- `offsetY` `number`
- `offsetZ` `number`
- `vType` `integer`
- `tType` `integer`
- `Axis` `integer`

**Returns**

- `nil`

### Spring.SetFeaturePieceCollisionVolumeData {#Spring.SetFeaturePieceCollisionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5339-L5354" target="_blank">source</a>]

```lua
Spring.SetFeaturePieceCollisionVolumeData(FeatureID, integer, boolean, number, number, number, number, number, number, number, number, number?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceIndex` `integer`
- `enable` `boolean`
- `scaleX` `number`
- `scaleY` `number`
- `scaleZ` `number`
- `offsetX` `number`
- `offsetY` `number`
- `offsetZ` `number`
- `Axis` `number`
- `volumeType` `number`
- `primaryAxis` `number?`

**Returns**

- `nil`

### Spring.SetFeaturePieceVisible {#Spring.SetFeaturePieceVisible}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5360-L5367" target="_blank">source</a>]

```lua
Spring.SetFeaturePieceVisible(FeatureID, integer, boolean) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceIndex` `integer`
- `visible` `boolean`

**Returns**

- `nil`

### Spring.SetFeaturePieceMatrix {#Spring.SetFeaturePieceMatrix}
*function*

Sets the local (i.e. parent-relative) matrix of the given piece, for a feature.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5373-L5381" target="_blank">source</a>]

```lua
Spring.SetFeaturePieceMatrix(FeatureID, integer, number[]) -> boolean?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceIndex` `integer`
- `matrix` `number[]` — an array of 16 floats

**Returns**

- `valid` `boolean?` — whether the matrix can be used for the purpose of defining the piece spatial transformation

### Spring.SetFeatureFireTime {#Spring.SetFeatureFireTime}
*function*

Set the fire timer for a feature.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5389-L5398" target="_blank">source</a>]

Starts or resets an internal feature fire timer, when reaching zero the
feature will be destroyed.

```lua
Spring.SetFeatureFireTime(FeatureID, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `fireTime` `number` — in seconds

### Spring.SetFeatureSmokeTime {#Spring.SetFeatureSmokeTime}
*function*

Set the smoke timer for a feature.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5421-L5433" target="_blank">source</a>]

If different than zero, starts emitting smoke until the timer counts down to zero.

Setting to zero will stop smoke emission by the feature.

The smoke timer affects both the duration and size of the smoke particles.

```lua
Spring.SetFeatureSmokeTime(FeatureID, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `smokeTime` `number` — in seconds

### Spring.CreateUnitWreck {#Spring.CreateUnitWreck}
*function*

Create a wreck from a unit

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5462-L5470" target="_blank">source</a>]

```lua
Spring.CreateUnitWreck(UnitID, integer?, boolean?) -> FeatureID?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `wreckLevel` `integer?` — (Default: `1`) Wreck index to use.
- `doSmoke` `boolean?` — (Default: `true`) Wreck emits smoke when `true`.

**Returns**

- `featureID` `FeatureID?` — The wreck featureID, or nil if it couldn't be created or unit doesn't exist.

### Spring.CreateFeatureWreck {#Spring.CreateFeatureWreck}
*function*

Create a wreck from a feature

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5492-L5500" target="_blank">source</a>]

```lua
Spring.CreateFeatureWreck(FeatureID, integer?, boolean?) -> FeatureID?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `wreckLevel` `integer?` — (Default: `1`) Wreck index to use.
- `doSmoke` `boolean?` — (Default: `false`) Wreck emits smoke when `true`.

**Returns**

- `featureID` `FeatureID?` — The wreck featureID, or nil if it couldn't be created or unit doesn't exist.

### Spring.SetProjectileAlwaysVisible {#Spring.SetProjectileAlwaysVisible}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5527-L5532" target="_blank">source</a>]

```lua
Spring.SetProjectileAlwaysVisible(ProjectileID, boolean) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `alwaysVisible` `boolean`

**Returns**

- `nil`

### Spring.SetProjectileUseAirLos {#Spring.SetProjectileUseAirLos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5539-L5545" target="_blank">source</a>]

```lua
Spring.SetProjectileUseAirLos(ProjectileID, boolean) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `useAirLos` `boolean`

**Returns**

- `nil`

### Spring.SetProjectileMoveControl {#Spring.SetProjectileMoveControl}
*function*

Set whether engine should process position and speed for a projectile

Contrary to [Spring.SetFeatureMoveCtrl](Spring.md#Spring.SetFeatureMoveCtrl), speed and position for projectiles
can be set regardless of whether this method has been called or not.

Passing true merely skips engine updating velocity and position.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5552-L5563" target="_blank">source</a>]

```lua
Spring.SetProjectileMoveControl(ProjectileID, boolean?) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `enable` `boolean?`

### Spring.SetProjectilePosition {#Spring.SetProjectilePosition}
*function*

Set the position of a projectile

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5577-L5584" target="_blank">source</a>]

```lua
Spring.SetProjectilePosition(ProjectileID, number?, number?, number?) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `posX` `number?` — (Default: `0`)
- `posY` `number?` — (Default: `0`)
- `posZ` `number?` — (Default: `0`)

### Spring.SetProjectileVelocity {#Spring.SetProjectileVelocity}
*function*

Set the velocity of a projectile

> [!NOTE]
> Differently from features, [Spring.SetProjectileMoveControl](Spring.md#Spring.SetProjectileMoveControl) is not
> required to have been called to make use of this method, but often used in
> conjunction.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5599-L5612" target="_blank">source</a>]

**See:** [Spring.SetProjectileMoveControl](Spring.md#Spring.SetProjectileMoveControl)

```lua
Spring.SetProjectileVelocity(ProjectileID, number, number, number) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `velX` `number` — in elmos/frame
- `velY` `number` — in elmos/frame
- `velZ` `number` — in elmos/frame

### Spring.SetProjectileCollision {#Spring.SetProjectileCollision}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5618-L5621" target="_blank">source</a>]

```lua
Spring.SetProjectileCollision(ProjectileID) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

### Spring.SetProjectileTarget {#Spring.SetProjectileTarget}
*function*

Set projectile target (object)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5641-L5648" target="_blank">source</a>]

```lua
Spring.SetProjectileTarget(ProjectileID, (UnitID|FeatureID|ProjectileID), ProjectileTargetType) -> boolean?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `targetID` `(UnitID|FeatureID|ProjectileID)`
- `targetType` [`ProjectileTargetType`](ProjectileTargetType.md#ProjectileTargetType)

**Returns**

- `validTarget` `boolean?`

### Spring.SetProjectileTarget (overload 1) {#Spring.SetProjectileTarget-1}
*function*

Set projectile target (position)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5650-L5659" target="_blank">source</a>]

```lua
Spring.SetProjectileTarget(ProjectileID, number, number, number) -> boolean?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `posX` `number`
- `posY` `number`
- `posZ` `number`

**Returns**

- `validTarget` `boolean?`

### Spring.SetProjectileTimeToLive {#Spring.SetProjectileTimeToLive}
*function*

Set Time To Live for a projectile

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5734-L5739" target="_blank">source</a>]

```lua
Spring.SetProjectileTimeToLive(ProjectileID, integer) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `ttl` `integer` — Remaining time to live in frames

### Spring.SetProjectileIsIntercepted {#Spring.SetProjectileIsIntercepted}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5756-L5759" target="_blank">source</a>]

```lua
Spring.SetProjectileIsIntercepted(ProjectileID) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

### Spring.SetProjectileDamages {#Spring.SetProjectileDamages}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5775-L5781" target="_blank">source</a>]

```lua
Spring.SetProjectileDamages(ProjectileID, integer, string, number) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `weaponNum` `integer`
- `key` `string`
- `value` `number`

### Spring.SetProjectileIgnoreTrackingError {#Spring.SetProjectileIgnoreTrackingError}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5811-L5815" target="_blank">source</a>]

```lua
Spring.SetProjectileIgnoreTrackingError(ProjectileID, boolean) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `ignore` `boolean`

### Spring.SetProjectileGravity {#Spring.SetProjectileGravity}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5840-L5845" target="_blank">source</a>]

```lua
Spring.SetProjectileGravity(ProjectileID, number?) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `grav` `number?` — (Default: `0`)

**Returns**

- `nil`

### Spring.SetPieceProjectileParams {#Spring.SetPieceProjectileParams}
*function*

Set piece projectile params

Non passed or nil args don't set params.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5863-L5875" target="_blank">source</a>]

```lua
Spring.SetPieceProjectileParams(ProjectileID, integer?, number?, number?, number?, number?, number?) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `explosionFlags` `integer?`
- `spinAngle` `number?`
- `spinSpeed` `number?`
- `spinVectorX` `number?`
- `spinVectorY` `number?`
- `spinVectorZ` `number?`

### Spring.SetProjectileCEG {#Spring.SetProjectileCEG}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5897-L5902" target="_blank">source</a>]

```lua
Spring.SetProjectileCEG(ProjectileID, string) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `ceg_name` `string`

**Returns**

- `nil`

### Spring.UnitFinishCommand {#Spring.UnitFinishCommand}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5936-L5939" target="_blank">source</a>]

```lua
Spring.UnitFinishCommand(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### Spring.GiveOrderToUnit {#Spring.GiveOrderToUnit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5953-L5962" target="_blank">source</a>]

```lua
Spring.GiveOrderToUnit(UnitID, (CMD|integer), CreateCommandParams?, CreateCommandOptions?, integer?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `cmdID` `(CMD|integer)` — The command ID.
- `params` `CreateCommandParams?` — Parameters for the given command.
- `options` `CreateCommandOptions?`
- `timeout` `integer?` — Absolute frame number. The command will be discarded after this frame. Only respected by mobile units.

**Returns**

- `unitOrdered` `boolean`

### Spring.GiveOrderToUnit (overload 1) {#Spring.GiveOrderToUnit-1}
*function*

Give order to specific unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3557-L3567" target="_blank">source</a>]

```lua
Spring.GiveOrderToUnit(UnitID, (CMD|integer), CreateCommandParams?, CreateCommandOptions?, integer?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `cmdID` `(CMD|integer)` — The command ID.
- `params` `CreateCommandParams?` — Parameters for the given command.
- `options` `CreateCommandOptions?`
- `timeout` `integer?` — Absolute frame number. The command will be discarded after this frame. Only respected by mobile units.

**Returns**

- `boolean`

### Spring.GiveOrderToUnitMap {#Spring.GiveOrderToUnitMap}
*function*

Give order to multiple units, specified by table keys.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L5989-L5999" target="_blank">source</a>]

```lua
Spring.GiveOrderToUnitMap(table<UnitID,any>, (CMD|integer), CreateCommandParams?, CreateCommandOptions?, integer?) -> integer
```

**Parameters**

- `unitMap` `table<UnitID,any>` — A table with unit IDs as keys.
- `cmdID` `(CMD|integer)` — The command ID.
- `params` `CreateCommandParams?` — Parameters for the given command.
- `options` `CreateCommandOptions?`
- `timeout` `integer?` — Absolute frame number. The command will be discarded after this frame. Only respected by mobile units.

**Returns**

- `unitsOrdered` `integer` — The number of units ordered.

### Spring.GiveOrderToUnitMap (overload 1) {#Spring.GiveOrderToUnitMap-1}
*function*

Give order to multiple units, specified by table keys.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3591-L3601" target="_blank">source</a>]

```lua
Spring.GiveOrderToUnitMap(table<UnitID,any>, (CMD|integer), CreateCommandParams?, CreateCommandOptions?, integer?) -> boolean
```

**Parameters**

- `unitMap` `table<UnitID,any>` — A table with unit IDs as keys.
- `cmdID` `(CMD|integer)` — The command ID.
- `params` `CreateCommandParams?` — Parameters for the given command.
- `options` `CreateCommandOptions?`
- `timeout` `integer?` — Absolute frame number. The command will be discarded after this frame. Only respected by mobile units.

**Returns**

- `orderGiven` `boolean`

### Spring.GiveOrderToUnitArray {#Spring.GiveOrderToUnitArray}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6032-L6041" target="_blank">source</a>]

```lua
Spring.GiveOrderToUnitArray(UnitID[], (CMD|integer), CreateCommandParams?, CreateCommandOptions?, integer?) -> integer
```

**Parameters**

- `unitIDs` `UnitID[]` — An array of unit IDs.
- `cmdID` `(CMD|integer)` — The command ID.
- `params` `CreateCommandParams?` — Parameters for the given command.
- `options` `CreateCommandOptions?`
- `timeout` `integer?` — Absolute frame number. The command will be discarded after this frame. Only respected by mobile units.

**Returns**

- `unitsOrdered` `integer` — The number of units ordered.

### Spring.GiveOrderToUnitArray (overload 1) {#Spring.GiveOrderToUnitArray-1}
*function*

Give order to an array of units.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3625-L3635" target="_blank">source</a>]

```lua
Spring.GiveOrderToUnitArray(UnitID[], (CMD|integer), CreateCommandParams?, CreateCommandOptions?, integer?) -> boolean
```

**Parameters**

- `unitIDs` `UnitID[]` — Array of unit IDs.
- `cmdID` `(CMD|integer)` — The command ID.
- `params` `CreateCommandParams?` — Parameters for the given command.
- `options` `CreateCommandOptions?`
- `timeout` `integer?` — Absolute frame number. The command will be discarded after this frame. Only respected by mobile units.

**Returns**

- `ordersGiven` `boolean` — `true` if any orders were sent, otherwise `false`.

### Spring.GiveOrderArrayToUnit {#Spring.GiveOrderArrayToUnit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6076-L6082" target="_blank">source</a>]

```lua
Spring.GiveOrderArrayToUnit(UnitID, CreateCommand[]) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `commands` `CreateCommand[]`

**Returns**

- `ordersGiven` `boolean`

### Spring.GiveOrderArrayToUnit (overload 1) {#Spring.GiveOrderArrayToUnit-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3658-L3664" target="_blank">source</a>]

```lua
Spring.GiveOrderArrayToUnit(UnitID, CreateCommand[]) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID) — Unit ID.
- `commands` `CreateCommand[]`

**Returns**

- `ordersGiven` `boolean` — `true` if any orders were sent, otherwise `false`.

### Spring.GiveOrderArrayToUnitMap {#Spring.GiveOrderArrayToUnitMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6115-L6120" target="_blank">source</a>]

```lua
Spring.GiveOrderArrayToUnitMap(table<UnitID,any>, CreateCommand[]) -> integer
```

**Parameters**

- `unitMap` `table<UnitID,any>` — A table with unit IDs as keys.
- `commands` `CreateCommand[]`

**Returns**

- `unitsOrdered` `integer` — The number of units ordered.

### Spring.GiveOrderArrayToUnitMap (overload 1) {#Spring.GiveOrderArrayToUnitMap-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3692-L3698" target="_blank">source</a>]

```lua
Spring.GiveOrderArrayToUnitMap(table<UnitID,any>, CreateCommand[]) -> boolean
```

**Parameters**

- `unitMap` `table<UnitID,any>` — A table with unit IDs as keys.
- `commands` `CreateCommand[]`

**Returns**

- `ordersGiven` `boolean` — `true` if any orders were sent, otherwise `false`.

### Spring.GiveOrderArrayToUnitArray {#Spring.GiveOrderArrayToUnitArray}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6155-L6167" target="_blank">source</a>]

```lua
Spring.GiveOrderArrayToUnitArray(UnitID[], CreateCommand[], boolean?) -> integer
```

**Parameters**

- `unitIDs` `UnitID[]` — Array of unit IDs.
- `commands` `CreateCommand[]`
- `pairwise` `boolean?` — (Default: `false`) When `false`, assign all commands to each unit.

When `true`, assign commands according to index between units and cmds arrays.

If `len(unitArray) < len(cmdArray)` only the first `len(unitArray)` commands
will be assigned, and vice-versa.

**Returns**

- `unitsOrdered` `integer` — The number of units ordered.

### Spring.GiveOrderArrayToUnitArray (overload 1) {#Spring.GiveOrderArrayToUnitArray-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3726-L3738" target="_blank">source</a>]

```lua
Spring.GiveOrderArrayToUnitArray(UnitID[], CreateCommand[], boolean?) -> boolean
```

**Parameters**

- `unitIDs` `UnitID[]` — Array of unit IDs.
- `commands` `CreateCommand[]`
- `pairwise` `boolean?` — (Default: `false`) When `false`, assign all commands to each unit.

When `true`, assign commands according to index between units and cmds arrays.

If `len(unitArray) < len(cmdArray)` only the first `len(unitArray)` commands
will be assigned, and vice-versa.

**Returns**

- `ordersGiven` `boolean` — `true` if any orders were sent, otherwise `false`.

### Spring.LevelHeightMap {#Spring.LevelHeightMap}
*function*

Set the height of a point in the world.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6283-L6290" target="_blank">source</a>]

```lua
Spring.LevelHeightMap(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`

### Spring.LevelHeightMap (overload 1) {#Spring.LevelHeightMap-1}
*function*

Set the height of a rectangle area in the world.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6291-L6301" target="_blank">source</a>]

```lua
Spring.LevelHeightMap(number, number, number, number, number?) -> nil
```

**Parameters**

- `x1` `number`
- `z1` `number`
- `x2` `number`
- `z2` `number`
- `height` `number?`

**Returns**

- `nil`

### Spring.AdjustHeightMap {#Spring.AdjustHeightMap}
*function*

Add height to a point in the world.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6322-L6329" target="_blank">source</a>]

```lua
Spring.AdjustHeightMap(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`

### Spring.AdjustHeightMap (overload 1) {#Spring.AdjustHeightMap-1}
*function*

Add height to a rectangle in the world.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6331-L6341" target="_blank">source</a>]

```lua
Spring.AdjustHeightMap(number, number, number, number, number?) -> nil
```

**Parameters**

- `x1` `number`
- `z1` `number`
- `x2` `number`
- `z2` `number`
- `height` `number?`

**Returns**

- `nil`

### Spring.RevertHeightMap {#Spring.RevertHeightMap}
*function*

Restore map height at a point in the world.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6363-L6370" target="_blank">source</a>]

```lua
Spring.RevertHeightMap(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`

### Spring.RevertHeightMap (overload 1) {#Spring.RevertHeightMap-1}
*function*

Restore map height of a rectangle area in the world.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6371-L6381" target="_blank">source</a>]

```lua
Spring.RevertHeightMap(number, number, number, number, number?) -> nil
```

**Parameters**

- `x1` `number`
- `z1` `number`
- `x2` `number`
- `z2` `number`
- `height` `number?`

**Returns**

- `nil`

### Spring.AddHeightMap {#Spring.AddHeightMap}
*function*

Can only be called in [Spring.SetHeightMapFunc](Spring.md#Spring.SetHeightMapFunc)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6420-L6427" target="_blank">source</a>]

```lua
Spring.AddHeightMap(number, number, number) -> integer?
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`

**Returns**

- `newHeight` `integer?`

### Spring.SetHeightMap {#Spring.SetHeightMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6465-L6477" target="_blank">source</a>]

Can only be called in [Spring.SetHeightMapFunc](Spring.md#Spring.SetHeightMapFunc).

```lua
Spring.SetHeightMap(number, number, number, number?) -> integer?
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`
- `terraform` `number?` — (Default: `1`) Scaling factor.

**Returns**

- `absHeightDiff` `integer?` — If `0`, nothing will be changed (the terraform starts), if `1` the terraform will be finished.

### Spring.SetHeightMapFunc {#Spring.SetHeightMapFunc}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6524-L6542" target="_blank">source</a>]

Example code:

```lua
function Spring.SetHeightMapFunc(function()
  for z=0,Game.mapSizeZ, Game.squareSize do
    for x=0,Game.mapSizeX, Game.squareSize do
      Spring.SetHeightMap( x, z, 200 + 20 * math.cos((x + z) / 90) )
    end
  end
end)
```

```lua
Spring.SetHeightMapFunc(function, [number, ]*) -> integer?
```

**Parameters**

- `luaFunction` `function`
- `...` `number`

**Returns**

- `absTotalHeightMapAmountChanged` `integer?`

### Spring.LevelOriginalHeightMap {#Spring.LevelOriginalHeightMap}
*function*

Set the height of a point in the original map height cache.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6588-L6595" target="_blank">source</a>]

```lua
Spring.LevelOriginalHeightMap(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`

### Spring.LevelOriginalHeightMap (overload 1) {#Spring.LevelOriginalHeightMap-1}
*function*

Set the height of a rectangle area in the original map height cache.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6596-L6605" target="_blank">source</a>]

```lua
Spring.LevelOriginalHeightMap(number, number, number, number, number) -> nil
```

**Parameters**

- `x1` `number`
- `z1` `number`
- `x2` `number`
- `z2` `number`
- `height` `number`

### Spring.AdjustOriginalHeightMap {#Spring.AdjustOriginalHeightMap}
*function*

Add height to a point in the original map height cache.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6624-L6631" target="_blank">source</a>]

```lua
Spring.AdjustOriginalHeightMap(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`

### Spring.AdjustOriginalHeightMap (overload 1) {#Spring.AdjustOriginalHeightMap-1}
*function*

Add height to a rectangle area in the original map height cache.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6632-L6641" target="_blank">source</a>]

```lua
Spring.AdjustOriginalHeightMap(number, number, number, number, number) -> nil
```

**Parameters**

- `x1` `number`
- `z1` `number`
- `x2` `number`
- `z2` `number`
- `height` `number`

### Spring.RevertOriginalHeightMap {#Spring.RevertOriginalHeightMap}
*function*

Restore original map height at a point in the world.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6663-L6670" target="_blank">source</a>]

```lua
Spring.RevertOriginalHeightMap(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`

### Spring.RevertOriginalHeightMap (overload 1) {#Spring.RevertOriginalHeightMap-1}
*function*

Restore original map height over a rectangle in the world.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6671-L6681" target="_blank">source</a>]

```lua
Spring.RevertOriginalHeightMap(number, number, number, number, number?) -> nil
```

**Parameters**

- `x1` `number`
- `z1` `number`
- `x2` `number`
- `z2` `number`
- `height` `number?`

**Returns**

- `nil`

### Spring.AddOriginalHeightMap {#Spring.AddOriginalHeightMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6719-L6729" target="_blank">source</a>]

Can only be called in [Spring.SetOriginalHeightMapFunc](Spring.md#Spring.SetOriginalHeightMapFunc)

```lua
Spring.AddOriginalHeightMap(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `height` `number`

**Returns**

- `nil`

### Spring.SetOriginalHeightMap {#Spring.SetOriginalHeightMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6761-L6772" target="_blank">source</a>]

Can only be called in [Spring.SetOriginalHeightMapFunc](Spring.md#Spring.SetOriginalHeightMapFunc)

```lua
Spring.SetOriginalHeightMap(number, number, number, number?) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `height` `number`
- `factor` `number?`

**Returns**

- `nil`

### Spring.SetOriginalHeightMapFunc {#Spring.SetOriginalHeightMapFunc}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6813-L6821" target="_blank">source</a>]

Cannot recurse on itself

```lua
Spring.SetOriginalHeightMapFunc(function) -> nil
```

**Parameters**

- `heightMapFunc` `function`

**Returns**

- `nil`

### Spring.RebuildSmoothMesh {#Spring.RebuildSmoothMesh}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6865-L6872" target="_blank">source</a>]

Heightmap changes normally take up to 25s to propagate to the smooth mesh.
Use to force a mapwide update immediately.

```lua
Spring.RebuildSmoothMesh() -> nil
```

**Returns**

- `nil`

### Spring.LevelSmoothMesh {#Spring.LevelSmoothMesh}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6880-L6885" target="_blank">source</a>]

```lua
Spring.LevelSmoothMesh(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`

### Spring.LevelSmoothMesh (overload 1) {#Spring.LevelSmoothMesh-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6886-L6893" target="_blank">source</a>]

```lua
Spring.LevelSmoothMesh(number, number, number, number, number) -> nil
```

**Parameters**

- `x1` `number`
- `z1` `number`
- `x2` `number`
- `z2` `number`
- `height` `number`

### Spring.AdjustSmoothMesh {#Spring.AdjustSmoothMesh}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6912-L6917" target="_blank">source</a>]

```lua
Spring.AdjustSmoothMesh(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`

### Spring.AdjustSmoothMesh (overload 1) {#Spring.AdjustSmoothMesh-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6918-L6925" target="_blank">source</a>]

```lua
Spring.AdjustSmoothMesh(number, number, number, number, number) -> nil
```

**Parameters**

- `x1` `number`
- `z1` `number`
- `x2` `number`
- `z2` `number`
- `height` `number`

### Spring.RevertSmoothMesh {#Spring.RevertSmoothMesh}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6942-L6947" target="_blank">source</a>]

```lua
Spring.RevertSmoothMesh(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `z` `number`
- `origFactor` `number`

### Spring.RevertSmoothMesh (overload 1) {#Spring.RevertSmoothMesh-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6948-L6955" target="_blank">source</a>]

```lua
Spring.RevertSmoothMesh(number, number, number, number, number) -> nil
```

**Parameters**

- `x1` `number`
- `z1` `number`
- `x2` `number`
- `z2` `number`
- `origFactor` `number`

### Spring.AddSmoothMesh {#Spring.AddSmoothMesh}
*function*

Can only be called in [Spring.SetSmoothMeshFunc](Spring.md#Spring.SetSmoothMeshFunc).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L6989-L6996" target="_blank">source</a>]

```lua
Spring.AddSmoothMesh(number, number, number) -> number?
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`

**Returns**

- `height` `number?` — The new height, or `nil` if coordinates are invalid.

### Spring.SetSmoothMesh {#Spring.SetSmoothMesh}
*function*

Can only be called in [Spring.SetSmoothMeshFunc](Spring.md#Spring.SetSmoothMeshFunc).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7027-L7035" target="_blank">source</a>]

```lua
Spring.SetSmoothMesh(number, number, number, number?) -> number?
```

**Parameters**

- `x` `number`
- `z` `number`
- `height` `number`
- `terraform` `number?` — (Default: `1`)

**Returns**

- `heightDifference` `number?` — The absolute height difference, or `nil` if coordinates are invalid.

### Spring.SetSmoothMeshFunc {#Spring.SetSmoothMeshFunc}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7075-L7081" target="_blank">source</a>]

```lua
Spring.SetSmoothMeshFunc(function, any, [any, ]*) -> number?
```

**Parameters**

- `luaFunction` `function`
- `arg` `any`
- `...` `any`

**Returns**

- `absTotalHeightMapAmountChanged` `number?`

### Spring.SetMapSquareTerrainType {#Spring.SetMapSquareTerrainType}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7116-L7122" target="_blank">source</a>]

```lua
Spring.SetMapSquareTerrainType(number, number, integer) -> integer?
```

**Parameters**

- `x` `number`
- `z` `number`
- `newType` `integer`

**Returns**

- `oldType` `integer?`

### Spring.SetTerrainTypeData {#Spring.SetTerrainTypeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7146-L7154" target="_blank">source</a>]

```lua
Spring.SetTerrainTypeData(integer, number?, number?, number?, number?) -> boolean?
```

**Parameters**

- `typeIndex` `integer`
- `speedTanks` `number?` — (Default: nil)
- `speedKBOts` `number?` — (Default: nil)
- `speedHovers` `number?` — (Default: nil)
- `speedShips` `number?` — (Default: nil)

**Returns**

- `boolean?` — true

### Spring.SetSquareBuildingMask {#Spring.SetSquareBuildingMask}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7193-L7201" target="_blank">source</a>]

```lua
Spring.SetSquareBuildingMask(integer, integer, integer) -> nil
```

**Parameters**

- `x` `integer`
- `z` `integer`
- `mask` `integer`

**Returns**

- `See` `nil` — also buildingMask unitdef tag.

### Spring.UnitWeaponFire {#Spring.UnitWeaponFire}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7225-L7230" target="_blank">source</a>]

```lua
Spring.UnitWeaponFire(UnitID, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponID` `integer`

**Returns**

- `nil`

### Spring.UnitWeaponHoldFire {#Spring.UnitWeaponHoldFire}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7248-L7253" target="_blank">source</a>]

```lua
Spring.UnitWeaponHoldFire(UnitID, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponID` `integer`

**Returns**

- `nil`

### Spring.ForceUnitCollisionUpdate {#Spring.ForceUnitCollisionUpdate}
*function*

Prevent collision checks from working on outdated data

There's a rare edge case that requires units to be in specific positions
and being shot by specific weapons but which can result in shots ghosting
through the unit. This is because the unit's collision volume is stale.
The `movement.unitQuadPositionUpdateRate` modrule controls this behaviour
and can guarantee 100% correctness if set to 1, but the default value is 3
and large-scale games generally don't want to set it so low. This function
lets you guarantee success for important weapons regardless of how high
the normal update rate is set.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7269-L7283" target="_blank">source</a>]

```lua
Spring.ForceUnitCollisionUpdate(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `nil`

### Spring.UnitAttach {#Spring.UnitAttach}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7296-L7304" target="_blank">source</a>]

```lua
Spring.UnitAttach(UnitID, UnitID, integer, boolean?) -> nil
```

**Parameters**

- `transporterID` [`UnitID`](Aliases.md#UnitID)
- `passengerID` [`UnitID`](Aliases.md#UnitID)
- `pieceNum` `integer`
- `force` `boolean?`

**Returns**

- `nil`

### Spring.UnitDetach {#Spring.UnitDetach}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7338-L7342" target="_blank">source</a>]

```lua
Spring.UnitDetach(UnitID) -> nil
```

**Parameters**

- `passengerID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `nil`

### Spring.UnitDetachFromAir {#Spring.UnitDetachFromAir}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7360-L7364" target="_blank">source</a>]

```lua
Spring.UnitDetachFromAir(UnitID) -> nil
```

**Parameters**

- `passengerID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `nil`

### Spring.SetUnitLoadingTransport {#Spring.SetUnitLoadingTransport}
*function*

Disables collisions between the two units to allow colvol intersection during the approach.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7392-L7398" target="_blank">source</a>]

```lua
Spring.SetUnitLoadingTransport(UnitID, UnitID) -> nil
```

**Parameters**

- `passengerID` [`UnitID`](Aliases.md#UnitID)
- `transportID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `nil`

### Spring.SpawnProjectile {#Spring.SpawnProjectile}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7441-L7447" target="_blank">source</a>]

```lua
Spring.SpawnProjectile(WeaponDefID, ProjectileParams) -> ProjectileID?
```

**Parameters**

- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)
- `projectileParams` [`ProjectileParams`](ProjectileParams.md#ProjectileParams)

**Returns**

- `projectileID` `ProjectileID?`

### Spring.DeleteProjectile {#Spring.DeleteProjectile}
*function*

Silently removes projectiles (no explosion).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7463-L7468" target="_blank">source</a>]

```lua
Spring.DeleteProjectile(ProjectileID) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `nil`

### Spring.SpawnExplosion {#Spring.SpawnExplosion}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7614-L7624" target="_blank">source</a>]

```lua
Spring.SpawnExplosion(number?, number?, number?, number?, number?, number?, ExplosionParams?) -> nil
```

**Parameters**

- `posX` `number?` — (Default: `0`)
- `posY` `number?` — (Default: `0`)
- `posZ` `number?` — (Default: `0`)
- `dirX` `number?` — (Default: `0`)
- `dirY` `number?` — (Default: `0`)
- `dirZ` `number?` — (Default: `0`)
- `explosionParams` `ExplosionParams?`

**Returns**

- `nil`

### Spring.SpawnCEG {#Spring.SpawnCEG}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7686-L7699" target="_blank">source</a>]

```lua
Spring.SpawnCEG(string, number?, number?, number?, number?, number?, number?, number?, number?) -> boolean?, integer
```

**Parameters**

- `cegname` `string`
- `posX` `number?` — (Default: `0`)
- `posY` `number?` — (Default: `0`)
- `posZ` `number?` — (Default: `0`)
- `dirX` `number?` — (Default: `0`)
- `dirY` `number?` — (Default: `0`)
- `dirZ` `number?` — (Default: `0`)
- `radius` `number?` — (Default: `0`)
- `damage` `number?` — (Default: `0`)

**Returns**

- `success` `boolean?`
- `cegID` `integer`

### Spring.SpawnSFX {#Spring.SpawnSFX}
*function*

Equal to the UnitScript versions of EmitSFX, but takes position and direction arguments (in either unit- or piece-space) instead of a piece index.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7727-L7742" target="_blank">source</a>]

```lua
Spring.SpawnSFX(UnitID?, integer?, number?, number?, number?, number?, number?, number?, number?, number?, boolean?) -> boolean?
```

**Parameters**

- `unitID` `UnitID?` — (Default: `0`)
- `sfxID` `integer?` — (Default: `0`)
- `posX` `number?` — (Default: `0`)
- `posY` `number?` — (Default: `0`)
- `posZ` `number?` — (Default: `0`)
- `dirX` `number?` — (Default: `0`)
- `dirY` `number?` — (Default: `0`)
- `dirZ` `number?` — (Default: `0`)
- `radius` `number?` — (Default: `0`)
- `damage` `number?` — (Default: `0`)
- `absolute` `boolean?`

**Returns**

- `success` `boolean?`

### Spring.SetNoPause {#Spring.SetNoPause}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7767-L7771" target="_blank">source</a>]

```lua
Spring.SetNoPause(boolean) -> nil
```

**Parameters**

- `noPause` `boolean`

**Returns**

- `nil`

### Spring.SetExperienceGrade {#Spring.SetExperienceGrade}
*function*

Defines how often `Callins.UnitExperience` will be called.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7785-L7793" target="_blank">source</a>]

```lua
Spring.SetExperienceGrade(number, number?, number?, number?) -> nil
```

**Parameters**

- `expGrade` `number`
- `ExpPowerScale` `number?`
- `ExpHealthScale` `number?`
- `ExpReloadScale` `number?`

**Returns**

- `nil`

### Spring.SetRadarErrorParams {#Spring.SetRadarErrorParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7816-L7824" target="_blank">source</a>]

```lua
Spring.SetRadarErrorParams(AllyTeamID, number, number?, number?) -> nil
```

**Parameters**

- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `allyteamErrorSize` `number`
- `baseErrorSize` `number?`
- `baseErrorMult` `number?`

**Returns**

- `nil`

### Spring.EditUnitCmdDesc {#Spring.EditUnitCmdDesc}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7951-L7956" target="_blank">source</a>]

```lua
Spring.EditUnitCmdDesc(UnitID, integer, CommandDescription) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `cmdDescID` `integer`
- `cmdArray` [`CommandDescription`](CommandDescription.md#CommandDescription)

### Spring.InsertUnitCmdDesc {#Spring.InsertUnitCmdDesc}
*function*

Insert a command description at a specific index.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7983-L7990" target="_blank">source</a>]

```lua
Spring.InsertUnitCmdDesc(UnitID, integer, CommandDescription) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `index` `integer`
- `cmdDesc` [`CommandDescription`](CommandDescription.md#CommandDescription)

### Spring.InsertUnitCmdDesc (overload 1) {#Spring.InsertUnitCmdDesc-1}
*function*

Insert a command description at the last position.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7991-L7997" target="_blank">source</a>]

```lua
Spring.InsertUnitCmdDesc(UnitID, CommandDescription) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `cmdDesc` [`CommandDescription`](CommandDescription.md#CommandDescription)

### Spring.RemoveUnitCmdDesc {#Spring.RemoveUnitCmdDesc}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L8032-L8036" target="_blank">source</a>]

```lua
Spring.RemoveUnitCmdDesc(UnitID, integer?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `cmdDescID` `integer?`

### Spring.IsCheatingEnabled {#Spring.IsCheatingEnabled}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L774-L779" target="_blank">source</a>]

```lua
Spring.IsCheatingEnabled() -> boolean
```

**Returns**

- `enabled` `boolean`

### Spring.IsGodModeEnabled {#Spring.IsGodModeEnabled}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L787-L792" target="_blank">source</a>]

```lua
Spring.IsGodModeEnabled() -> boolean
```

**Returns**

- `enabled` `boolean`

### Spring.IsDevLuaEnabled {#Spring.IsDevLuaEnabled}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L802-L807" target="_blank">source</a>]

```lua
Spring.IsDevLuaEnabled() -> boolean
```

**Returns**

- `enabled` `boolean`

### Spring.IsEditDefsEnabled {#Spring.IsEditDefsEnabled}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L815-L820" target="_blank">source</a>]

```lua
Spring.IsEditDefsEnabled() -> boolean
```

**Returns**

- `enabled` `boolean`

### Spring.IsNoCostEnabled {#Spring.IsNoCostEnabled}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L828-L833" target="_blank">source</a>]

```lua
Spring.IsNoCostEnabled() -> boolean
```

**Returns**

- `enabled` `boolean`

### Spring.GetGlobalLos {#Spring.GetGlobalLos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L841-L848" target="_blank">source</a>]

```lua
Spring.GetGlobalLos(TeamID?) -> boolean
```

**Parameters**

- `teamID` `TeamID?`

**Returns**

- `enabled` `boolean`

### Spring.AreHelperAIsEnabled {#Spring.AreHelperAIsEnabled}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L860-L865" target="_blank">source</a>]

```lua
Spring.AreHelperAIsEnabled() -> boolean
```

**Returns**

- `enabled` `boolean`

### Spring.FixedAllies {#Spring.FixedAllies}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L873-L878" target="_blank">source</a>]

```lua
Spring.FixedAllies() -> boolean?
```

**Returns**

- `enabled` `boolean?`

### Spring.IsGameOver {#Spring.IsGameOver}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L886-L891" target="_blank">source</a>]

```lua
Spring.IsGameOver() -> boolean
```

**Returns**

- `isGameOver` `boolean`

### Spring.GetGameFrame {#Spring.GetGameFrame}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L908-L914" target="_blank">source</a>]

```lua
Spring.GetGameFrame() -> integer, integer
```

**Returns**

- `t1` `integer` — frameNum % dayFrames
- `t2` `integer` — frameNum / dayFrames

### Spring.GetGameSeconds {#Spring.GetGameSeconds}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L926-L931" target="_blank">source</a>]

```lua
Spring.GetGameSeconds() -> number
```

**Returns**

- `seconds` `number`

### Spring.GetTidal {#Spring.GetTidal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L945-L950" target="_blank">source</a>]

```lua
Spring.GetTidal() -> number
```

**Returns**

- `tidalStrength` `number`

### Spring.GetWind {#Spring.GetWind}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L958-L969" target="_blank">source</a>]

```lua
Spring.GetWind() -> number, number, number, number, number, number, number
```

**Returns**

- `windSpeedX` `number`
- `windSpeedY` `number` — (Always 0)
- `windSpeedZ` `number`
- `windStrength` `number` — (Length of windSpeed)
- `windDirX` `number` — (Normalized windSpeed)
- `windDirY` `number` — (Always 0)
- `windDirZ` `number`

### Spring.GetGameRulesParams {#Spring.GetGameRulesParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L996-L1001" target="_blank">source</a>]

```lua
Spring.GetGameRulesParams() -> RulesParams
```

**Returns**

- `rulesParams` [`RulesParams`](RulesParams.md#RulesParams) — map with rules names as key and values as values

### Spring.GetTeamRulesParams {#Spring.GetTeamRulesParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1009-L1016" target="_blank">source</a>]

```lua
Spring.GetTeamRulesParams(TeamID) -> RulesParams
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `rulesParams` [`RulesParams`](RulesParams.md#RulesParams) — map with rules names as key and values as values

### Spring.GetPlayerRulesParams {#Spring.GetPlayerRulesParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1035-L1042" target="_blank">source</a>]

```lua
Spring.GetPlayerRulesParams(PlayerID) -> RulesParams
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)

**Returns**

- `rulesParams` [`RulesParams`](RulesParams.md#RulesParams) — map with rules names as key and values as values

### Spring.GetUnitRulesParams {#Spring.GetUnitRulesParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1104-L1111" target="_blank">source</a>]

```lua
Spring.GetUnitRulesParams(UnitID) -> RulesParams
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `rulesParams` [`RulesParams`](RulesParams.md#RulesParams) — map with rules names as key and values as values

### Spring.GetFeatureRulesParams {#Spring.GetFeatureRulesParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1122-L1129" target="_blank">source</a>]

```lua
Spring.GetFeatureRulesParams(FeatureID) -> RulesParams
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `rulesParams` [`RulesParams`](RulesParams.md#RulesParams) — map with rules names as key and values as values

### Spring.GetGameRulesParam {#Spring.GetGameRulesParam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1158-L1165" target="_blank">source</a>]

```lua
Spring.GetGameRulesParam(string) -> (number|boolean|string)?
```

**Parameters**

- `name` `string` — rules-parameter key (only this argument is read)

**Returns**

- `value` `(number|boolean|string)?`

### Spring.GetTeamRulesParam {#Spring.GetTeamRulesParam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1173-L1181" target="_blank">source</a>]

```lua
Spring.GetTeamRulesParam(TeamID, (number|string)) -> (number|string)?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `ruleRef` `(number|string)` — the rule index or name

**Returns**

- `value` `(number|string)?`

### Spring.GetPlayerRulesParam {#Spring.GetPlayerRulesParam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1201-L1209" target="_blank">source</a>]

```lua
Spring.GetPlayerRulesParam(PlayerID, (number|string)) -> (number|string)?
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `ruleRef` `(number|string)` — the rule index or name

**Returns**

- `value` `(number|string)?`

### Spring.GetUnitRulesParam {#Spring.GetUnitRulesParam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1232-L1240" target="_blank">source</a>]

```lua
Spring.GetUnitRulesParam(UnitID, (number|string)) -> (number|string)?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `ruleRef` `(number|string)` — the rule index or name

**Returns**

- `value` `(number|string)?`

### Spring.GetFeatureRulesParam {#Spring.GetFeatureRulesParam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1251-L1259" target="_blank">source</a>]

```lua
Spring.GetFeatureRulesParam(FeatureID, (number|string)) -> (number|string)?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `ruleRef` `(number|string)` — the rule index or name

**Returns**

- `value` `(number|string)?`

### Spring.GetMapOption {#Spring.GetMapOption}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1327-L1334" target="_blank">source</a>]

```lua
Spring.GetMapOption(string) -> string
```

**Parameters**

- `mapOption` `string`

**Returns**

- `value` `string` — Value of `modOption`.

### Spring.GetMapOptions {#Spring.GetMapOptions}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1339-L1344" target="_blank">source</a>]

```lua
Spring.GetMapOptions() -> table<string,string>
```

**Returns**

- `mapOptions` `table<string,string>` — Table with options names as keys and values as values.

### Spring.GetModOption {#Spring.GetModOption}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1351-L1358" target="_blank">source</a>]

```lua
Spring.GetModOption(string) -> string
```

**Parameters**

- `modOption` `string`

**Returns**

- `value` `string` — Value of `modOption`.

### Spring.GetModOptions {#Spring.GetModOptions}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1365-L1370" target="_blank">source</a>]

```lua
Spring.GetModOptions() -> table<string,string>
```

**Returns**

- `modOptions` `table<string,string>` — Table with options names as keys and values as values.

### Spring.GetHeadingFromVector {#Spring.GetHeadingFromVector}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1384-L1392" target="_blank">source</a>]

```lua
Spring.GetHeadingFromVector(number, number) -> integer
```

**Parameters**

- `x` `number`
- `z` `number`

**Returns**

- `heading` `integer`

### Spring.GetVectorFromHeading {#Spring.GetVectorFromHeading}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1403-L1411" target="_blank">source</a>]

```lua
Spring.GetVectorFromHeading(integer) -> number, number
```

**Parameters**

- `heading` `integer`

**Returns**

- `x` `number`
- `z` `number`

### Spring.GetFacingFromHeading {#Spring.GetFacingFromHeading}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1421-L1425" target="_blank">source</a>]

```lua
Spring.GetFacingFromHeading(integer) -> FacingInteger
```

**Parameters**

- `heading` `integer`

**Returns**

- `facing` [`FacingInteger`](Aliases.md#FacingInteger)

### Spring.GetHeadingFromFacing {#Spring.GetHeadingFromFacing}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1432-L1436" target="_blank">source</a>]

```lua
Spring.GetHeadingFromFacing(FacingInteger) -> integer
```

**Parameters**

- `facing` [`FacingInteger`](Aliases.md#FacingInteger)

**Returns**

- `heading` `integer`

### Spring.GetSideData {#Spring.GetSideData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1465-L1471" target="_blank">source</a>]

```lua
Spring.GetSideData(string) -> string?, string?
```

**Parameters**

- `sideName` `string` — Case-insensitive side name.

**Returns**

- `startUnit` `string?`
- `caseName` `string?` — Original case side name.

### Spring.GetSideData (overload 1) {#Spring.GetSideData-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1473-L1479" target="_blank">source</a>]

```lua
Spring.GetSideData(integer) -> string?, string?, string?
```

**Parameters**

- `sideID` `integer`

**Returns**

- `sideName` `string?` — Lowercase side name.
- `startUnit` `string?`
- `caseName` `string?` — Original case side name.

### Spring.GetSideData (overload 2) {#Spring.GetSideData-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1481-L1484" target="_blank">source</a>]

```lua
Spring.GetSideData() -> SideSpec[]
```

**Returns**

- `sideArray` `SideSpec[]`

### Spring.GetGaiaTeamID {#Spring.GetGaiaTeamID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1531-L1536" target="_blank">source</a>]

```lua
Spring.GetGaiaTeamID() -> TeamID
```

**Returns**

- `teamID` [`TeamID`](Aliases.md#TeamID)

### Spring.GetAllyTeamStartBox {#Spring.GetAllyTeamStartBox}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1547-L1557" target="_blank">source</a>]

```lua
Spring.GetAllyTeamStartBox(AllyTeamID) -> number?, number?, number?, number?
```

**Parameters**

- `allyID` [`AllyTeamID`](Aliases.md#AllyTeamID)

**Returns**

- `xMin` `number?`
- `zMin` `number?`
- `xMax` `number?`
- `zMax` `number?`

### Spring.GetTeamStartPosition {#Spring.GetTeamStartPosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1579-L1588" target="_blank">source</a>]

```lua
Spring.GetTeamStartPosition(TeamID) -> number?, number?, number?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `x` `number?`
- `y` `number?`
- `x` `number?`

### Spring.GetMapStartPositions {#Spring.GetMapStartPositions}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1607-L1611" target="_blank">source</a>]

```lua
Spring.GetMapStartPositions() -> float3[]
```

**Returns**

- `startPositions` `float3[]` — array of positions indexed by teamID

### Spring.GetAllyTeamList {#Spring.GetAllyTeamList}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1633-L1637" target="_blank">source</a>]

```lua
Spring.GetAllyTeamList() -> AllyTeamID[]
```

**Returns**

- `allyTeamIDs` `AllyTeamID[]`

### Spring.GetTeamList {#Spring.GetTeamList}
*function*

Get all team IDs.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1653-L1659" target="_blank">source</a>]

```lua
Spring.GetTeamList(unknown) -> TeamID[]
```

**Parameters**

- `allyTeamID` `unknown` — (Default: `-1`)

**Returns**

- `teamIDs` `TeamID[]` — List of team IDs.

### Spring.GetTeamList (overload 1) {#Spring.GetTeamList-1}
*function*

Get team IDs in a specific ally team.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1661-L1667" target="_blank">source</a>]

```lua
Spring.GetTeamList(AllyTeamID) -> TeamID[]?
```

**Parameters**

- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID) — The ally team ID to filter teams by. A value less than 0 will return all teams.

**Returns**

- `teamIDs` `TeamID[]?` — List of team IDs or `nil` if `allyTeamID` is invalid.

### Spring.GetPlayerList {#Spring.GetPlayerList}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1700-L1706" target="_blank">source</a>]

```lua
Spring.GetPlayerList(TeamID?, boolean?) -> PlayerID[]?
```

**Parameters**

- `teamID` `TeamID?` — (Default: `-1`) to filter by when >= 0
- `active` `boolean?` — (Default: `false`) whether to filter only active teams

**Returns**

- `playerIDs` `PlayerID[]?` — List of playerIDs.

### Spring.GetTeamInfo {#Spring.GetTeamInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1754-L1767" target="_blank">source</a>]

```lua
Spring.GetTeamInfo(TeamID, boolean?) -> TeamID?, PlayerID, number, number, string, AllyTeamID, number, table<string,string>
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `getTeamKeys` `boolean?` — (Default: `true`) whether to return the customTeamKeys table

**Returns**

- `teamID` `TeamID?`
- `leader` [`PlayerID`](Aliases.md#PlayerID)
- `isDead` `number`
- `hasAI` `number`
- `side` `string`
- `allyTeam` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `incomeMultiplier` `number`
- `customTeamKeys` `table<string,string>` — when getTeamKeys is true, otherwise nil

### Spring.GetTeamAllyTeamID {#Spring.GetTeamAllyTeamID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1805-L1810" target="_blank">source</a>]

```lua
Spring.GetTeamAllyTeamID(TeamID) -> AllyTeamID?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `allyTeamID` `AllyTeamID?`

### Spring.GetTeamResources {#Spring.GetTeamResources}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1826-L1840" target="_blank">source</a>]

```lua
Spring.GetTeamResources(TeamID, ResourceName) -> number?, number, number, number, number, number, number, number, number
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `resource` [`ResourceName`](Aliases.md#ResourceName)

**Returns**

- `currentLevel` `number?` — The current amount of the resource that the team has in storage at this moment
- `storage` `number` — The maximum storage capacity for the resource.
- `pull` `number` — The total amount of the resource that is being requested/used by all units and buildings per second, regardless of whether the resource is actually available.
- `income` `number` — The total amount of the resource being generated per second from all sources (e.g., mines, generators, reclaiming, etc.).
- `expense` `number` — The total amount of the resource actually being spent per second. This is the real consumption, which may be less than pull if there isn’t enough resource available.
- `share` `number` — The fraction (0.0 to 1.0) of the storage that the team is sharing with allied teams. A value of 0.0 means 100% of storage is shared, while 1.0 means only any excess is shared.
- `sent` `number` — The total amount of the resource that has actually been sent to allies (via sharing or manual transfer).
- `received` `number` — The total amount of the resource that has actually been received from allies (via sharing or manual transfer).
- `excess` `number` — The amount of the resource that was lost due to storage overflow (wasted).

### Spring.GetTeamUnitStats {#Spring.GetTeamUnitStats}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1885-L1895" target="_blank">source</a>]

```lua
Spring.GetTeamUnitStats(TeamID) -> integer?, integer, integer, integer, integer, integer
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `killed` `integer?`
- `died` `integer`
- `capturedBy` `integer`
- `capturedFrom` `integer`
- `received` `integer`
- `sent` `integer`

### Spring.GetTeamResourceStats {#Spring.GetTeamResourceStats}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1920-L1930" target="_blank">source</a>]

```lua
Spring.GetTeamResourceStats(TeamID, ResourceName) -> number?, number, number, number, number
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `resource` [`ResourceName`](Aliases.md#ResourceName)

**Returns**

- `used` `number?`
- `produced` `number`
- `excessed` `number`
- `received` `number`
- `sent` `number`

### Spring.GetTeamDamageStats {#Spring.GetTeamDamageStats}
*function*

Gets team damage dealt/received totals

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L1969-L1979" target="_blank">source</a>]

Returns a team's damage stats. Note that all damage is counted,
including self-inflicted and unconfirmed out-of-sight.

```lua
Spring.GetTeamDamageStats(TeamID) -> number, number
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `damageDealt` `number`
- `damageReceived` `number`

### Spring.GetTeamStatsHistory {#Spring.GetTeamStatsHistory}
*function*

Get the number of history entries.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2025-L2030" target="_blank">source</a>]

```lua
Spring.GetTeamStatsHistory(TeamID) -> integer?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `historyCount` `integer?` — The number of history entries, or `nil` if unable to resolve team.

### Spring.GetTeamStatsHistory (overload 1) {#Spring.GetTeamStatsHistory-1}
*function*

Get team stats history.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2031-L2038" target="_blank">source</a>]

```lua
Spring.GetTeamStatsHistory(TeamID, integer, integer?) -> TeamStats[]
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `startIndex` `integer`
- `endIndex` `integer?` — (Default: startIndex)

**Returns**

- `teamStatsHistory` `TeamStats[]` — The team stats history, or `nil` if unable to resolve team.

### Spring.GetTeamLuaAI {#Spring.GetTeamLuaAI}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2124-L2129" target="_blank">source</a>]

```lua
Spring.GetTeamLuaAI(TeamID) -> string
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `string`

### Spring.GetTeamMaxUnits {#Spring.GetTeamMaxUnits}
*function*

Returns a team's unit cap.

Also returns the current unit count for readable teams as the 2nd value.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2157-L2165" target="_blank">source</a>]

```lua
Spring.GetTeamMaxUnits(TeamID) -> integer, integer?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `maxUnits` `integer`
- `currentUnits` `integer?`

### Spring.GetPlayerInfo {#Spring.GetPlayerInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2182-L2199" target="_blank">source</a>]

```lua
Spring.GetPlayerInfo(PlayerID, boolean?) -> string, boolean, boolean, TeamID, AllyTeamID, number, number, string, integer, boolean, { [string]: string }, boolean
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `getPlayerOpts` `boolean?` — (Default: `true`) whether to return custom player options

**Returns**

- `name` `string`
- `active` `boolean`
- `spectator` `boolean`
- `teamID` [`TeamID`](Aliases.md#TeamID)
- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `pingTime` `number`
- `cpuUsage` `number`
- `country` `string`
- `rank` `integer`
- `hasSkirmishAIsInTeam` `boolean`
- `playerOpts` `{ [string]: string }` — when playerOpts is true
- `desynced` `boolean`

### Spring.GetPlayerControlledUnit {#Spring.GetPlayerControlledUnit}
*function*

Returns unit controlled by player on FPS mode

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2247-L2252" target="_blank">source</a>]

```lua
Spring.GetPlayerControlledUnit(PlayerID) -> UnitID?
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)

**Returns**

- `UnitID?`

### Spring.GetAIInfo {#Spring.GetAIInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2283-L2293" target="_blank">source</a>]

```lua
Spring.GetAIInfo(TeamID) -> integer, string, PlayerID, string, string, table<string,string>
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `skirmishAIID` `integer`
- `name` `string`
- `hostingPlayerID` [`PlayerID`](Aliases.md#PlayerID)
- `shortName` `string` — When synced `"SYNCED_NOSHORTNAME"`, otherwise the AI shortname or `"UNKNOWN"`.
- `version` `string` — When synced `"SYNCED_NOVERSION"`, otherwise the AI version or `"UNKNOWN"`.
- `options` `table<string,string>`

### Spring.GetAllyTeamInfo {#Spring.GetAllyTeamInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2342-L2347" target="_blank">source</a>]

```lua
Spring.GetAllyTeamInfo(AllyTeamID) -> table<string,string>?
```

**Parameters**

- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)

**Returns**

- `table<string,string>?`

### Spring.AreTeamsAllied {#Spring.AreTeamsAllied}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2368-L2374" target="_blank">source</a>]

```lua
Spring.AreTeamsAllied(TeamID, TeamID) -> boolean?
```

**Parameters**

- `teamID1` [`TeamID`](Aliases.md#TeamID)
- `teamID2` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `boolean?`

### Spring.ArePlayersAllied {#Spring.ArePlayersAllied}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2388-L2394" target="_blank">source</a>]

```lua
Spring.ArePlayersAllied(PlayerID, PlayerID) -> boolean?
```

**Parameters**

- `playerID1` [`PlayerID`](Aliases.md#PlayerID)
- `playerID2` [`PlayerID`](Aliases.md#PlayerID)

**Returns**

- `boolean?`

### Spring.GetAllUnits {#Spring.GetAllUnits}
*function*

Get a list of all unitIDs

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2424-L2437" target="_blank">source</a>]

Note that when called from a widget, this also returns units that are only
radar blips.

For units that are radar blips, you may want to check if they are in los,
as GetUnitDefID() will still return true if they have previously been seen.

**See:** UnsyncedRead.GetVisibleUnits

```lua
Spring.GetAllUnits() -> UnitID[]
```

**Returns**

- `unitIDs` `UnitID[]`

### Spring.GetTeamUnits {#Spring.GetTeamUnits}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2462-L2467" target="_blank">source</a>]

```lua
Spring.GetTeamUnits(TeamID) -> UnitID[]?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `unitIDs` `UnitID[]?`

### Spring.GetTeamUnitsSorted {#Spring.GetTeamUnitsSorted}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2562-L2567" target="_blank">source</a>]

```lua
Spring.GetTeamUnitsSorted(TeamID) -> table<UnitDefID,UnitID[]>
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `unitsByDef` `table<UnitDefID,UnitID[]>` — A table where keys are unitDefIDs and values are arrays of unitIDs

### Spring.GetTeamUnitsCounts {#Spring.GetTeamUnitsCounts}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2658-L2663" target="_blank">source</a>]

```lua
Spring.GetTeamUnitsCounts(TeamID) -> table<UnitDefID,integer>?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `countByUnit` `table<UnitDefID,integer>?` — A table where keys are unitDefIDs and values are counts.

### Spring.GetTeamUnitsByDefs {#Spring.GetTeamUnitsByDefs}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2741-L2747" target="_blank">source</a>]

```lua
Spring.GetTeamUnitsByDefs(TeamID, (UnitDefID|UnitDefID[])) -> UnitID[]?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `unitDefIDs` `(UnitDefID|UnitDefID[])`

**Returns**

- `unitIDs` `UnitID[]?`

### Spring.GetTeamUnitDefCount {#Spring.GetTeamUnitDefCount}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2817-L2823" target="_blank">source</a>]

```lua
Spring.GetTeamUnitDefCount(TeamID, UnitDefID) -> integer?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)

**Returns**

- `count` `integer?`

### Spring.GetTeamUnitCount {#Spring.GetTeamUnitCount}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2878-L2883" target="_blank">source</a>]

```lua
Spring.GetTeamUnitCount(TeamID) -> integer?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `count` `integer?`

### Spring.GetUnitsInRectangle {#Spring.GetUnitsInRectangle}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L2981-L2990" target="_blank">source</a>]

```lua
Spring.GetUnitsInRectangle(number, number, number, number, integer?) -> UnitID[]
```

**Parameters**

- `xmin` `number`
- `zmin` `number`
- `xmax` `number`
- `zmax` `number`
- `allegiance` `integer?`

**Returns**

- `unitIDs` `UnitID[]`

### Spring.GetUnitsInBox {#Spring.GetUnitsInBox}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3027-L3038" target="_blank">source</a>]

```lua
Spring.GetUnitsInBox(number, number, number, number, number, number, integer?) -> UnitID[]
```

**Parameters**

- `xmin` `number`
- `ymin` `number`
- `zmin` `number`
- `xmax` `number`
- `ymax` `number`
- `zmax` `number`
- `allegiance` `integer?`

**Returns**

- `unitIDs` `UnitID[]`

### Spring.GetUnitsInCylinder {#Spring.GetUnitsInCylinder}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3072-L3080" target="_blank">source</a>]

```lua
Spring.GetUnitsInCylinder(number, number, number, TeamID?) -> UnitID[]
```

**Parameters**

- `x` `number`
- `z` `number`
- `radius` `number`
- `teamID` `TeamID?` — filter by team, defaults to all units

**Returns**

- `unitIDs` `UnitID[]`

### Spring.GetUnitsInSphere {#Spring.GetUnitsInSphere}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3113-L3121" target="_blank">source</a>]

```lua
Spring.GetUnitsInSphere(number, number, number, number) -> UnitID[]
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`
- `radius` `number`

**Returns**

- `unitIDs` `UnitID[]`

### Spring.GetUnitsInPlanes {#Spring.GetUnitsInPlanes}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3180-L3195" target="_blank">source</a>]

Plane normals point towards accepted space, so the acceptance criteria for each plane is:

```
radius     = unit radius
px, py, pz = unit position
[(nx * px) + (ny * py) + (nz * pz) + (d - radius)]  <=  0
```

```lua
Spring.GetUnitsInPlanes(Plane[], integer?) -> UnitID[]
```

**Parameters**

- `planes` `Plane[]`
- `allegiance` `integer?`

**Returns**

- `unitIDs` `UnitID[]`

### Spring.GetUnitArrayCentroid {#Spring.GetUnitArrayCentroid}
*function*

Returns the centroid of an array of units

Returns nil for an empty array

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3284-L3293" target="_blank">source</a>]

```lua
Spring.GetUnitArrayCentroid(table) -> number, number, number
```

**Parameters**

- `units` `table` — { unitID, unitID, ... }

**Returns**

- `centerX` `number`
- `centerY` `number`
- `centerZ` `number`

### Spring.GetUnitMapCentroid {#Spring.GetUnitMapCentroid}
*function*

Returns the centroid of a map of units

Returns nil for an empty map

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3299-L3308" target="_blank">source</a>]

```lua
Spring.GetUnitMapCentroid(table) -> number, number, number
```

**Parameters**

- `units` `table` — { [unitID] = true, [unitID] = true, ... }

**Returns**

- `centerX` `number`
- `centerY` `number`
- `centerZ` `number`

### Spring.GetUnitNearestAlly {#Spring.GetUnitNearestAlly}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3315-L3321" target="_blank">source</a>]

```lua
Spring.GetUnitNearestAlly(UnitID, number?) -> UnitID?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `range` `number?` — (Default: `1.0e9`)

**Returns**

- `unitID` `UnitID?`

### Spring.GetUnitNearestEnemy {#Spring.GetUnitNearestEnemy}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3340-L3349" target="_blank">source</a>]

```lua
Spring.GetUnitNearestEnemy(UnitID, number?, boolean?, boolean?, boolean?) -> UnitID?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `range` `number?` — (Default: `1.0e9`) range of the search.
- `useLOS` `boolean?` — (Default: `true`) requires LOS/radar visibility of allied team.
- `sphereDistTest` `boolean?` — (Default: `false`) determines if using spherical(3D, includes target radius) or cylindrical(2D) search.
- `checkSightDist` `boolean?` — (Default: `false`) determine if during filter process, if candidate distance to be within candidate LOS radius.

**Returns**

- `unitID` `UnitID?`

### Spring.GetClosestEnemyUnit {#Spring.GetClosestEnemyUnit}
*function*

Returns the enemy unit closest to a position.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3375-L3387" target="_blank">source</a>]

```lua
Spring.GetClosestEnemyUnit(number, number, number, number?, AllyTeamID?, boolean?, boolean?, boolean?) -> UnitID?
```

**Parameters**

- `x` `number` — x coordinate of query position
- `y` `number` — y coordinate of query position
- `z` `number` — z coordinate of query position
- `range` `number?` — (Default: `1.0e9`)
- `allyTeamID` `AllyTeamID?` — whose enemies to consider, always own in non-full-read contexts
- `useLOS` `boolean?` — (Default: true) requires LOS/radar visibility or not. Always true in non-full-read contexts
- `sphereDistTest` `boolean?` — (Default: `false`) For non-LOS mode only. Determines if using spherical(3D, includes target radius) or cylindrical(2D) search
- `checkSightDist` `boolean?` — (Default: `false`) For non-LOS mode only. Determine if during filter process, if candidate distance to be within candidate LOS radius

**Returns**

- `unitID` `UnitID?`

### Spring.GetFeaturesInRectangle {#Spring.GetFeaturesInRectangle}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3460-L3468" target="_blank">source</a>]

```lua
Spring.GetFeaturesInRectangle(number, number, number, number) -> FeatureID[]
```

**Parameters**

- `xmin` `number`
- `zmin` `number`
- `xmax` `number`
- `zmax` `number`

**Returns**

- `featureIDs` `FeatureID[]`

### Spring.GetFeaturesInSphere {#Spring.GetFeaturesInSphere}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3486-L3494" target="_blank">source</a>]

```lua
Spring.GetFeaturesInSphere(number, number, number, number) -> FeatureID[]
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`
- `radius` `number`

**Returns**

- `featureIDs` `FeatureID[]`

### Spring.GetFeaturesInCylinder {#Spring.GetFeaturesInCylinder}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3511-L3519" target="_blank">source</a>]

```lua
Spring.GetFeaturesInCylinder(number, number, number, integer?) -> FeatureID[]
```

**Parameters**

- `x` `number`
- `z` `number`
- `radius` `number`
- `allegiance` `integer?`

**Returns**

- `featureIDs` `FeatureID[]`

### Spring.GetAllProjectiles {#Spring.GetAllProjectiles}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3579-L3585" target="_blank">source</a>]

```lua
Spring.GetAllProjectiles(boolean?, boolean?) -> ProjectileID[]
```

**Parameters**

- `excludeWeaponProjectiles` `boolean?` — (Default: `false`)
- `excludePieceProjectiles` `boolean?` — (Default: `false`)

**Returns**

- `projectileIDs` `ProjectileID[]`

### Spring.GetProjectilesInRectangle {#Spring.GetProjectilesInRectangle}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3595-L3605" target="_blank">source</a>]

```lua
Spring.GetProjectilesInRectangle(number, number, number, number, boolean?, boolean?) -> ProjectileID[]
```

**Parameters**

- `xmin` `number`
- `zmin` `number`
- `xmax` `number`
- `zmax` `number`
- `excludeWeaponProjectiles` `boolean?` — (Default: `false`)
- `excludePieceProjectiles` `boolean?` — (Default: `false`)

**Returns**

- `projectileIDs` `ProjectileID[]`

### Spring.GetProjectilesInSphere {#Spring.GetProjectilesInSphere}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3625-L3635" target="_blank">source</a>]

```lua
Spring.GetProjectilesInSphere(number, number, number, number, boolean?, boolean?) -> ProjectileID[]
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`
- `radius` `number`
- `excludeWeaponProjectiles` `boolean?` — (Default: false)
- `excludePieceProjectiles` `boolean?` — (Default: false)

**Returns**

- `projectileIDs` `ProjectileID[]`

### Spring.ValidUnitID {#Spring.ValidUnitID}
*function*

Get whether a unitID is valid

Dead units are not valid.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3657-L3664" target="_blank">source</a>]

```lua
Spring.ValidUnitID(UnitID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `boolean`

### Spring.GetUnitStates {#Spring.GetUnitStates}
*function*

Gets various states for the given unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3687-L3709" target="_blank">source</a>]

```lua
Spring.GetUnitStates(UnitID, false, true, true) -> number, number, number, boolean, boolean, boolean, boolean, boolean?, boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `retTable` `false` — Return a table instead of multiple values. Defaults to `true`
- `binState` `true` — Include binary state (activated, etc)? Defaults to `retTable`
- `amtState` `true` — Include Air/Hover MoveType state if available? Defaults to `retTable`

**Returns**

- `fireState` `number`
- `moveState` `number`
- `autorepairlevel` `number` — `-1` if not set
- `repeat` `boolean`
- `cloak` `boolean`
- `active` `boolean`
- `trajectory` `boolean`
- `autoLand` `boolean?`
- `loopbackAttack` `boolean?`

### Spring.GetUnitArmored {#Spring.GetUnitArmored}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3797-L3803" target="_blank">source</a>]

```lua
Spring.GetUnitArmored(UnitID) -> boolean?, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `armored` `boolean?`
- `armorMultiple` `number`

### Spring.GetUnitIsActive {#Spring.GetUnitIsActive}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3816-L3821" target="_blank">source</a>]

```lua
Spring.GetUnitIsActive(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `isActive` `boolean?`

### Spring.GetUnitIsCloaked {#Spring.GetUnitIsCloaked}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3833-L3838" target="_blank">source</a>]

```lua
Spring.GetUnitIsCloaked(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `isCloaked` `boolean?`

### Spring.GetUnitSeismicSignature {#Spring.GetUnitSeismicSignature}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3850-L3855" target="_blank">source</a>]

```lua
Spring.GetUnitSeismicSignature(UnitID) -> number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `seismicSignature` `number?`

### Spring.GetUnitLeavesGhost {#Spring.GetUnitLeavesGhost}
*function*

Get whether unit leaves static radar ghosts.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3866-L3871" target="_blank">source</a>]

```lua
Spring.GetUnitLeavesGhost() -> number?
```

**Returns**

- `number?`

### Spring.GetUnitSelfDTime {#Spring.GetUnitSelfDTime}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3882-L3887" target="_blank">source</a>]

```lua
Spring.GetUnitSelfDTime(UnitID) -> integer?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `selfDTime` `integer?`

### Spring.GetUnitStockpile {#Spring.GetUnitStockpile}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3899-L3906" target="_blank">source</a>]

```lua
Spring.GetUnitStockpile(UnitID) -> integer?, integer?, number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `numStockpiled` `integer?`
- `numStockpileQued` `integer?`
- `buildPercent` `number?`

### Spring.GetUnitSensorRadius {#Spring.GetUnitSensorRadius}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3923-L3929" target="_blank">source</a>]

```lua
Spring.GetUnitSensorRadius(UnitID, string) -> integer?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `type` `string` — one of los, airLos, radar, sonar, seismic, radarJammer, sonarJammer

**Returns**

- `radius` `integer?`

### Spring.GetUnitPosErrorParams {#Spring.GetUnitPosErrorParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L3966-L3979" target="_blank">source</a>]

```lua
Spring.GetUnitPosErrorParams(UnitID, AllyTeamID?) -> number?, number, number, number, number, number, integer, boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `allyTeamID` `AllyTeamID?`

**Returns**

- `posErrorVectorX` `number?`
- `posErrorVectorY` `number`
- `posErrorVectorZ` `number`
- `posErrorDeltaX` `number`
- `posErrorDeltaY` `number`
- `posErrorDeltaZ` `number`
- `nextPosErrorUpdate` `integer`
- `posErrorBit` `boolean`

### Spring.GetUnitTooltip {#Spring.GetUnitTooltip}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4003-L4008" target="_blank">source</a>]

```lua
Spring.GetUnitTooltip(UnitID) -> string?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `string?`

### Spring.GetUnitDefID {#Spring.GetUnitDefID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4043-L4048" target="_blank">source</a>]

```lua
Spring.GetUnitDefID(UnitID) -> UnitDefID?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `UnitDefID?`

### Spring.GetUnitMoveDefID {#Spring.GetUnitMoveDefID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4067-L4080" target="_blank">source</a>]

Returns a numerical movedef ID and its name. For things that have
no movedef, returns `false` (to tell them apart from unreadable
units while keeping the `if not x` pattern usable). For now, the
numerical ID is not too useful so you can use the name, but this
may get deprecated at some point.

```lua
Spring.GetUnitMoveDefID(UnitID) -> (integer|false)?, string?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `moveDefID` `(integer|false)?`
- `moveDefName` `string?`

### Spring.GetUnitTeam {#Spring.GetUnitTeam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4101-L4106" target="_blank">source</a>]

```lua
Spring.GetUnitTeam(UnitID) -> TeamID?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `TeamID?`

### Spring.GetUnitAllyTeam {#Spring.GetUnitAllyTeam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4118-L4123" target="_blank">source</a>]

```lua
Spring.GetUnitAllyTeam(UnitID) -> AllyTeamID?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `AllyTeamID?`

### Spring.GetUnitNeutral {#Spring.GetUnitNeutral}
*function*

Checks if a unit is neutral (NOT Gaia!)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4135-L4144" target="_blank">source</a>]

Note that a "neutral" unit can belong to any ally-team (ally, enemy, Gaia).
To check if a unit is Gaia, check its owner team.

```lua
Spring.GetUnitNeutral(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `boolean?`

### Spring.GetUnitHealth {#Spring.GetUnitHealth}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4156-L4165" target="_blank">source</a>]

```lua
Spring.GetUnitHealth(UnitID) -> number?, number, number, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `health` `number?`
- `maxHealth` `number`
- `paralyzeDamage` `number`
- `captureProgress` `number`
- `buildProgress` `number` — between 0.0-1.0

### Spring.GetUnitIsDead {#Spring.GetUnitIsDead}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4195-L4200" target="_blank">source</a>]

```lua
Spring.GetUnitIsDead(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `boolean?`

### Spring.GetUnitIsStunned {#Spring.GetUnitIsStunned}
*function*

Checks whether a unit is disabled and can't act

The first return value is a simple OR of the following ones,
any of those conditions is sufficient to disable the unit.

Note that EMP and being transported are mechanically the same and thus lumped together.
Use other callouts to differentiate them if you need to.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4212-L4225" target="_blank">source</a>]

```lua
Spring.GetUnitIsStunned(UnitID) -> boolean?, boolean, boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `stunnedOrBuilt` `boolean?` — unit is disabled
- `stunned` `boolean` — unit is either stunned via EMP or being transported by a non-fireplatform
- `beingBuilt` `boolean` — unit is under construction

### Spring.GetUnitIsBeingBuilt {#Spring.GetUnitIsBeingBuilt}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4239-L4245" target="_blank">source</a>]

```lua
Spring.GetUnitIsBeingBuilt(UnitID) -> boolean, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `beingBuilt` `boolean`
- `buildProgress` `number`

### Spring.GetUnitResources {#Spring.GetUnitResources}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4257-L4265" target="_blank">source</a>]

```lua
Spring.GetUnitResources(UnitID) -> number?, number, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `metalMake` `number?`
- `metalUse` `number`
- `energyMake` `number`
- `energyUse` `number`

### Spring.GetUnitStorage {#Spring.GetUnitStorage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4279-L4284" target="_blank">source</a>]

```lua
Spring.GetUnitStorage(UnitID) -> number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `metalStorage` `number` — Unit's metal storage
- `energyStorage` `number` — Unit's energy storage

### Spring.GetUnitCosts {#Spring.GetUnitCosts}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4297-L4303" target="_blank">source</a>]

```lua
Spring.GetUnitCosts(UnitID) -> number?, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `buildTime` `number?`
- `metalCost` `number`
- `energyCost` `number`

### Spring.GetUnitCostTable {#Spring.GetUnitCostTable}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4323-L4328" target="_blank">source</a>]

```lua
Spring.GetUnitCostTable(UnitID) -> ResourceCost?, number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `cost` `ResourceCost?` — The cost of the unit, or `nil` if invalid.
- `buildTime` `number?` — The build time the unit, or `nil` if invalid.

### Spring.GetUnitMetalExtraction {#Spring.GetUnitMetalExtraction}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4346-L4351" target="_blank">source</a>]

```lua
Spring.GetUnitMetalExtraction(UnitID) -> number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `metalExtraction` `number?`

### Spring.GetUnitExperience {#Spring.GetUnitExperience}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4366-L4372" target="_blank">source</a>]

```lua
Spring.GetUnitExperience(UnitID) -> number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `xp` `number` — [0.0; +∞)
- `limXp` `number` — [0.0; 1.0) as experience approaches infinity

### Spring.GetUnitHeight {#Spring.GetUnitHeight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4385-L4390" target="_blank">source</a>]

```lua
Spring.GetUnitHeight(UnitID) -> number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `number?`

### Spring.GetUnitRadius {#Spring.GetUnitRadius}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4402-L4407" target="_blank">source</a>]

```lua
Spring.GetUnitRadius(UnitID) -> number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `number?`

### Spring.GetUnitBuildeeRadius {#Spring.GetUnitBuildeeRadius}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4418-L4424" target="_blank">source</a>]

Gets the unit's radius for when targeted by build, repair, reclaim-type commands.

```lua
Spring.GetUnitBuildeeRadius(UnitID) -> number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `number?`

### Spring.GetUnitMass {#Spring.GetUnitMass}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4435-L4440" target="_blank">source</a>]

```lua
Spring.GetUnitMass(UnitID) -> number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `number?`

### Spring.GetUnitPosition {#Spring.GetUnitPosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4446-L4461" target="_blank">source</a>]

```lua
Spring.GetUnitPosition(UnitID, boolean?, boolean?) -> number?, number, number, number?, number, number, number?, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `midPos` `boolean?` — (Default: `false`) return midpoint as well
- `aimPos` `boolean?` — (Default: `false`) return aimpoint as well

**Returns**

- `basePointX` `number?`
- `basePointY` `number`
- `basePointZ` `number`
- `midPointX` `number?`
- `midPointY` `number`
- `midPointZ` `number`
- `aimPointX` `number?`
- `aimPointY` `number`
- `aimPointZ` `number`

### Spring.GetUnitBasePosition {#Spring.GetUnitBasePosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4467-L4476" target="_blank">source</a>]

The same as [Spring.GetUnitPosition](Spring.md#Spring.GetUnitPosition), but without the optional midpoint calculations.

**See:** [Spring.GetUnitPosition](Spring.md#Spring.GetUnitPosition)

```lua
Spring.GetUnitBasePosition(UnitID) -> number?, number?, number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `posX` `number?`
- `posY` `number?`
- `posZ` `number?`

### Spring.GetUnitVectors {#Spring.GetUnitVectors}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4483-L4490" target="_blank">source</a>]

```lua
Spring.GetUnitVectors(UnitID) -> float3?, float3, float3
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `front` `float3?`
- `up` [`float3`](Aliases.md#float3)
- `right` [`float3`](Aliases.md#float3)

### Spring.GetUnitRotation {#Spring.GetUnitRotation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4511-L4519" target="_blank">source</a>]

Note: PYR order

```lua
Spring.GetUnitRotation(UnitID) -> number, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `pitch` `number` — Rotation in X axis
- `yaw` `number` — Rotation in Y axis
- `roll` `number` — Rotation in Z axis

### Spring.GetUnitDirection {#Spring.GetUnitDirection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4526-L4539" target="_blank">source</a>]

```lua
Spring.GetUnitDirection(UnitID) -> number, number, number, number, number, number, number, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `frontDirX` `number`
- `frontDirY` `number`
- `frontDirZ` `number`
- `rightDirX` `number`
- `rightDirY` `number`
- `rightDirZ` `number`
- `upDirX` `number`
- `upDirY` `number`
- `upDirZ` `number`

### Spring.GetUnitHeading {#Spring.GetUnitHeading}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4563-L4569" target="_blank">source</a>]

```lua
Spring.GetUnitHeading(UnitID, boolean?) -> number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `convertToRadians` `boolean?` — (Default: `false`)

**Returns**

- `heading` `number`

### Spring.GetUnitVelocity {#Spring.GetUnitVelocity}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4586-L4590" target="_blank">source</a>]

```lua
Spring.GetUnitVelocity(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### Spring.GetUnitBuildFacing {#Spring.GetUnitBuildFacing}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4597-L4602" target="_blank">source</a>]

```lua
Spring.GetUnitBuildFacing(UnitID) -> FacingInteger?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `buildFacing` `FacingInteger?` — facing of footprint, `0` - `3`

### Spring.GetUnitIsBuilding {#Spring.GetUnitIsBuilding}
*function*

Checks whether a unit is currently building another (NOT for checking if it's a structure)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4614-L4622" target="_blank">source</a>]

Works for both mobile builders and factories.

```lua
Spring.GetUnitIsBuilding(UnitID) -> UnitID?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `buildeeUnitID` `UnitID?`

### Spring.GetUnitWorkerTask {#Spring.GetUnitWorkerTask}
*function*

Checks a builder's current task

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4702-L4720" target="_blank">source</a>]

Checks what a builder is currently doing. This is not the same as [Spring.GetUnitCurrentCommand](Spring.md#Spring.GetUnitCurrentCommand),
because you can have a command at the front of the queue and not be doing it (for example because
the target is still too far away), and on the other hand you can also be doing a task despite not
having it in front of the queue (for example you're Guarding another builder who does). Also, it
resolves the Repair command into either actual repair, or construction assist (in which case it
returns the appropriate "build" command). Only build-related commands are returned (no Move or any
custom commands).

The possible commands returned are repair, reclaim, resurrect, capture, restore,
and build commands (negative buildee unitDefID).

```lua
Spring.GetUnitWorkerTask(UnitID) -> integer, integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `cmdID` `integer` — of the relevant command
- `targetID` `integer` — if applicable (all except RESTORE)

### Spring.GetUnitEffectiveBuildRange {#Spring.GetUnitEffectiveBuildRange}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4736-L4743" target="_blank">source</a>]

Useful for setting move goals manually.

```lua
Spring.GetUnitEffectiveBuildRange(UnitID, UnitDefID?) -> number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `buildeeDefID` `UnitDefID?`

**Returns**

- `effectiveBuildRange` `number` — counted to the center of prospective buildee; buildRange if buildee nil

### Spring.GetUnitCurrentBuildPower {#Spring.GetUnitCurrentBuildPower}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4792-L4797" target="_blank">source</a>]

```lua
Spring.GetUnitCurrentBuildPower(UnitID) -> number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `buildPower` `number?` — `nil` if the unit is neither a builder nor a factory.

### Spring.GetUnitHarvestStorage {#Spring.GetUnitHarvestStorage}
*function*

Get a unit's carried resources

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4826-L4837" target="_blank">source</a>]

Checks resources being carried internally by the unit.

```lua
Spring.GetUnitHarvestStorage(UnitID) -> number, number, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `storedMetal` `number`
- `maxStoredMetal` `number`
- `storedEnergy` `number`
- `maxStoredEnergy` `number`

### Spring.GetUnitBuildParams {#Spring.GetUnitBuildParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4851-L4859" target="_blank">source</a>]

```lua
Spring.GetUnitBuildParams(UnitID, ("buildRange"|"buildDistance"|"buildRange3D")) -> (number|boolean)?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `paramName` `("buildRange"|"buildDistance"|"buildRange3D")` — The build param to get

**Returns**

- `value` `(number|boolean)?` — number for `"buildRange"` or `"buildDistance"`,
boolean for `"buildRange3D"`, otherwise `nil` for unrecognized paramName or not
allied builder unit.

### Spring.GetUnitInBuildStance {#Spring.GetUnitInBuildStance}
*function*

Is builder in build stance

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4888-L4897" target="_blank">source</a>]

Checks if a builder is in build stance, i.e. can create nanoframes.
Returns nil for non-builders.

```lua
Spring.GetUnitInBuildStance(UnitID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `inBuildStance` `boolean`

### Spring.GetUnitNanoPieces {#Spring.GetUnitNanoPieces}
*function*

Get construction FX attachment points

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4914-L4927" target="_blank">source</a>]

Returns an array of pieces which represent construction
points. Default engine construction FX (nano spray) will
originate there.

Only works on builders and factories, returns nil (NOT empty table)
for other units.

```lua
Spring.GetUnitNanoPieces(UnitID) -> integer[]
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `pieceArray` `integer[]`

### Spring.GetUnitTransporter {#Spring.GetUnitTransporter}
*function*

Get the transport carrying the unit

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4969-L4978" target="_blank">source</a>]

Returns the unit ID of the transport, if any.
Returns nil if the unit is not being transported.

```lua
Spring.GetUnitTransporter(UnitID) -> UnitID?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `transportUnitID` `UnitID?`

### Spring.GetUnitIsTransporting {#Spring.GetUnitIsTransporting}
*function*

Get units being transported

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L4993-L5000" target="_blank">source</a>]

```lua
Spring.GetUnitIsTransporting(UnitID) -> UnitID[]?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `transporteeArray` `UnitID[]?`

### Spring.GetUnitShieldState {#Spring.GetUnitShieldState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5022-L5029" target="_blank">source</a>]

```lua
Spring.GetUnitShieldState(UnitID, integer?) -> integer, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer?` — Optional if the unit has just one shield

**Returns**

- `isEnabled` `integer` — Warning, number not boolean. 0 or 1
- `currentPower` `number`

### Spring.GetUnitFlanking {#Spring.GetUnitFlanking}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5054-L5073" target="_blank">source</a>]

When called without a key, returns every value. When called with one of
`"mode"`, `"moveFactor"`, `"minDamage"` or `"maxDamage"` returns just that
single number, and with `"dir"` returns just `dirX`, `dirY`, `dirZ`.

```lua
Spring.GetUnitFlanking(UnitID) -> number, number, number, number, number, number, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `mode` `number`
- `moveFactor` `number`
- `minDamage` `number`
- `maxDamage` `number`
- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`
- `mobility` `number` — The amount of mobility the unit has collected up to now.

### Spring.GetUnitMaxRange {#Spring.GetUnitMaxRange}
*function*

Get a unit's engagement range

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5128-L5138" target="_blank">source</a>]

Returns the range at which a unit will stop to engage.
By default this is the highest among the unit's weapon ranges (hence name),
but can be changed dynamically. Also note that unarmed units ignore this.

```lua
Spring.GetUnitMaxRange(UnitID) -> number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `maxRange` `number`

### Spring.GetUnitWeaponState {#Spring.GetUnitWeaponState}
*function*

Check the state of a unit's weapon

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5157-L5188" target="_blank">source</a>]

Available states to poll:
"reloadFrame" (frame on which the weapon will be ready to fire),
"reloadSpeed" (reload time in seconds),
"range" (in elmos),
"autoTargetRangeBoost" (predictive aiming range buffer, in elmos),
"projectileSpeed" (in elmos/frame),
"reloadTimeXP" (reload time after XP bonus, in seconds),
"reaimTime" (frames between AimWeapon calls),
"burst" (shots in a burst),
"burstRate" (delay between shots in a burst, in seconds),
"projectiles" (projectiles per shot),
"salvoLeft" (shots remaining in ongoing burst),
"nextSalvo" (simframe of the next shot in an ongoing burst),
"accuracy" (INaccuracy after XP bonus),
"sprayAngle" (spray angle after XP bonus),
"targetMoveError" (extra inaccuracy against moving targets, after XP bonus)
"avoidFlags" (bitmask for targeting avoidance),
"ttl" (number of seconds a projectile should live)
"collisionFlags" (bitmask for collisions).

The state "salvoError" is an exception and returns a table: {x, y, z},
which represents the inaccuracy error of the ongoing burst.

```lua
Spring.GetUnitWeaponState(UnitID, integer, string?) -> number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `stateName` `string?`

**Returns**

- `stateValue` `number`

### Spring.GetUnitWeaponDamages {#Spring.GetUnitWeaponDamages}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5367-L5371" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponDamages(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### Spring.GetUnitWeaponVectors {#Spring.GetUnitWeaponVectors}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5406-L5417" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponVectors(UnitID, integer) -> number?, number, number, number, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer` — 1-indexed weapon number

**Returns**

- `posX` `number?`
- `posY` `number`
- `posZ` `number`
- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`

### Spring.GetUnitWeaponTryTarget {#Spring.GetUnitWeaponTryTarget}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5453-L5460" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponTryTarget(UnitID, integer, UnitID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `targetID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `canTarget` `boolean`

### Spring.GetUnitWeaponTryTarget (overload 1) {#Spring.GetUnitWeaponTryTarget-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5461-L5470" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponTryTarget(UnitID, integer, number, number, number) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `posX` `number`
- `posY` `number`
- `posZ` `number`

**Returns**

- `canTarget` `boolean`

### Spring.GetUnitWeaponTestTarget {#Spring.GetUnitWeaponTestTarget}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5511-L5518" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponTestTarget(UnitID, integer, UnitID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponID` `integer` — weapon number (1-based Lua index)
- `targetUnitID` [`UnitID`](Aliases.md#UnitID) — enemy unit to test (when fewer than five arguments)

**Returns**

- `validTarget` `boolean`

### Spring.GetUnitWeaponTestTarget (overload 1) {#Spring.GetUnitWeaponTestTarget-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5519-L5528" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponTestTarget(UnitID, integer, number, number, number) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponID` `integer` — weapon number (1-based Lua index)
- `targetX` `number` — world X to test (with `targetY`, `targetZ`; used when at least five arguments are passed)
- `targetY` `number`
- `targetZ` `number`

**Returns**

- `validTarget` `boolean`

### Spring.GetUnitWeaponTestRange {#Spring.GetUnitWeaponTestRange}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5562-L5569" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponTestRange(UnitID, integer, UnitID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `targetID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `inRange` `boolean`

### Spring.GetUnitWeaponTestRange (overload 1) {#Spring.GetUnitWeaponTestRange-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5570-L5579" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponTestRange(UnitID, integer, number, number, number) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `posX` `number`
- `posY` `number`
- `posZ` `number`

**Returns**

- `inRange` `boolean`

### Spring.GetUnitWeaponHaveFreeLineOfFire {#Spring.GetUnitWeaponHaveFreeLineOfFire}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5613-L5620" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponHaveFreeLineOfFire(UnitID, integer, UnitID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `targetID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `haveFreeLineOfFire` `boolean`

### Spring.GetUnitWeaponHaveFreeLineOfFire (overload 1) {#Spring.GetUnitWeaponHaveFreeLineOfFire-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5621-L5630" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponHaveFreeLineOfFire(UnitID, integer, number, number, number) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `srcPosX` `number`
- `srcPosY` `number`
- `srcPosZ` `number`

**Returns**

- `haveFreeLineOfFire` `boolean`

### Spring.GetUnitWeaponHaveFreeLineOfFire (overload 2) {#Spring.GetUnitWeaponHaveFreeLineOfFire-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5631-L5641" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponHaveFreeLineOfFire(UnitID, integer, number, number, number, UnitID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `srcPosX` `number`
- `srcPosY` `number`
- `srcPosZ` `number`
- `targetID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `haveFreeLineOfFire` `boolean`

### Spring.GetUnitWeaponHaveFreeLineOfFire (overload 3) {#Spring.GetUnitWeaponHaveFreeLineOfFire-3}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5642-L5654" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponHaveFreeLineOfFire(UnitID, integer, number, number, number, number, number, number) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `srcPosX` `number`
- `srcPosY` `number`
- `srcPosZ` `number`
- `tgtPosX` `number`
- `tgtPosY` `number`
- `tgtPosZ` `number`

**Returns**

- `haveFreeLineOfFire` `boolean`

### Spring.GetUnitWeaponCanFire {#Spring.GetUnitWeaponCanFire}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5716-L5725" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponCanFire(UnitID, integer, boolean?, boolean?, boolean?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`
- `ignoreAngleGood` `boolean?`
- `ignoreTargetType` `boolean?`
- `ignoreRequestedDir` `boolean?`

**Returns**

- `canFire` `boolean`

### Spring.GetUnitWeaponTarget {#Spring.GetUnitWeaponTarget}
*function*

Checks a weapon's target

Note that this doesn't need to reflect the unit's Attack orders or such, and
that weapons can aim individually unless slaved.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5754-L5765" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponTarget(UnitID, integer) -> 0, boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`

**Returns**

- `TargetType` `0` — none
- `isUserTarget` `boolean`

### Spring.GetUnitWeaponTarget (overload 1) {#Spring.GetUnitWeaponTarget-1}
*function*

Checks a weapon's target

Note that this doesn't need to reflect the unit's Attack orders or such, and
that weapons can aim individually unless slaved.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5766-L5778" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponTarget(UnitID, integer) -> 1, boolean, UnitID
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`

**Returns**

- `TargetType` `1` — unit
- `isUserTarget` `boolean`
- `targetUnitID` [`UnitID`](Aliases.md#UnitID)

### Spring.GetUnitWeaponTarget (overload 2) {#Spring.GetUnitWeaponTarget-2}
*function*

Checks a weapon's target

Note that this doesn't need to reflect the unit's Attack orders or such, and
that weapons can aim individually unless slaved.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5779-L5791" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponTarget(UnitID, integer) -> 2, boolean, float3
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`

**Returns**

- `TargetType` `2` — position
- `isUserTarget` `boolean`
- `targetPosition` [`float3`](Aliases.md#float3)

### Spring.GetUnitWeaponTarget (overload 3) {#Spring.GetUnitWeaponTarget-3}
*function*

Checks a weapon's target

Note that this doesn't need to reflect the unit's Attack orders or such, and
that weapons can aim individually unless slaved.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5792-L5804" target="_blank">source</a>]

```lua
Spring.GetUnitWeaponTarget(UnitID, integer) -> 3, boolean, ProjectileID
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponNum` `integer`

**Returns**

- `TargetType` `3` — projectileID
- `isUserTarget` `boolean`
- `targetProjectileId` [`ProjectileID`](Aliases.md#ProjectileID)

### Spring.GetUnitEstimatedPath {#Spring.GetUnitEstimatedPath}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5861-L5865" target="_blank">source</a>]

```lua
Spring.GetUnitEstimatedPath(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### Spring.GetUnitLastAttacker {#Spring.GetUnitLastAttacker}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5881-L5886" target="_blank">source</a>]

```lua
Spring.GetUnitLastAttacker(UnitID) -> UnitID?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `attackerUnitID` `UnitID?` — `nil` if the unit has no last attacker or the attacker is not visible.

### Spring.GetUnitLastAttackedPiece {#Spring.GetUnitLastAttackedPiece}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5902-L5906" target="_blank">source</a>]

```lua
Spring.GetUnitLastAttackedPiece(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### Spring.GetUnitCollisionVolumeData {#Spring.GetUnitCollisionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5912-L5916" target="_blank">source</a>]

```lua
Spring.GetUnitCollisionVolumeData(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### Spring.GetUnitPieceCollisionVolumeData {#Spring.GetUnitPieceCollisionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5927-L5945" target="_blank">source</a>]

```lua
Spring.GetUnitPieceCollisionVolumeData(UnitID, integer) -> number?, number?, number?, number?, number?, number?, integer?, integer?, integer?, boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceIndex` `integer` — 1-based local-model piece index

**Returns**

- `scaleX` `number?`
- `scaleY` `number?`
- `scaleZ` `number?`
- `offsetX` `number?`
- `offsetY` `number?`
- `offsetZ` `number?`
- `volumeType` `integer?`
- `testType` `integer?`
- `primaryAxis` `integer?`
- `disabled` `boolean?`

### Spring.GetUnitSeparation {#Spring.GetUnitSeparation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5952-L5960" target="_blank">source</a>]

```lua
Spring.GetUnitSeparation(UnitID, UnitID, boolean?, boolean?) -> number?
```

**Parameters**

- `unitID1` [`UnitID`](Aliases.md#UnitID)
- `unitID2` [`UnitID`](Aliases.md#UnitID)
- `direction` `boolean?` — (Default: `false`) to subtract from, default unitID1 - unitID2
- `subtractRadii` `boolean?` — (Default: `false`) whether units radii should be subtracted from the total

**Returns**

- `number?`

### Spring.GetUnitFeatureSeparation {#Spring.GetUnitFeatureSeparation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5994-L6001" target="_blank">source</a>]

```lua
Spring.GetUnitFeatureSeparation(UnitID, FeatureID, boolean?) -> number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `flat` `boolean?` — (Default: `false`) if true, XZ (2D) distance; otherwise 3D distance

**Returns**

- `distance` `number`

### Spring.GetUnitDefDimensions {#Spring.GetUnitDefDimensions}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6047-L6052" target="_blank">source</a>]

```lua
Spring.GetUnitDefDimensions(UnitDefID) -> UnitDefDimensions?
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)

**Returns**

- `dimensions` `UnitDefDimensions?`

### Spring.GetCEGID {#Spring.GetCEGID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6082-L6086" target="_blank">source</a>]

```lua
Spring.GetCEGID() -> integer
```

**Returns**

- `cegID` `integer`

### Spring.GetUnitBlocking {#Spring.GetUnitBlocking}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6094-L6105" target="_blank">source</a>]

```lua
Spring.GetUnitBlocking(UnitID) -> boolean?, boolean, boolean, boolean, boolean, boolean, boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `isBlocking` `boolean?`
- `isSolidObjectCollidable` `boolean`
- `isProjectileCollidable` `boolean`
- `isRaySegmentCollidable` `boolean`
- `crushable` `boolean`
- `blockEnemyPushing` `boolean`
- `blockHeightChanges` `boolean`

### Spring.GetUnitMoveTypeData {#Spring.GetUnitMoveTypeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6112-L6116" target="_blank">source</a>]

```lua
Spring.GetUnitMoveTypeData(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### Spring.GetUnitCurrentCommand {#Spring.GetUnitCurrentCommand}
*function*

Get a command from a units command queue.

For factories, this function uses the command queue automatically assigned to new units.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6345-L6360" target="_blank">source</a>]

**See:** Spring.GetFactoryCommands for getting factory build queue commands

```lua
Spring.GetUnitCurrentCommand(UnitID, integer?) -> CMD?, (integer|CommandOptionBit)?, integer?, number? ...
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID) — unitID when invalid this function returns nil.
- `cmdIndex` `integer?` — (Default: `0`) Command index to get. If negative will count from the end of the queue, e.g. -1 will be the last command.

**Returns**

- `cmdID` `CMD?`
- `options` `(integer|CommandOptionBit)?`
- `tag` `integer?`
- `Command` `number? ...` — parameters.

### Spring.GetUnitCommands {#Spring.GetUnitCommands}
*function*

Get the commands for a unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6397-L6407" target="_blank">source</a>]

Same as [Spring.GetCommandQueue](Spring.md#Spring.GetCommandQueue)

```lua
Spring.GetUnitCommands(UnitID, integer) -> Command[]
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `count` `integer` — Maximum amount of commands to return, `-1` returns all commands.

**Returns**

- `commands` `Command[]`

### Spring.GetUnitCommands (overload 1) {#Spring.GetUnitCommands-1}
*function*

Get the count of commands for a unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6408-L6417" target="_blank">source</a>]

**Deprecated:** This overload is deprecated, use `Spring.GetUnitCommandCount(unitId)` instead.

```lua
Spring.GetUnitCommands(UnitID, 0) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `count` `0` — Returns the number of commands in the units queue.

**Returns**

- `cmdCount` `integer` — The number of commands in the unit queue.

### Spring.GetFactoryCommands {#Spring.GetFactoryCommands}
*function*

Get the number or list of commands for a factory

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6445-L6455" target="_blank">source</a>]

**See:** Spring.GetFactoryCounts to get command counts grouped by cmdID.

```lua
Spring.GetFactoryCommands(UnitID, integer) -> Command[]
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `count` `integer` — Maximum amount of commands to return, `-1` returns all commands.

**Returns**

- `commands` `Command[]`

### Spring.GetFactoryCommands (overload 1) {#Spring.GetFactoryCommands-1}
*function*

Get the count of commands for a factory.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6456-L6467" target="_blank">source</a>]

**Deprecated:** This overload is deprecated, use `Spring.GetFactoryCommandCount(unitId)` instead.
**See:** Spring.GetFactoryCommandCount for replacement function.

```lua
Spring.GetFactoryCommands(UnitID, 0) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `count` `0` — Returns the number of commands in the factory queue.

**Returns**

- `cmdCount` `integer` — The number of commands in the factory queue.

### Spring.GetUnitCommandCount {#Spring.GetUnitCommandCount}
*function*

Get the number of commands in a unit's queue.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6497-L6502" target="_blank">source</a>]

```lua
Spring.GetUnitCommandCount(UnitID) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `cmdCount` `integer` — The number of commands in the unit's queue.

### Spring.GetFactoryCommandCount {#Spring.GetFactoryCommandCount}
*function*

Get the number of commands in a factory queue.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6520-L6528" target="_blank">source</a>]

**See:** Spring.GetFactoryCounts to get command counts grouped by cmdID.

```lua
Spring.GetFactoryCommandCount(UnitID) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `cmdCount` `integer` — The number of commands in the factory queue.

### Spring.GetFactoryBuggerOff {#Spring.GetFactoryBuggerOff}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6550-L6560" target="_blank">source</a>]

```lua
Spring.GetFactoryBuggerOff(UnitID) -> boolean?, number, number, number, boolean, boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `boPerform` `boolean?` — `nil` if the unit does not exist or is not a factory.
- `boOffset` `number`
- `boRadius` `number`
- `boRelHeading` `number`
- `boSherical` `boolean`
- `boForced` `boolean`

### Spring.GetFactoryCounts {#Spring.GetFactoryCounts}
*function*

Gets the build queue of a factory

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6636-L6644" target="_blank">source</a>]

```lua
Spring.GetFactoryCounts(UnitID, integer?, boolean?) -> table<number,number>?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `count` `integer?` — (Default: `-1`) Number of commands to retrieve, `-1` for all.
- `addCmds` `boolean?` — (Default: `false`) Retrieve commands other than buildunit

**Returns**

- `counts` `table<number,number>?` — Build queue count by `unitDefID` or `-cmdID`, or `nil` if unit is not found.

### Spring.GetCommandQueue {#Spring.GetCommandQueue}
*function*

Get the commands for a unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6672-L6683" target="_blank">source</a>]

Same as [Spring.GetUnitCommands](Spring.md#Spring.GetUnitCommands)

**Deprecated:** Use Spring.GetUnitCommands instead.

```lua
Spring.GetCommandQueue(UnitID, integer) -> Command[]
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `count` `integer` — Number of commands to return, `-1` returns all commands, `0` returns command count.

**Returns**

- `commands` `Command[]`

### Spring.GetCommandQueue (overload 1) {#Spring.GetCommandQueue-1}
*function*

Get the count of commands for a unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6684-L6696" target="_blank">source</a>]

Same as [Spring.GetUnitCommands](Spring.md#Spring.GetUnitCommands)

**Deprecated:** Use Spring.GetUnitCommandCount instead.

```lua
Spring.GetCommandQueue(UnitID, 0) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `count` `0` — Returns the number of commands in the units queue.

**Returns**

- `cmdCount` `integer` — The number of commands in the unit queue.

### Spring.GetFullBuildQueue {#Spring.GetFullBuildQueue}
*function*

Returns the build queue

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6777-L6782" target="_blank">source</a>]

```lua
Spring.GetFullBuildQueue(UnitID) -> table<UnitDefID,integer>?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `buildqueue` `table<UnitDefID,integer>?` — indexed by unitDefID with count values

### Spring.GetRealBuildQueue {#Spring.GetRealBuildQueue}
*function*

Returns the build queue cleaned of things the unit can't build itself

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6789-L6794" target="_blank">source</a>]

```lua
Spring.GetRealBuildQueue(UnitID) -> table<UnitDefID,integer>?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `buildqueue` `table<UnitDefID,integer>?` — indexed by unitDefID with count values

### Spring.GetUnitCmdDescs {#Spring.GetUnitCmdDescs}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6804-L6808" target="_blank">source</a>]

```lua
Spring.GetUnitCmdDescs(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### Spring.FindUnitCmdDesc {#Spring.FindUnitCmdDesc}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6843-L6849" target="_blank">source</a>]

```lua
Spring.FindUnitCmdDesc(UnitID, integer) -> integer?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `cmdID` `integer`

**Returns**

- `integer?`

### Spring.ValidFeatureID {#Spring.ValidFeatureID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6872-L6877" target="_blank">source</a>]

```lua
Spring.ValidFeatureID(FeatureID) -> boolean
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `boolean`

### Spring.GetAllFeatures {#Spring.GetAllFeatures}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6885-L6888" target="_blank">source</a>]

```lua
Spring.GetAllFeatures() -> FeatureID[]
```

**Returns**

- `featureIDs` `FeatureID[]`

### Spring.GetFeatureDefID {#Spring.GetFeatureDefID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6913-L6918" target="_blank">source</a>]

```lua
Spring.GetFeatureDefID(FeatureID) -> FeatureDefID?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `FeatureDefID?`

### Spring.GetFeatureTeam {#Spring.GetFeatureTeam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6930-L6935" target="_blank">source</a>]

```lua
Spring.GetFeatureTeam(FeatureID) -> TeamID?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `TeamID?`

### Spring.GetFeatureAllyTeam {#Spring.GetFeatureAllyTeam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6951-L6956" target="_blank">source</a>]

```lua
Spring.GetFeatureAllyTeam(FeatureID) -> AllyTeamID?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `AllyTeamID?`

### Spring.GetFeatureHealth {#Spring.GetFeatureHealth}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6968-L6975" target="_blank">source</a>]

```lua
Spring.GetFeatureHealth(FeatureID) -> number?, number, number
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `health` `number?`
- `defHealth` `number`
- `resurrectProgress` `number`

### Spring.GetFeatureHeight {#Spring.GetFeatureHeight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L6989-L6994" target="_blank">source</a>]

```lua
Spring.GetFeatureHeight(FeatureID) -> number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `number?`

### Spring.GetFeatureRadius {#Spring.GetFeatureRadius}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7006-L7011" target="_blank">source</a>]

```lua
Spring.GetFeatureRadius(FeatureID) -> number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `number?`

### Spring.GetFeatureMass {#Spring.GetFeatureMass}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7022-L7027" target="_blank">source</a>]

```lua
Spring.GetFeatureMass(FeatureID) -> number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `number?`

### Spring.GetFeaturePosition {#Spring.GetFeaturePosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7033-L7040" target="_blank">source</a>]

```lua
Spring.GetFeaturePosition(FeatureID) -> number?, number?, number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `x` `number?`
- `y` `number?`
- `z` `number?`

### Spring.GetFeatureSeparation {#Spring.GetFeatureSeparation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7047-L7054" target="_blank">source</a>]

```lua
Spring.GetFeatureSeparation(FeatureID, FeatureID, boolean?) -> number?
```

**Parameters**

- `featureID1` [`FeatureID`](Aliases.md#FeatureID)
- `featureID2` [`FeatureID`](Aliases.md#FeatureID)
- `direction` `boolean?` — (Default: `false`) to subtract from, default featureID1 - featureID2

**Returns**

- `number?`

### Spring.GetFeatureRotation {#Spring.GetFeatureRotation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7079-L7087" target="_blank">source</a>]

Note: PYR order

```lua
Spring.GetFeatureRotation(FeatureID) -> number?, number?, number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `pitch` `number?` — Rotation in X axis
- `yaw` `number?` — Rotation in Y axis
- `roll` `number?` — Rotation in Z axis

### Spring.GetFeatureDirection {#Spring.GetFeatureDirection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7097-L7110" target="_blank">source</a>]

```lua
Spring.GetFeatureDirection(FeatureID) -> number?, number?, number?, number?, number?, number?, number?, number?, number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `frontDirX` `number?`
- `frontDirY` `number?`
- `frontDirZ` `number?`
- `rightDirX` `number?`
- `rightDirY` `number?`
- `rightDirZ` `number?`
- `upDirX` `number?`
- `upDirY` `number?`
- `upDirZ` `number?`

### Spring.GetFeatureVelocity {#Spring.GetFeatureVelocity}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7138-L7147" target="_blank">source</a>]

Returns nil if no feature found with ID.

```lua
Spring.GetFeatureVelocity(FeatureID) -> number?, number?, number?, number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `x` `number?`
- `y` `number?`
- `z` `number?`
- `w` `number?`

### Spring.GetFeatureHeading {#Spring.GetFeatureHeading}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7154-L7159" target="_blank">source</a>]

```lua
Spring.GetFeatureHeading(FeatureID) -> number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `heading` `number?`

### Spring.GetFeatureResources {#Spring.GetFeatureResources}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7171-L7181" target="_blank">source</a>]

```lua
Spring.GetFeatureResources(FeatureID) -> number?, number, number, number, number, number
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `metal` `number?`
- `defMetal` `number`
- `energy` `number`
- `defEnergy` `number`
- `reclaimLeft` `number`
- `reclaimTime` `number`

### Spring.GetFeatureBlocking {#Spring.GetFeatureBlocking}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7198-L7209" target="_blank">source</a>]

```lua
Spring.GetFeatureBlocking(FeatureID) -> boolean?, boolean?, boolean?, boolean?, boolean?, boolean?, boolean?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `isBlocking` `boolean?`
- `isSolidObjectCollidable` `boolean?`
- `isProjectileCollidable` `boolean?`
- `isRaySegmentCollidable` `boolean?`
- `crushable` `boolean?`
- `blockEnemyPushing` `boolean?`
- `blockHeightChanges` `boolean?`

### Spring.GetFeatureNoSelect {#Spring.GetFeatureNoSelect}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7216-L7221" target="_blank">source</a>]

```lua
Spring.GetFeatureNoSelect(FeatureID) -> boolean?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `boolean?`

### Spring.GetFeatureResurrect {#Spring.GetFeatureResurrect}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7234-L7241" target="_blank">source</a>]

Returns nil if no feature found with ID.

```lua
Spring.GetFeatureResurrect(FeatureID) -> (string|"")?, FacingInteger
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `featureDefName` `(string|"")?`
- `buildFacing` [`FacingInteger`](Aliases.md#FacingInteger) — facing of footprint, 0 - 3

### Spring.GetFeatureLastAttackedPiece {#Spring.GetFeatureLastAttackedPiece}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7260-L7266" target="_blank">source</a>]

```lua
Spring.GetFeatureLastAttackedPiece(FeatureID) -> (string|"")?, integer?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `pieceName` `(string|"")?` — Last hit piece name
- `frame` `integer?` — frame it was last hit on, `nil` when featureID is not valid

### Spring.GetFeatureCollisionVolumeData {#Spring.GetFeatureCollisionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7290-L7295" target="_blank">source</a>]

```lua
Spring.GetFeatureCollisionVolumeData(FeatureID) -> CollisionVolumeData?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `CollisionVolumeData?`

### Spring.GetFeaturePieceCollisionVolumeData {#Spring.GetFeaturePieceCollisionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7306-L7311" target="_blank">source</a>]

```lua
Spring.GetFeaturePieceCollisionVolumeData(FeatureID) -> CollisionVolumeData?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `CollisionVolumeData?`

### Spring.GetFeatureFireTime {#Spring.GetFeatureFireTime}
*function*

Get the feature current fire timer.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7318-L7324" target="_blank">source</a>]

```lua
Spring.GetFeatureFireTime(FeatureID) -> number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `fireTime` `number?` — in seconds, nil when featureID is invalid.

### Spring.GetFeatureSmokeTime {#Spring.GetFeatureSmokeTime}
*function*

Get the feature current smoke timer.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7337-L7343" target="_blank">source</a>]

```lua
Spring.GetFeatureSmokeTime(FeatureID) -> number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `smokeTime` `number?` — in seconds, nil when featureID is invalid.

### Spring.GetProjectilePosition {#Spring.GetProjectilePosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7363-L7370" target="_blank">source</a>]

```lua
Spring.GetProjectilePosition(ProjectileID) -> number?, number?, number?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `posX` `number?`
- `posY` `number?`
- `posZ` `number?`

### Spring.GetProjectileDirection {#Spring.GetProjectileDirection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7384-L7391" target="_blank">source</a>]

```lua
Spring.GetProjectileDirection(ProjectileID) -> number?, number?, number?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `dirX` `number?`
- `dirY` `number?`
- `dirZ` `number?`

### Spring.GetProjectileVelocity {#Spring.GetProjectileVelocity}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7405-L7413" target="_blank">source</a>]

```lua
Spring.GetProjectileVelocity(ProjectileID) -> number?, number?, number?, number?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `velX` `number?`
- `velY` `number?`
- `velZ` `number?`
- `velW` `number?`

### Spring.GetProjectileGravity {#Spring.GetProjectileGravity}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7420-L7425" target="_blank">source</a>]

```lua
Spring.GetProjectileGravity(ProjectileID) -> number?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `number?`

### Spring.GetPieceProjectileParams {#Spring.GetPieceProjectileParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7439-L7449" target="_blank">source</a>]

```lua
Spring.GetPieceProjectileParams(ProjectileID) -> integer?, number, number, number, number, number
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `explosionFlags` `integer?` — encoded bitwise with SHATTER = 1, EXPLODE = 2, EXPLODE_ON_HIT = 2, FALL = 4, SMOKE = 8, FIRE = 16, NONE = 32, NO_CEG_TRAIL = 64, NO_HEATCLOUD = 128
- `spinAngle` `number`
- `spinSpeed` `number`
- `spinVectorX` `number`
- `spinVectorY` `number`
- `spinVectorZ` `number`

### Spring.GetProjectileTarget {#Spring.GetProjectileTarget}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7469-L7479" target="_blank">source</a>]

```lua
Spring.GetProjectileTarget(ProjectileID) -> integer?, (UnitID|FeatureID|ProjectileID|float3)
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `targetTypeInt` `integer?` — where
string.byte('g') := GROUND
string.byte('u') := UNIT
string.byte('f') := FEATURE
string.byte('p') := PROJECTILE
- `target` `(UnitID|FeatureID|ProjectileID|float3)` — targetID or targetPos when targetTypeInt == string.byte('g')

### Spring.GetProjectileIsIntercepted {#Spring.GetProjectileIsIntercepted}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7521-L7526" target="_blank">source</a>]

```lua
Spring.GetProjectileIsIntercepted(ProjectileID) -> boolean?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `boolean?`

### Spring.GetProjectileTimeToLive {#Spring.GetProjectileTimeToLive}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7541-L7546" target="_blank">source</a>]

```lua
Spring.GetProjectileTimeToLive(ProjectileID) -> integer?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `integer?`

### Spring.GetProjectileOwnerID {#Spring.GetProjectileOwnerID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7561-L7566" target="_blank">source</a>]

```lua
Spring.GetProjectileOwnerID(ProjectileID) -> UnitID?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `UnitID?`

### Spring.GetProjectileTeamID {#Spring.GetProjectileTeamID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7583-L7588" target="_blank">source</a>]

```lua
Spring.GetProjectileTeamID(ProjectileID) -> TeamID?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `TeamID?`

### Spring.GetProjectileAllyTeamID {#Spring.GetProjectileAllyTeamID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7604-L7609" target="_blank">source</a>]

```lua
Spring.GetProjectileAllyTeamID(ProjectileID) -> AllyTeamID?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `AllyTeamID?`

### Spring.GetProjectileType {#Spring.GetProjectileType}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7625-L7631" target="_blank">source</a>]

```lua
Spring.GetProjectileType(ProjectileID) -> boolean?, boolean
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `weapon` `boolean?`
- `piece` `boolean`

### Spring.GetProjectileDefID {#Spring.GetProjectileDefID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7645-L7651" target="_blank">source</a>]

```lua
Spring.GetProjectileDefID(ProjectileID) -> WeaponDefID?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `WeaponDefID?`

### Spring.GetPieceProjectileName {#Spring.GetPieceProjectileName}
*function*

Returns the name of the model piece from which a piece projectile was spawned. Returns nil for other projectiles including weapons

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7671-L7676" target="_blank">source</a>]

```lua
Spring.GetPieceProjectileName(ProjectileID) -> string?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `pieceName` `string?`

### Spring.GetProjectileDamages {#Spring.GetProjectileDamages}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7696-L7717" target="_blank">source</a>]

```lua
Spring.GetProjectileDamages(ProjectileID, string) -> number?
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `tag` `string` — one of:
"paralyzeDamageTime"
"impulseFactor"
"impulseBoost"
"craterMult"
"craterBoost"
"dynDamageExp"
"dynDamageMin"
"dynDamageRange"
"dynDamageInverted"
"craterAreaOfEffect"
"damageAreaOfEffect"
"edgeEffectiveness"
"explosionSpeed"
- or -
an armor type index to get the damage against it.

**Returns**

- `number?`

### Spring.IsPosInMap {#Spring.IsPosInMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7744-L7751" target="_blank">source</a>]

```lua
Spring.IsPosInMap(number, number) -> boolean, boolean
```

**Parameters**

- `x` `number`
- `z` `number`

**Returns**

- `inPlayArea` `boolean` — whether the position is in the active play area
- `inMap` `boolean` — whether the position is in the full map area (currently this is the same as above)

### Spring.GetGroundHeight {#Spring.GetGroundHeight}
*function*

Get ground height

On sea, this returns the negative depth of the seafloor

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7785-L7793" target="_blank">source</a>]

```lua
Spring.GetGroundHeight(number, number) -> number
```

**Parameters**

- `x` `number`
- `z` `number`

**Returns**

- `number`

### Spring.GetWaterPlaneLevel {#Spring.GetWaterPlaneLevel}
*function*

Get water plane height

Water may at some point become shaped (rivers etc) but for now it is always a flat plane.
Use this function instead of GetWaterLevel to denote you are relying on that assumption.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7802-L7810" target="_blank">source</a>]

**See:** [Spring.GetWaterLevel](Spring.md#Spring.GetWaterLevel)

```lua
Spring.GetWaterPlaneLevel() -> number
```

**Returns**

- `waterPlaneLevel` `number`

### Spring.GetWaterLevel {#Spring.GetWaterLevel}
*function*

Get water level in a specific position

Water is currently a flat plane, so this returns the same value regardless of XZ.
However water may become more dynamic at some point so by using this you are future-proof.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7817-L7826" target="_blank">source</a>]

```lua
Spring.GetWaterLevel(number, number) -> number
```

**Parameters**

- `x` `number`
- `z` `number`

**Returns**

- `waterLevel` `number`

### Spring.GetGroundOrigHeight {#Spring.GetGroundOrigHeight}
*function*

Get ground height as it was at game start

Returns the original height before the ground got deformed

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7836-L7844" target="_blank">source</a>]

```lua
Spring.GetGroundOrigHeight(number, number) -> number
```

**Parameters**

- `x` `number`
- `z` `number`

**Returns**

- `number`

### Spring.GetGroundNormal {#Spring.GetGroundNormal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7854-L7864" target="_blank">source</a>]

```lua
Spring.GetGroundNormal(number, number, boolean?) -> number, number, number, number
```

**Parameters**

- `x` `number`
- `z` `number`
- `smoothed` `boolean?` — (Default: `false`) raw or smoothed center normal

**Returns**

- `normalX` `number`
- `normalY` `number`
- `normalZ` `number`
- `slope` `number`

### Spring.GetGroundInfo {#Spring.GetGroundInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7884-L7900" target="_blank">source</a>]

```lua
Spring.GetGroundInfo(number, number) -> integer, integer, integer, string, number, number, number, number, number, number, boolean
```

**Parameters**

- `x` `number`
- `z` `number`

**Returns**

- `ix` `integer`
- `iz` `integer`
- `terrainTypeIndex` `integer`
- `name` `string`
- `metalExtraction` `number`
- `hardness` `number`
- `tankSpeed` `number`
- `kbotSpeed` `number`
- `hoverSpeed` `number`
- `shipSpeed` `number`
- `receiveTracks` `boolean`

### Spring.GetGroundBlocked {#Spring.GetGroundBlocked}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L7955-L7964" target="_blank">source</a>]

```lua
Spring.GetGroundBlocked(number, number, number?, number?) -> string?, ObjectID?
```

**Parameters**

- `x` `number` — world x coordinate (or xMin when using 4-arg form)
- `z` `number` — world z coordinate (or zMin when using 4-arg form)
- `x2` `number?` — world xMax (4-arg rectangle form)
- `z2` `number?` — world zMax (4-arg rectangle form)

**Returns**

- `objectType` `string?` — `"feature"` or `"unit"`
- `objectID` `ObjectID?` — the feature or unit ID

### Spring.GetGroundExtremes {#Spring.GetGroundExtremes}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8006-L8013" target="_blank">source</a>]

```lua
Spring.GetGroundExtremes() -> number, number, number, number
```

**Returns**

- `initMinHeight` `number`
- `initMaxHeight` `number`
- `currMinHeight` `number`
- `currMaxHeight` `number`

### Spring.GetTerrainTypeData {#Spring.GetTerrainTypeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8024-L8036" target="_blank">source</a>]

```lua
Spring.GetTerrainTypeData(integer) -> integer, string, number, number, number, number, number, boolean
```

**Parameters**

- `terrainTypeInfo` `integer`

**Returns**

- `index` `integer`
- `name` `string`
- `hardness` `number`
- `tankSpeed` `number`
- `kbotSpeed` `number`
- `hoverSpeed` `number`
- `shipSpeed` `number`
- `receiveTracks` `boolean`

### Spring.GetGrass {#Spring.GetGrass}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8048-L8054" target="_blank">source</a>]

```lua
Spring.GetGrass(number, number) -> number
```

**Parameters**

- `x` `number`
- `z` `number`

**Returns**

- `number`

### Spring.GetSmoothMeshHeight {#Spring.GetSmoothMeshHeight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8064-L8070" target="_blank">source</a>]

```lua
Spring.GetSmoothMeshHeight(number, number) -> number
```

**Parameters**

- `x` `number`
- `z` `number`

**Returns**

- `height` `number`

### Spring.TestMoveOrder {#Spring.TestMoveOrder}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8088-L8102" target="_blank">source</a>]

```lua
Spring.TestMoveOrder(UnitDefID, number, number, number, number?, number?, number?, boolean?, boolean?, boolean?) -> boolean
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `dirX` `number?` — (Default: `0.0`)
- `dirY` `number?` — (Default: `0.0`)
- `dirZ` `number?` — (Default: `0.0`)
- `testTerrain` `boolean?` — (Default: `true`)
- `testObjects` `boolean?` — (Default: `true`)
- `centerOnly` `boolean?` — (Default: `false`)

**Returns**

- `boolean`

### Spring.TestBuildOrder {#Spring.TestBuildOrder}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8153-L8162" target="_blank">source</a>]

```lua
Spring.TestBuildOrder(UnitDefID, number, number, number, Facing) -> BuildOrderBlockedStatus, FeatureID?
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `x` `number`
- `y` `number`
- `z` `number`
- `facing` [`Facing`](Aliases.md#Facing)

**Returns**

- `blocking` [`BuildOrderBlockedStatus`](Aliases.md#BuildOrderBlockedStatus)
- `featureID` `FeatureID?` — A reclaimable feature in the way.

### Spring.Pos2BuildPos {#Spring.Pos2BuildPos}
*function*

Snaps a position to the building grid

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8203-L8214" target="_blank">source</a>]

```lua
Spring.Pos2BuildPos(UnitDefID, number, number, number, number?) -> number, number, number
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `buildFacing` `number?` — (Default: `0`) one of SOUTH = 0, EAST = 1, NORTH = 2, WEST  = 3

**Returns**

- `buildPosX` `number`
- `buildPosY` `number`
- `buildPosZ` `number`

### Spring.ClosestBuildPos {#Spring.ClosestBuildPos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8232-L8246" target="_blank">source</a>]

```lua
Spring.ClosestBuildPos(TeamID, UnitDefID, number, number, number, number, number, number) -> number, number, number
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `searchRadius` `number`
- `minDistance` `number`
- `buildFacing` `number` — one of SOUTH = 0, EAST = 1, NORTH = 2, WEST  = 3

**Returns**

- `buildPosX` `number`
- `buildPosY` `number`
- `buildPosZ` `number`

### Spring.GetPositionLosState {#Spring.GetPositionLosState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8300-L8311" target="_blank">source</a>]

```lua
Spring.GetPositionLosState(number, number, number, AllyTeamID?) -> boolean, boolean, boolean, boolean
```

**Parameters**

- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `allyTeamID` `AllyTeamID?`

**Returns**

- `inLosOrRadar` `boolean`
- `inLos` `boolean`
- `inRadar` `boolean`
- `inJammer` `boolean`

### Spring.IsPosInLos {#Spring.IsPosInLos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8340-L8348" target="_blank">source</a>]

```lua
Spring.IsPosInLos(number, number, number, AllyTeamID?) -> boolean
```

**Parameters**

- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `allyTeamID` `AllyTeamID?`

**Returns**

- `boolean`

### Spring.IsPosInRadar {#Spring.IsPosInRadar}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8366-L8374" target="_blank">source</a>]

```lua
Spring.IsPosInRadar(number, number, number, AllyTeamID?) -> boolean
```

**Parameters**

- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `allyTeamID` `AllyTeamID?`

**Returns**

- `boolean`

### Spring.IsPosInAirLos {#Spring.IsPosInAirLos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8392-L8400" target="_blank">source</a>]

```lua
Spring.IsPosInAirLos(number, number, number, AllyTeamID?) -> boolean
```

**Parameters**

- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `allyTeamID` `AllyTeamID?`

**Returns**

- `boolean`

### Spring.GetUnitLosState {#Spring.GetUnitLosState}
*function*

Get unit los state (bitmask)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8417-L8424" target="_blank">source</a>]

```lua
Spring.GetUnitLosState(UnitID, AllyTeamID?, true) -> (LosMask|integer)?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `allyTeamID` `AllyTeamID?`
- `raw` `true` — Return a bitmask.

**Returns**

- `bitmask` `(LosMask|integer)?` — A bitmask of [LosMask](LosMask.md#LosMask) bits

### Spring.GetUnitLosState (overload 1) {#Spring.GetUnitLosState-1}
*function*

Get unit los state (table)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8426-L8433" target="_blank">source</a>]

```lua
Spring.GetUnitLosState(UnitID, AllyTeamID?, false?) -> table<("los"|"radar"...),boolean>?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `allyTeamID` `AllyTeamID?`
- `raw` `false?` — (Default: `false`) Return a table.

**Returns**

- `los` `table<("los"|"radar"...),boolean>?` — A table of LOS state names as keys and booleans as values, or `nil` if `unitID` is invalid.

### Spring.IsUnitInLos {#Spring.IsUnitInLos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8476-L8482" target="_blank">source</a>]

```lua
Spring.IsUnitInLos(UnitID, AllyTeamID?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `allyTeamID` `AllyTeamID?` — defaults to the calling widget/gadget's ally team

**Returns**

- `inLos` `boolean`

### Spring.IsUnitInAirLos {#Spring.IsUnitInAirLos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8500-L8506" target="_blank">source</a>]

```lua
Spring.IsUnitInAirLos(UnitID, AllyTeamID?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `allyTeamID` `AllyTeamID?` — defaults to the calling widget/gadget's ally team

**Returns**

- `inAirLos` `boolean`

### Spring.IsUnitInRadar {#Spring.IsUnitInRadar}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8524-L8530" target="_blank">source</a>]

```lua
Spring.IsUnitInRadar(UnitID, AllyTeamID?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `allyTeamID` `AllyTeamID?` — defaults to the calling widget/gadget's ally team

**Returns**

- `inRadar` `boolean`

### Spring.IsUnitInJammer {#Spring.IsUnitInJammer}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8548-L8554" target="_blank">source</a>]

```lua
Spring.IsUnitInJammer(UnitID, AllyTeamID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)

**Returns**

- `inJammer` `boolean`

### Spring.GetModelRootPiece {#Spring.GetModelRootPiece}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8846-L8851" target="_blank">source</a>]

```lua
Spring.GetModelRootPiece(string) -> integer
```

**Parameters**

- `modelName` `string`

**Returns**

- `index` `integer` — of the root piece

### Spring.GetModelPieceMap {#Spring.GetModelPieceMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8856-L8861" target="_blank">source</a>]

```lua
Spring.GetModelPieceMap(string) -> table<string,integer>?
```

**Parameters**

- `modelName` `string`

**Returns**

- `pieceInfos` `table<string,integer>?` — where keys are piece names and values are indices

### Spring.GetModelPieceList {#Spring.GetModelPieceList}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8867-L8872" target="_blank">source</a>]

```lua
Spring.GetModelPieceList(string) -> string[]?
```

**Parameters**

- `modelName` `string`

**Returns**

- `pieceNames` `string[]?`

### Spring.GetUnitRootPiece {#Spring.GetUnitRootPiece}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8878-L8883" target="_blank">source</a>]

```lua
Spring.GetUnitRootPiece(UnitID) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `index` `integer` — of the root piece

### Spring.GetUnitPieceMap {#Spring.GetUnitPieceMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8888-L8893" target="_blank">source</a>]

```lua
Spring.GetUnitPieceMap(UnitID) -> table<string,integer>?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `pieceInfos` `table<string,integer>?` — where keys are piece names and values are indices

### Spring.GetUnitPieceList {#Spring.GetUnitPieceList}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8899-L8904" target="_blank">source</a>]

```lua
Spring.GetUnitPieceList(UnitID) -> string[]
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `pieceNames` `string[]`

### Spring.GetUnitPieceInfo {#Spring.GetUnitPieceInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8910-L8916" target="_blank">source</a>]

```lua
Spring.GetUnitPieceInfo(UnitID, integer) -> PieceInfo?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceIndex` `integer`

**Returns**

- `pieceInfo` `PieceInfo?`

### Spring.GetUnitPiecePosDir {#Spring.GetUnitPiecePosDir}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8922-L8933" target="_blank">source</a>]

```lua
Spring.GetUnitPiecePosDir(UnitID, integer) -> number?, number, number, number, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceIndex` `integer`

**Returns**

- `posX` `number?`
- `posY` `number`
- `posZ` `number`
- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`

### Spring.GetUnitPiecePosition {#Spring.GetUnitPiecePosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8939-L8947" target="_blank">source</a>]

```lua
Spring.GetUnitPiecePosition(UnitID, integer) -> number?, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceIndex` `integer`

**Returns**

- `posX` `number?`
- `posY` `number`
- `posZ` `number`

### Spring.GetUnitPieceDirection {#Spring.GetUnitPieceDirection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8953-L8961" target="_blank">source</a>]

```lua
Spring.GetUnitPieceDirection(UnitID, integer) -> number?, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceIndex` `integer`

**Returns**

- `dirX` `number?`
- `dirY` `number`
- `dirZ` `number`

### Spring.GetUnitPieceMatrix {#Spring.GetUnitPieceMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8967-L8988" target="_blank">source</a>]

```lua
Spring.GetUnitPieceMatrix(UnitID, integer) -> number?, number, number, number, number, number, number, number, number, number, number, number, number, number, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceIndex` `integer`

**Returns**

- `m11` `number?`
- `m12` `number`
- `m13` `number`
- `m14` `number`
- `m21` `number`
- `m22` `number`
- `m23` `number`
- `m24` `number`
- `m31` `number`
- `m32` `number`
- `m33` `number`
- `m34` `number`
- `m41` `number`
- `m42` `number`
- `m43` `number`
- `m44` `number`

### Spring.GetFeatureRootPiece {#Spring.GetFeatureRootPiece}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8993-L8998" target="_blank">source</a>]

```lua
Spring.GetFeatureRootPiece(FeatureID) -> integer
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `index` `integer` — of the root piece

### Spring.GetFeaturePieceMap {#Spring.GetFeaturePieceMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9003-L9008" target="_blank">source</a>]

```lua
Spring.GetFeaturePieceMap(FeatureID) -> table<string,integer>
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `pieceInfos` `table<string,integer>` — where keys are piece names and values are indices

### Spring.GetFeaturePieceList {#Spring.GetFeaturePieceList}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9014-L9019" target="_blank">source</a>]

```lua
Spring.GetFeaturePieceList(FeatureID) -> string[]
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `pieceNames` `string[]`

### Spring.GetFeaturePieceInfo {#Spring.GetFeaturePieceInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9025-L9031" target="_blank">source</a>]

```lua
Spring.GetFeaturePieceInfo(FeatureID, integer) -> PieceInfo?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceIndex` `integer`

**Returns**

- `pieceInfo` `PieceInfo?`

### Spring.GetFeaturePiecePosDir {#Spring.GetFeaturePiecePosDir}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9037-L9048" target="_blank">source</a>]

```lua
Spring.GetFeaturePiecePosDir(FeatureID, integer) -> number?, number, number, number, number, number
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceIndex` `integer`

**Returns**

- `posX` `number?`
- `posY` `number`
- `posZ` `number`
- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`

### Spring.GetFeaturePiecePosition {#Spring.GetFeaturePiecePosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9054-L9062" target="_blank">source</a>]

```lua
Spring.GetFeaturePiecePosition(FeatureID, integer) -> number?, number, number
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceIndex` `integer`

**Returns**

- `posX` `number?`
- `posY` `number`
- `posZ` `number`

### Spring.GetFeaturePieceDirection {#Spring.GetFeaturePieceDirection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9068-L9076" target="_blank">source</a>]

```lua
Spring.GetFeaturePieceDirection(FeatureID, integer) -> number?, number, number
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceIndex` `integer`

**Returns**

- `dirX` `number?`
- `dirY` `number`
- `dirZ` `number`

### Spring.GetFeaturePieceMatrix {#Spring.GetFeaturePieceMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9082-L9103" target="_blank">source</a>]

```lua
Spring.GetFeaturePieceMatrix(FeatureID, integer) -> number?, number, number, number, number, number, number, number, number, number, number, number, number, number, number, number
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceIndex` `integer`

**Returns**

- `m11` `number?`
- `m12` `number`
- `m13` `number`
- `m14` `number`
- `m21` `number`
- `m22` `number`
- `m23` `number`
- `m24` `number`
- `m31` `number`
- `m32` `number`
- `m33` `number`
- `m34` `number`
- `m41` `number`
- `m42` `number`
- `m43` `number`
- `m44` `number`

### Spring.GetUnitScriptPiece {#Spring.GetUnitScriptPiece}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9108-L9114" target="_blank">source</a>]

```lua
Spring.GetUnitScriptPiece(UnitID) -> integer[]
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `pieceIndices` `integer[]`

### Spring.GetUnitScriptPiece (overload 1) {#Spring.GetUnitScriptPiece-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9115-L9122" target="_blank">source</a>]

```lua
Spring.GetUnitScriptPiece(UnitID, integer) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `scriptPiece` `integer`

**Returns**

- `pieceIndex` `integer`

### Spring.GetUnitScriptNames {#Spring.GetUnitScriptNames}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9154-L9161" target="_blank">source</a>]

```lua
Spring.GetUnitScriptNames(UnitID) -> table<string,integer>
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `pieceInfos` `table<string,integer>` — where keys are piece names and values are piece indices

### Spring.TraceRayInDirection {#Spring.TraceRayInDirection}
*function*

Traces a ray from a position in a direction

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9267-L9283" target="_blank">source</a>]

Returns all unit and/or feature hits along a ray, sorted by distance
from the start position.

```lua
Spring.TraceRayInDirection(number, number, number, number, number, number, number, string) -> table[]
```

**Parameters**

- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`
- `maxLength` `number`
- `type` `string` — Object type to test: `"unit"`, `"feature"`, or `"both"`

**Returns**

- `hits` `table[]` — Array of `{hitLength, objectID, objectType}` entries

### Spring.TraceRayBetweenPositions {#Spring.TraceRayBetweenPositions}
*function*

Traces a ray between two positions

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9293-L9308" target="_blank">source</a>]

Checks for unit and/or feature collisions between two positions
and returns all hits sorted by distance from the start position.

```lua
Spring.TraceRayBetweenPositions(number, number, number, number, number, number, string) -> table[]
```

**Parameters**

- `startX` `number`
- `startY` `number`
- `startZ` `number`
- `endX` `number`
- `endY` `number`
- `endZ` `number`
- `type` `string` — Object type to test: `"unit"`, `"feature"`, or `"both"`

**Returns**

- `hits` `table[]` — Array of `{hitLength, objectID, objectType}` entries

### Spring.TraceRayGroundInDirection {#Spring.TraceRayGroundInDirection}
*function*

Checks for a ground collision in given direction

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9333-L9352" target="_blank">source</a>]

Checks if there is surface (ground, optionally water) towards a vector
and returns the distance to the closest hit and its position, if any.

```lua
Spring.TraceRayGroundInDirection(number, number, number, number, number, number, number?, boolean?) -> number?, number?, number?, number?
```

**Parameters**

- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`
- `maxLength` `number?` — (Default: `999999`)
- `testWater` `boolean?` — (Default: `true`)

**Returns**

- `rayLength` `number?`
- `posX` `number?`
- `posY` `number?`
- `posZ` `number?`

### Spring.TraceRayGroundBetweenPositions {#Spring.TraceRayGroundBetweenPositions}
*function*

Checks for a ground collision between two positions

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9363-L9381" target="_blank">source</a>]

Checks if there is surface (ground, optionally water) between two positions
and returns the distance to the closest hit and its position, if any.

```lua
Spring.TraceRayGroundBetweenPositions(number, number, number, number, number, number, boolean?) -> number, number, number, number
```

**Parameters**

- `startX` `number`
- `startY` `number`
- `startZ` `number`
- `endX` `number`
- `endY` `number`
- `endZ` `number`
- `testWater` `boolean?` — (Default: `true`)

**Returns**

- `rayLength` `number`
- `posX` `number`
- `posY` `number`
- `posZ` `number`

### Spring.GetRadarErrorParams {#Spring.GetRadarErrorParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L9401-L9410" target="_blank">source</a>]

```lua
Spring.GetRadarErrorParams(AllyTeamID) -> number?, number, number
```

**Parameters**

- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)

**Returns**

- `radarErrorSize` `number?` — actual radar error size (when allyTeamID is allied to current team) or base radar error size
- `baseRadarErrorSize` `number`
- `baseRadarErrorMult` `number`

### Spring.SetShockFrontFactors {#Spring.SetShockFrontFactors}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUI.cpp#L676-L681" target="_blank">source</a>]

```lua
Spring.SetShockFrontFactors(number?, number?, number?) -> nil
```

**Parameters**

- `minArea` `number?`
- `minPower` `number?`
- `distAdj` `number?`

### Spring.Ping {#Spring.Ping}
*function*

Send a ping request to the server

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L471-L478" target="_blank">source</a>]

```lua
Spring.Ping(integer?) -> nil
```

**Parameters**

- `pingTag` `integer?`

**Returns**

- `nil`

### Spring.SendCommands {#Spring.SendCommands}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L503-L506" target="_blank">source</a>]

```lua
Spring.SendCommands(string[]) -> nil
```

**Parameters**

- `commands` `string[]`

### Spring.SendCommands (overload 1) {#Spring.SendCommands-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L508-L513" target="_blank">source</a>]

```lua
Spring.SendCommands(string, [string, ]*) -> nil
```

**Parameters**

- `command` `string`
- `...` `string` — additional commands

**Returns**

- `nil`

### Spring.SendPublicChat {#Spring.SendPublicChat}
*function*

Sends a chat message to everyone (players and spectators).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L587-L592" target="_blank">source</a>]

```lua
Spring.SendPublicChat(string) -> nil
```

**Parameters**

- `message` `string`

**Returns**

- `nil`

### Spring.SendAllyChat {#Spring.SendAllyChat}
*function*

Sends a chat message to the sender's ally team (if a spectator, to other spectators).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L603-L608" target="_blank">source</a>]

```lua
Spring.SendAllyChat(string) -> nil
```

**Parameters**

- `message` `string`

**Returns**

- `nil`

### Spring.SendSpectatorChat {#Spring.SendSpectatorChat}
*function*

Sends a chat message to spectators. Works even if you're a player.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L618-L623" target="_blank">source</a>]

```lua
Spring.SendSpectatorChat(string) -> nil
```

**Parameters**

- `message` `string`

**Returns**

- `nil`

### Spring.SendPrivateChat {#Spring.SendPrivateChat}
*function*

Sends a private chat message to a specific player ID.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L633-L639" target="_blank">source</a>]

```lua
Spring.SendPrivateChat(string, PlayerID) -> nil
```

**Parameters**

- `message` `string`
- `playerID` [`PlayerID`](Aliases.md#PlayerID)

**Returns**

- `nil`

### Spring.SendMessage {#Spring.SendMessage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L663-L666" target="_blank">source</a>]

```lua
Spring.SendMessage(string) -> nil
```

**Parameters**

- `message` `string`

**Returns**

- `nil`

### Spring.SendMessageToSpectators {#Spring.SendMessageToSpectators}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L674-L683" target="_blank">source</a>]

```lua
Spring.SendMessageToSpectators(string) -> nil
```

**Parameters**

- `message` `string` — ``"`<PLAYER#>`"`` where `#` is a player ID.

This will be replaced with the player's name. e.g.
```lua
Spring.SendMessage("`<PLAYER1>` did something") -- "ProRusher did something"
```

**Returns**

- `nil`

### Spring.SendMessageToPlayer {#Spring.SendMessageToPlayer}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L693-L697" target="_blank">source</a>]

```lua
Spring.SendMessageToPlayer(PlayerID, string) -> nil
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `message` `string`

**Returns**

- `nil`

### Spring.SendMessageToTeam {#Spring.SendMessageToTeam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L707-L711" target="_blank">source</a>]

```lua
Spring.SendMessageToTeam(TeamID, string) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `message` `string`

**Returns**

- `nil`

### Spring.SendMessageToAllyTeam {#Spring.SendMessageToAllyTeam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L721-L725" target="_blank">source</a>]

```lua
Spring.SendMessageToAllyTeam(AllyTeamID, string) -> nil
```

**Parameters**

- `allyID` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `message` `string`

**Returns**

- `nil`

### Spring.RequestStartPosition {#Spring.RequestStartPosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L734-L742" target="_blank">source</a>]

Requests a startpoint, as if clicking the spot with the native GUI.

```lua
Spring.RequestStartPosition(number, number, number, boolean?) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`
- `ready` `boolean?`

### Spring.LoadSoundDef {#Spring.LoadSoundDef}
*function*

Loads a SoundDefs file, the format is the same as in `gamedata/sounds.lua`.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L767-L772" target="_blank">source</a>]

```lua
Spring.LoadSoundDef(string) -> boolean
```

**Parameters**

- `soundfile` `string`

**Returns**

- `success` `boolean`

### Spring.PlaySoundFile {#Spring.PlaySoundFile}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L799-L810" target="_blank">source</a>]

```lua
Spring.PlaySoundFile(string, number?, number?, number?, number?, number?, number?, number?, SoundChannel?) -> boolean
```

**Parameters**

- `soundfile` `string`
- `volume` `number?` — (Default: 1.0) optional; all following arguments are optional
- `posx` `number?` — world position X (use with `posy` and `posz`, or omit all three)
- `posy` `number?`
- `posz` `number?`
- `speedx` `number?` — velocity X (use with `speedy` and `speedz` after position, or omit all three)
- `speedy` `number?`
- `speedz` `number?`
- `channel` `SoundChannel?` — (Default: `0|"general"`) optional; parsed from the last argument index after position and speed triples

**Returns**

- `playSound` `boolean`

### Spring.PlaySoundStream {#Spring.PlaySoundStream}
*function*

Allows to play an Ogg Vorbis (.OGG) and mp3 compressed sound file.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L890-L901" target="_blank">source</a>]

Multiple sound streams may be played at once.

```lua
Spring.PlaySoundStream(string, number?, boolean?) -> boolean
```

**Parameters**

- `oggfile` `string`
- `volume` `number?` — (Default: 1.0)
- `enqueue` `boolean?`

**Returns**

- `success` `boolean`

### Spring.StopSoundStream {#Spring.StopSoundStream}
*function*

Terminates any SoundStream currently running.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L914-L918" target="_blank">source</a>]

```lua
Spring.StopSoundStream() -> nil
```

**Returns**

- `nil`

### Spring.PauseSoundStream {#Spring.PauseSoundStream}
*function*

Pause any SoundStream currently running.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L926-L930" target="_blank">source</a>]

```lua
Spring.PauseSoundStream() -> nil
```

**Returns**

- `nil`

### Spring.SetSoundStreamVolume {#Spring.SetSoundStreamVolume}
*function*

Set volume for SoundStream

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L938-L943" target="_blank">source</a>]

```lua
Spring.SetSoundStreamVolume(number) -> nil
```

**Parameters**

- `volume` `number`

**Returns**

- `nil`

### Spring.SetSoundEffectParams {#Spring.SetSoundEffectParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L951-L952" target="_blank">source</a>]

```lua
Spring.SetSoundEffectParams() -> nil
```

### Spring.AddWorldIcon {#Spring.AddWorldIcon}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1061-L1069" target="_blank">source</a>]

```lua
Spring.AddWorldIcon(integer, number, number, number) -> nil
```

**Parameters**

- `cmdID` `integer`
- `posX` `number`
- `posY` `number`
- `posZ` `number`

**Returns**

- `nil`

### Spring.AddWorldText {#Spring.AddWorldText}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1081-L1089" target="_blank">source</a>]

```lua
Spring.AddWorldText(string, number, number, number) -> nil
```

**Parameters**

- `text` `string`
- `posX` `number`
- `posY` `number`
- `posZ` `number`

**Returns**

- `nil`

### Spring.AddWorldUnit {#Spring.AddWorldUnit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1101-L1111" target="_blank">source</a>]

```lua
Spring.AddWorldUnit(UnitDefID, number, number, number, TeamID, FacingInteger) -> nil
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `teamID` [`TeamID`](Aliases.md#TeamID)
- `facing` [`FacingInteger`](Aliases.md#FacingInteger)

**Returns**

- `nil`

### Spring.DrawUnitCommands {#Spring.DrawUnitCommands}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1134-L1137" target="_blank">source</a>]

```lua
Spring.DrawUnitCommands(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### Spring.DrawUnitCommands (overload 1) {#Spring.DrawUnitCommands-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1138-L1142" target="_blank">source</a>]

```lua
Spring.DrawUnitCommands(UnitID[], false?) -> nil
```

**Parameters**

- `unitIDs` `UnitID[]` — Unit ids.
- `tableOrArray` `false?` — Set to `true` if the unit IDs should be read from the keys of `unitIDs`.

### Spring.DrawUnitCommands (overload 2) {#Spring.DrawUnitCommands-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1143-L1148" target="_blank">source</a>]

```lua
Spring.DrawUnitCommands(table<UnitID,any>, true) -> nil
```

**Parameters**

- `unitIDs` `table<UnitID,any>` — Table with unit IDs as keys.
- `tableOrArray` `true` — Set to `false` if the unit IDs should be read from the values of `unitIDs`.

**Returns**

- `nil`

### Spring.SetCameraTarget {#Spring.SetCameraTarget}
*function*

For Spring Engine XZ represents horizontal, from north west corner of map and Y vertical, from water level and rising.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1208-L1220" target="_blank">source</a>]

```lua
Spring.SetCameraTarget(number, number, number, number?, number?, number?, number?) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`
- `transTime` `number?` — (Default: `0.5`) transition duration; values below zero are clamped to zero
- `dirX` `number?` — (Default: current camera direction X)
- `dirY` `number?` — (Default: current camera direction Y)
- `dirZ` `number?` — (Default: current camera direction Z)

**Returns**

- `nil`

### Spring.SetCameraOffset {#Spring.SetCameraOffset}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1249-L1260" target="_blank">source</a>]

```lua
Spring.SetCameraOffset(number?, number?, number?, number?, number?, number?) -> nil
```

**Parameters**

- `posX` `number?` — (Default: `0`)
- `posY` `number?` — (Default: `0`)
- `posZ` `number?` — (Default: `0`)
- `tiltX` `number?` — (Default: `0`)
- `tiltY` `number?` — (Default: `0`)
- `tiltZ` `number?` — (Default: `0`)

**Returns**

- `nil`

### Spring.SetCameraState {#Spring.SetCameraState}
*function*

Set camera state.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1274-L1295" target="_blank">source</a>]

```lua
Spring.SetCameraState(CameraState, number?, number?, number?) -> boolean
```

**Parameters**

- `cameraState` [`CameraState`](CameraState.md#CameraState) — The fields must be consistent with the name/mode and current/new camera mode.
- `transitionTime` `number?` — (Default: `0`) in nanoseconds
- `transitionTimeFactor` `number?`
- `transitionTimeExponent` `number?`

**Returns**

- `set` `boolean` — `true` when applied without errors, otherwise `false`.

### Spring.RunDollyCamera {#Spring.RunDollyCamera}
*function*

Runs Dolly Camera

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1318-L1323" target="_blank">source</a>]

```lua
Spring.RunDollyCamera(number) -> nil
```

**Parameters**

- `runtime` `number` — Runtime in milliseconds.

**Returns**

- `nil`

### Spring.PauseDollyCamera {#Spring.PauseDollyCamera}
*function*

Pause Dolly Camera

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1333-L1338" target="_blank">source</a>]

```lua
Spring.PauseDollyCamera(number?) -> nil
```

**Parameters**

- `fraction` `number?` — Fraction of the total runtime to pause at, 0 to 1 inclusive. A null value pauses at current percent

**Returns**

- `nil`

### Spring.ResumeDollyCamera {#Spring.ResumeDollyCamera}
*function*

Resume Dolly Camera

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1348-L1352" target="_blank">source</a>]

```lua
Spring.ResumeDollyCamera() -> nil
```

**Returns**

- `nil`

### Spring.SetDollyCameraPosition {#Spring.SetDollyCameraPosition}
*function*

Sets Dolly Camera Position

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1360-L1367" target="_blank">source</a>]

```lua
Spring.SetDollyCameraPosition(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`

**Returns**

- `nil`

### Spring.SetDollyCameraCurve {#Spring.SetDollyCameraCurve}
*function*

Sets Dolly Camera movement Curve

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1390-L1397" target="_blank">source</a>]

```lua
Spring.SetDollyCameraCurve(integer, ControlPoint[], table) -> nil
```

**Parameters**

- `degree` `integer`
- `cpoints` `ControlPoint[]` — NURBS control point positions.
- `knots` `table`

**Returns**

- `nil`

### Spring.SetDollyCameraMode {#Spring.SetDollyCameraMode}
*function*

Sets Dolly Camera movement mode

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1413-L1418" target="_blank">source</a>]

```lua
Spring.SetDollyCameraMode((1|2)) -> nil
```

**Parameters**

- `mode` `(1|2)` — `1` static position, `2` nurbs curve

**Returns**

- `nil`

### Spring.SetDollyCameraRelativeMode {#Spring.SetDollyCameraRelativeMode}
*function*

Sets Dolly Camera movement curve to world relative or look target relative

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1428-L1433" target="_blank">source</a>]

```lua
Spring.SetDollyCameraRelativeMode(integer) -> nil
```

**Parameters**

- `relativeMode` `integer` — `1` world, `2` look target

**Returns**

- `nil`

### Spring.SetDollyCameraLookCurve {#Spring.SetDollyCameraLookCurve}
*function*

Sets Dolly Camera Look Curve

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1444-L1451" target="_blank">source</a>]

```lua
Spring.SetDollyCameraLookCurve(integer, ControlPoint[], table) -> nil
```

**Parameters**

- `degree` `integer`
- `cpoints` `ControlPoint[]` — NURBS control point positions.
- `knots` `table`

**Returns**

- `nil`

### Spring.SetDollyCameraLookPosition {#Spring.SetDollyCameraLookPosition}
*function*

Sets Dolly Camera Look Position

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1468-L1475" target="_blank">source</a>]

```lua
Spring.SetDollyCameraLookPosition(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`

**Returns**

- `nil`

### Spring.SetDollyCameraLookUnit {#Spring.SetDollyCameraLookUnit}
*function*

Sets target unit for Dolly Camera to look towards

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1488-L1493" target="_blank">source</a>]

```lua
Spring.SetDollyCameraLookUnit(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID) — The unit to look at.

**Returns**

- `nil`

### Spring.SelectUnit {#Spring.SelectUnit}
*function*

Selects a single unit

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1511-L1517" target="_blank">source</a>]

```lua
Spring.SelectUnit(UnitID?, boolean?) -> nil
```

**Parameters**

- `unitID` `UnitID?`
- `append` `boolean?` — (Default: `false`) Append to current selection.

**Returns**

- `nil`

### Spring.DeselectUnit {#Spring.DeselectUnit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1535-L1540" target="_blank">source</a>]

```lua
Spring.DeselectUnit(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `nil`

### Spring.DeselectUnitArray {#Spring.DeselectUnitArray}
*function*

Deselects multiple units.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1577-L1582" target="_blank">source</a>]

```lua
Spring.DeselectUnitArray(UnitID[]) -> nil
```

**Parameters**

- `unitIDs` `UnitID[]` — Table with unit IDs as values.

**Returns**

- `nil`

### Spring.DeselectUnitMap {#Spring.DeselectUnitMap}
*function*

Deselects multiple units.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1588-L1593" target="_blank">source</a>]

```lua
Spring.DeselectUnitMap(table<UnitID,any>) -> nil
```

**Parameters**

- `unitMap` `table<UnitID,any>` — Table with unit IDs as keys.

**Returns**

- `nil`

### Spring.SelectUnitArray {#Spring.SelectUnitArray}
*function*

Selects multiple units, or appends to selection. Accepts a table with unitIDs as values

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1599-L1605" target="_blank">source</a>]

```lua
Spring.SelectUnitArray(UnitID[], boolean?) -> nil
```

**Parameters**

- `unitIDs` `UnitID[]` — Table with unit IDs as values.
- `append` `boolean?` — (Default: `false`) append to current selection

**Returns**

- `nil`

### Spring.SelectUnitMap {#Spring.SelectUnitMap}
*function*

Selects multiple units, or appends to selection. Accepts a table with unitIDs as keys

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1611-L1617" target="_blank">source</a>]

```lua
Spring.SelectUnitMap(table<UnitID,any>, boolean?) -> nil
```

**Parameters**

- `unitMap` `table<UnitID,any>` — Table with unit IDs as keys.
- `append` `boolean?` — (Default: `false`) append to current selection

**Returns**

- `nil`

### Spring.AddMapLight {#Spring.AddMapLight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1769-L1776" target="_blank">source</a>]

requires MaxDynamicMapLights > 0

```lua
Spring.AddMapLight(LightParams) -> integer
```

**Parameters**

- `lightParams` [`LightParams`](LightParams.md#LightParams)

**Returns**

- `lightHandle` `integer`

### Spring.AddModelLight {#Spring.AddModelLight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1795-L1802" target="_blank">source</a>]

requires MaxDynamicMapLights > 0

```lua
Spring.AddModelLight(LightParams) -> integer
```

**Parameters**

- `lightParams` [`LightParams`](LightParams.md#LightParams)

**Returns**

- `lightHandle` `integer`

### Spring.UpdateMapLight {#Spring.UpdateMapLight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1821-L1827" target="_blank">source</a>]

```lua
Spring.UpdateMapLight(integer, LightParams) -> boolean
```

**Parameters**

- `lightHandle` `integer`
- `lightParams` [`LightParams`](LightParams.md#LightParams)

**Returns**

- `success` `boolean`

### Spring.UpdateModelLight {#Spring.UpdateModelLight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1843-L1849" target="_blank">source</a>]

```lua
Spring.UpdateModelLight(integer, LightParams) -> boolean
```

**Parameters**

- `lightHandle` `integer`
- `lightParams` [`LightParams`](LightParams.md#LightParams)

**Returns**

- `success` `boolean`

### Spring.AddLightTrackingTarget {#Spring.AddLightTrackingTarget}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1865-L1867" target="_blank">source</a>]

```lua
Spring.AddLightTrackingTarget() -> nil
```

### Spring.SetMapLightTrackingState {#Spring.SetMapLightTrackingState}
*function*

Set a map-illuminating light to start/stop tracking the position of a moving object (unit or projectile)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1922-L1931" target="_blank">source</a>]

```lua
Spring.SetMapLightTrackingState(integer, (UnitID|ProjectileID), boolean?, boolean?) -> boolean
```

**Parameters**

- `lightHandle` `integer`
- `unitOrProjectileID` `(UnitID|ProjectileID)`
- `enableTracking` `boolean?`
- `unitOrProjectile` `boolean?`

**Returns**

- `success` `boolean`

### Spring.SetModelLightTrackingState {#Spring.SetModelLightTrackingState}
*function*

Set a model-illuminating light to start/stop tracking the position of a moving object (unit or projectile)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1958-L1967" target="_blank">source</a>]

```lua
Spring.SetModelLightTrackingState(integer, (UnitID|ProjectileID), boolean?, boolean?) -> boolean
```

**Parameters**

- `lightHandle` `integer`
- `unitOrProjectileID` `(UnitID|ProjectileID)`
- `enableTracking` `boolean?`
- `unitOrProjectile` `boolean?`

**Returns**

- `success` `boolean`

### Spring.SetMapShader {#Spring.SetMapShader}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2000-L2009" target="_blank">source</a>]

The ID's must refer to valid programs returned by [gl.CreateShader](gl.md#gl.CreateShader).
Passing in a value of 0 will cause the respective shader to revert back to its engine default.
Custom map shaders that declare a uniform ivec2 named "texSquare" can sample from the default diffuse texture(s), which are always bound to TU 0.

```lua
Spring.SetMapShader(integer, integer) -> nil
```

**Parameters**

- `standardShaderID` `integer`
- `deferredShaderID` `integer`

**Returns**

- `nil`

### Spring.SetMapSquareTexture {#Spring.SetMapSquareTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2029-L2034" target="_blank">source</a>]

```lua
Spring.SetMapSquareTexture(integer, integer, string) -> boolean
```

**Parameters**

- `texSqrX` `integer`
- `texSqrY` `integer`
- `luaTexName` `string`

**Returns**

- `success` `boolean`

### Spring.SetMapShadingTexture {#Spring.SetMapShadingTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2126-L2131" target="_blank">source</a>]

```lua
Spring.SetMapShadingTexture(string, string) -> boolean
```

**Parameters**

- `texType` `string`
- `texName` `string`

**Returns**

- `success` `boolean`

### Spring.SetSkyBoxTexture {#Spring.SetSkyBoxTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2147-L2150" target="_blank">source</a>]

```lua
Spring.SetSkyBoxTexture(string) -> nil
```

**Parameters**

- `texName` `string`

**Returns**

- `nil`

### Spring.SetUnitNoDraw {#Spring.SetUnitNoDraw}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2168-L2174" target="_blank">source</a>]

```lua
Spring.SetUnitNoDraw(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `noDraw` `boolean`

**Returns**

- `nil`

### Spring.SetUnitEngineDrawMask {#Spring.SetUnitEngineDrawMask}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2187-L2193" target="_blank">source</a>]

```lua
Spring.SetUnitEngineDrawMask(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `drawMask` `number`

**Returns**

- `nil`

### Spring.SetUnitAlwaysUpdateMatrix {#Spring.SetUnitAlwaysUpdateMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2206-L2212" target="_blank">source</a>]

```lua
Spring.SetUnitAlwaysUpdateMatrix(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `alwaysUpdateMatrix` `boolean`

**Returns**

- `nil`

### Spring.SetUnitNoMinimap {#Spring.SetUnitNoMinimap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2225-L2231" target="_blank">source</a>]

```lua
Spring.SetUnitNoMinimap(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitNoMinimap` `boolean`

**Returns**

- `nil`

### Spring.SetMiniMapRotation {#Spring.SetMiniMapRotation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2243-L2247" target="_blank">source</a>]

```lua
Spring.SetMiniMapRotation(number) -> nil
```

**Parameters**

- `rotation` `number` — amount in radians

**Returns**

- `nil`

### Spring.SetUnitNoGroup {#Spring.SetUnitNoGroup}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2273-L2278" target="_blank">source</a>]

```lua
Spring.SetUnitNoGroup(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitNoGroup` `boolean` — Whether unit can be added to selection groups

### Spring.SetUnitNoSelect {#Spring.SetUnitNoSelect}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2295-L2301" target="_blank">source</a>]

```lua
Spring.SetUnitNoSelect(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitNoSelect` `boolean` — whether unit can be selected or not

**Returns**

- `nil`

### Spring.SetUnitLeaveTracks {#Spring.SetUnitLeaveTracks}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2323-L2329" target="_blank">source</a>]

```lua
Spring.SetUnitLeaveTracks(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitLeaveTracks` `boolean` — whether unit leaves tracks on movement

**Returns**

- `nil`

### Spring.SetUnitSelectionVolumeData {#Spring.SetUnitSelectionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2342-L2356" target="_blank">source</a>]

```lua
Spring.SetUnitSelectionVolumeData(UnitID, number, number, number, number, number, number, integer, integer, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `scaleX` `number`
- `scaleY` `number`
- `scaleZ` `number`
- `offsetX` `number`
- `offsetY` `number`
- `offsetZ` `number`
- `vType` `integer`
- `tType` `integer`
- `Axis` `integer`

**Returns**

- `nil`

### Spring.SetFeatureNoDraw {#Spring.SetFeatureNoDraw}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2374-L2382" target="_blank">source</a>]

```lua
Spring.SetFeatureNoDraw(FeatureID, boolean) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `noDraw` `boolean`

**Returns**

- `nil`

### Spring.SetFeatureEngineDrawMask {#Spring.SetFeatureEngineDrawMask}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2395-L2401" target="_blank">source</a>]

```lua
Spring.SetFeatureEngineDrawMask(FeatureID, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `engineDrawMask` `number`

**Returns**

- `nil`

### Spring.SetFeatureAlwaysUpdateMatrix {#Spring.SetFeatureAlwaysUpdateMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2414-L2420" target="_blank">source</a>]

```lua
Spring.SetFeatureAlwaysUpdateMatrix(FeatureID, number) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `alwaysUpdateMat` `number`

**Returns**

- `nil`

### Spring.SetFeatureFade {#Spring.SetFeatureFade}
*function*

Control whether a feature will fade or not when zoomed out.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2433-L2441" target="_blank">source</a>]

```lua
Spring.SetFeatureFade(FeatureID, boolean) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `allow` `boolean`

**Returns**

- `nil`

### Spring.SetFeatureSelectionVolumeData {#Spring.SetFeatureSelectionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2454-L2469" target="_blank">source</a>]

```lua
Spring.SetFeatureSelectionVolumeData(FeatureID, number, number, number, number, number, number, integer, integer, integer) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `scaleX` `number`
- `scaleY` `number`
- `scaleZ` `number`
- `offsetX` `number`
- `offsetY` `number`
- `offsetZ` `number`
- `vType` `integer`
- `tType` `integer`
- `Axis` `integer`

**Returns**

- `nil`

### Spring.AddUnitIcon {#Spring.AddUnitIcon}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2488-L2504" target="_blank">source</a>]

```lua
Spring.AddUnitIcon(string, string, number?, number?, number?, number?, number?, number?, number?, number?) -> boolean
```

**Parameters**

- `iconName` `string`
- `texFile` `string`
- `size` `number?`
- `dist` `number?`
- `radAdjust` `number?`
- `u0` `number?`
- `v0` `number?`
- `u1` `number?`
- `v1` `number?`
- `drawOrder` `number?` — (Default: 0) Sort priority for icon drawing; icons with higher values are drawn on top of lower ones.

**Returns**

- `added` `boolean`

### Spring.FreeUnitIcon {#Spring.FreeUnitIcon}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2531-L2538" target="_blank">source</a>]

```lua
Spring.FreeUnitIcon(string) -> boolean?
```

**Parameters**

- `iconName` `string`

**Returns**

- `freed` `boolean?`

### Spring.UnitIconSetDraw {#Spring.UnitIconSetDraw}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2549-L2557" target="_blank">source</a>]

Use Spring.SetUnitIconDraw instead.

**Deprecated:** 

```lua
Spring.UnitIconSetDraw(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `drawIcon` `boolean`

**Returns**

- `nil`

### Spring.SetUnitIconDraw {#Spring.SetUnitIconDraw}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2565-L2571" target="_blank">source</a>]

```lua
Spring.SetUnitIconDraw(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `drawIcon` `boolean`

**Returns**

- `nil`

### Spring.SetUnitIcon {#Spring.SetUnitIcon}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2583-L2589" target="_blank">source</a>]

```lua
Spring.SetUnitIcon(UnitID, string?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `iconName` `string?` — supply nil to reset to the default

**Returns**

- `nil`

### Spring.SetUnitDefIcon {#Spring.SetUnitDefIcon}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2618-L2626" target="_blank">source</a>]

```lua
Spring.SetUnitDefIcon(UnitDefID, string) -> nil
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `iconName` `string`

**Returns**

- `nil`

### Spring.SetUnitDefImage {#Spring.SetUnitDefImage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2666-L2674" target="_blank">source</a>]

```lua
Spring.SetUnitDefImage(UnitDefID, string?) -> nil
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `image` `string?` — luaTexture|texFile

**Returns**

- `nil`

### Spring.ExtractModArchiveFile {#Spring.ExtractModArchiveFile}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2718-L2723" target="_blank">source</a>]

```lua
Spring.ExtractModArchiveFile(string) -> boolean
```

**Parameters**

- `modfile` `string`

**Returns**

- `extracted` `boolean`

### Spring.CreateDir {#Spring.CreateDir}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2782-L2787" target="_blank">source</a>]

```lua
Spring.CreateDir(string) -> boolean?
```

**Parameters**

- `path` `string`

**Returns**

- `dirCreated` `boolean?`

### Spring.SetActiveCommand {#Spring.SetActiveCommand}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2860-L2865" target="_blank">source</a>]

```lua
Spring.SetActiveCommand(string, string?) -> boolean?
```

**Parameters**

- `action` `string`
- `actionExtra` `string?`

**Returns**

- `commandSet` `boolean?`

### Spring.SetActiveCommand (overload 1) {#Spring.SetActiveCommand-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2867-L2877" target="_blank">source</a>]

```lua
Spring.SetActiveCommand(integer, integer?, boolean?, boolean?, boolean?, boolean?, boolean?, boolean?) -> boolean?
```

**Parameters**

- `cmdIndex` `integer`
- `button` `integer?` — (Default: `1`)
- `leftClick` `boolean?`
- `rightClick` `boolean?`
- `alt` `boolean?`
- `ctrl` `boolean?`
- `meta` `boolean?`
- `shift` `boolean?`

**Returns**

- `commandSet` `boolean?`

### Spring.LoadCmdColorsConfig {#Spring.LoadCmdColorsConfig}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2899-L2902" target="_blank">source</a>]

```lua
Spring.LoadCmdColorsConfig(string) -> nil
```

**Parameters**

- `config` `string`

**Returns**

- `nil`

### Spring.LoadCtrlPanelConfig {#Spring.LoadCtrlPanelConfig}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2910-L2913" target="_blank">source</a>]

```lua
Spring.LoadCtrlPanelConfig(string) -> nil
```

**Parameters**

- `config` `string`

**Returns**

- `nil`

### Spring.ForceLayoutUpdate {#Spring.ForceLayoutUpdate}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2924-L2926" target="_blank">source</a>]

```lua
Spring.ForceLayoutUpdate() -> nil
```

**Returns**

- `nil`

### Spring.SetDrawSelectionInfo {#Spring.SetDrawSelectionInfo}
*function*

Disables the "Selected Units x" box in the GUI.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2937-L2942" target="_blank">source</a>]

```lua
Spring.SetDrawSelectionInfo(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

**Returns**

- `nil`

### Spring.SetBoxSelectionByEngine {#Spring.SetBoxSelectionByEngine}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2952-L2957" target="_blank">source</a>]

```lua
Spring.SetBoxSelectionByEngine(boolean) -> nil
```

**Parameters**

- `state` `boolean`

**Returns**

- `nil`

### Spring.SetTeamColor {#Spring.SetTeamColor}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2966-L2975" target="_blank">source</a>]

```lua
Spring.SetTeamColor(TeamID, number, number, number, number?) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `r` `number`
- `g` `number`
- `b` `number`
- `alpha` `number?`

**Returns**

- `nil`

### Spring.SetCustomPaletteColor {#Spring.SetCustomPaletteColor}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L2994-L3002" target="_blank">source</a>]

```lua
Spring.SetCustomPaletteColor(integer, number, number, number) -> nil
```

**Parameters**

- `index` `integer` — 0-based index into custom palette (0..1791, maps to palette slots 256..2047)
- `r` `number`
- `g` `number`
- `b` `number`

**Returns**

- `nil`

### Spring.SetUnitPaletteIndex {#Spring.SetUnitPaletteIndex}
*function*

Sets a custom color for a unit from the palette. Custom assignments are permanent
until explicitly reset by passing nil, and are NOT affected by team changes.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3016-L3023" target="_blank">source</a>]

```lua
Spring.SetUnitPaletteIndex(UnitID, integer?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `customIndex` `integer?` — [0..MAX_CUSTOM_COLORS) index into custom palette, or nil to reset to team color

**Returns**

- `nil`

### Spring.SetFeaturePaletteIndex {#Spring.SetFeaturePaletteIndex}
*function*

Sets a custom color for a feature from the palette. Custom assignments are permanent
until explicitly reset by passing nil, and are NOT affected by team changes.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3042-L3049" target="_blank">source</a>]

```lua
Spring.SetFeaturePaletteIndex(FeatureID, integer?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `customIndex` `integer?` — [0..MAX_CUSTOM_COLORS) index into custom palette, or nil to reset to team color

**Returns**

- `nil`

### Spring.AssignMouseCursor {#Spring.AssignMouseCursor}
*function*

Changes/creates the cursor of a single CursorCmd.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3071-L3082" target="_blank">source</a>]

```lua
Spring.AssignMouseCursor(string, string, boolean?, boolean?) -> boolean?
```

**Parameters**

- `cmdName` `string`
- `iconFileName` `string` — not the full filename, instead it is like this:
Wanted filename: Anims/cursorattack_0.bmp
=> iconFileName: cursorattack
- `overwrite` `boolean?` — (Default: `true`)
- `hotSpotTopLeft` `boolean?` — (Default: `false`)

**Returns**

- `assigned` `boolean?`

### Spring.ReplaceMouseCursor {#Spring.ReplaceMouseCursor}
*function*

Mass replace all occurrences of the cursor in all CursorCmds.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3098-L3105" target="_blank">source</a>]

```lua
Spring.ReplaceMouseCursor(string, string, boolean?) -> boolean?
```

**Parameters**

- `oldFileName` `string`
- `newFileName` `string`
- `hotSpotTopLeft` `boolean?` — (Default: `false`)

**Returns**

- `assigned` `boolean?`

### Spring.SetCustomCommandDrawData {#Spring.SetCustomCommandDrawData}
*function*

Register your custom cmd so it gets visible in the unit's cmd queue

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3123-L3131" target="_blank">source</a>]

```lua
Spring.SetCustomCommandDrawData(integer, (string|integer)?, rgba?, boolean?) -> nil
```

**Parameters**

- `cmdID` `integer`
- `cmdReference` `(string|integer)?` — The name or ID of an icon for command. Pass `nil` to clear draw data for command.
- `color` `rgba?` — (Default: white)
- `showArea` `boolean?` — (Default: `false`)

**Returns**

- `nil`

### Spring.WarpMouse {#Spring.WarpMouse}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3170-L3174" target="_blank">source</a>]

```lua
Spring.WarpMouse(integer, integer) -> nil
```

**Parameters**

- `x` `integer`
- `y` `integer`

**Returns**

- `nil`

### Spring.SetMouseCursor {#Spring.SetMouseCursor}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3184-L3188" target="_blank">source</a>]

```lua
Spring.SetMouseCursor(string, number?) -> nil
```

**Parameters**

- `cursorName` `string`
- `cursorScale` `number?` — (Default: `1.0`)

**Returns**

- `nil`

### Spring.SetLosViewColors {#Spring.SetLosViewColors}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3205-L3212" target="_blank">source</a>]

```lua
Spring.SetLosViewColors(rgb, rgb, rgb, rgb, rgb) -> nil
```

**Parameters**

- `always` [`rgb`](rgb.md#rgb)
- `LOS` [`rgb`](rgb.md#rgb)
- `radar` [`rgb`](rgb.md#rgb)
- `jam` [`rgb`](rgb.md#rgb)
- `radar2` [`rgb`](rgb.md#rgb)

**Returns**

- `nil`

### Spring.SetNanoProjectileParams {#Spring.SetNanoProjectileParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3253-L3263" target="_blank">source</a>]

```lua
Spring.SetNanoProjectileParams(number?, number?, number?, number?, number?, number?) -> nil
```

**Parameters**

- `rotVal` `number?` — (Default: `0`) in degrees
- `rotVel` `number?` — (Default: `0`) in degrees
- `rotAcc` `number?` — (Default: `0`) in degrees
- `rotValRng` `number?` — (Default: `0`) in degrees
- `rotVelRng` `number?` — (Default: `0`) in degrees
- `rotAccRng` `number?` — (Default: `0`) in degrees

**Returns**

- `nil`

### Spring.SetConfigInt {#Spring.SetConfigInt}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3289-L3296" target="_blank">source</a>]

```lua
Spring.SetConfigInt(string, integer, boolean?) -> nil
```

**Parameters**

- `name` `string`
- `value` `integer`
- `useOverlay` `boolean?` — (Default: `false`) If `true`, the value will only be set in memory, and not be restored for the next game.

**Returns**

- `nil`

### Spring.SetConfigFloat {#Spring.SetConfigFloat}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3318-L3325" target="_blank">source</a>]

```lua
Spring.SetConfigFloat(string, number, boolean?) -> nil
```

**Parameters**

- `name` `string`
- `value` `number`
- `useOverlay` `boolean?` — (Default: `false`) If `true`, the value will only be set in memory, and not be restored for the next game.

**Returns**

- `nil`

### Spring.SetConfigString {#Spring.SetConfigString}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3342-L3349" target="_blank">source</a>]

```lua
Spring.SetConfigString(string, string, boolean?) -> nil
```

**Parameters**

- `name` `string`
- `value` `string`
- `useOverlay` `boolean?` — (Default: `false`) If `true`, the value will only be set in memory, and not be restored for the next game.

**Returns**

- `nil`

### Spring.Quit {#Spring.Quit}
*function*

Closes the application

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3421-L3425" target="_blank">source</a>]

```lua
Spring.Quit() -> nil
```

**Returns**

- `nil`

### Spring.SetUnitGroup {#Spring.SetUnitGroup}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3437-L3443" target="_blank">source</a>]

```lua
Spring.SetUnitGroup(UnitID, GroupID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `groupID` [`GroupID`](Aliases.md#GroupID) — the group number to be assigned, or -1 for deassignment

**Returns**

- `nil`

### Spring.GiveOrder {#Spring.GiveOrder}
*function*

Give order to selected units.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3533-L3542" target="_blank">source</a>]

```lua
Spring.GiveOrder((CMD|integer), CreateCommandParams?, CreateCommandOptions?, integer?) -> boolean
```

**Parameters**

- `cmdID` `(CMD|integer)` — The command ID.
- `params` `CreateCommandParams?` — Parameters for the given command.
- `options` `CreateCommandOptions?`
- `timeout` `integer?` — Absolute frame number. The command will be discarded after this frame. Only respected by mobile units.

**Returns**

- `boolean`

### Spring.SetBuildSpacing {#Spring.SetBuildSpacing}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3768-L3773" target="_blank">source</a>]

```lua
Spring.SetBuildSpacing(integer) -> nil
```

**Parameters**

- `spacing` `integer`

**Returns**

- `nil`

### Spring.SetBuildFacing {#Spring.SetBuildFacing}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3783-L3788" target="_blank">source</a>]

```lua
Spring.SetBuildFacing(FacingInteger) -> nil
```

**Parameters**

- `facing` [`FacingInteger`](Aliases.md#FacingInteger)

**Returns**

- `nil`

### Spring.SendLuaUIMsg {#Spring.SendLuaUIMsg}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3805-L3809" target="_blank">source</a>]

```lua
Spring.SendLuaUIMsg(string, string?) -> nil
```

**Parameters**

- `message` `string`
- `mode` `string?` — "s"/"specs" | "a"/"allies"

**Returns**

- `nil`

### Spring.SendLuaGaiaMsg {#Spring.SendLuaGaiaMsg}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3830-L3833" target="_blank">source</a>]

```lua
Spring.SendLuaGaiaMsg(string) -> nil
```

**Parameters**

- `message` `string`

**Returns**

- `nil`

### Spring.SendLuaRulesMsg {#Spring.SendLuaRulesMsg}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3849-L3852" target="_blank">source</a>]

```lua
Spring.SendLuaRulesMsg(string) -> nil
```

**Parameters**

- `message` `string`

**Returns**

- `nil`

### Spring.SendLuaMenuMsg {#Spring.SendLuaMenuMsg}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3867-L3872" target="_blank">source</a>]

```lua
Spring.SendLuaMenuMsg(string) -> nil
```

**Parameters**

- `msg` `string`

### Spring.SetShareLevel {#Spring.SetShareLevel}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3888-L3895" target="_blank">source</a>]

```lua
Spring.SetShareLevel(string, number) -> nil
```

**Parameters**

- `resource` `string` — metal | energy
- `shareLevel` `number`

**Returns**

- `nil`

### Spring.ShareResources {#Spring.ShareResources}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3919-L3926" target="_blank">source</a>]

```lua
Spring.ShareResources(TeamID, string) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `units` `string`

**Returns**

- `nil`

### Spring.ShareResources (overload 1) {#Spring.ShareResources-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3928-L3936" target="_blank">source</a>]

```lua
Spring.ShareResources(TeamID, string, number) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `resource` `string` — metal | energy
- `amount` `number`

**Returns**

- `nil`

### Spring.SetLastMessagePosition {#Spring.SetLastMessagePosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L3984-L3989" target="_blank">source</a>]

```lua
Spring.SetLastMessagePosition(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`

**Returns**

- `nil`

### Spring.MarkerAddPoint {#Spring.MarkerAddPoint}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4007-L4015" target="_blank">source</a>]

```lua
Spring.MarkerAddPoint(number, number, number, string?, boolean?, PlayerID?) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`
- `text` `string?` — (Default: `""`)
- `localOnly` `boolean?`
- `playerID` `PlayerID?` — Local labels pretend they are from this player

**Returns**

- `nil`

### Spring.MarkerAddLine {#Spring.MarkerAddLine}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4037-L4047" target="_blank">source</a>]

```lua
Spring.MarkerAddLine(number, number, number, number, number, number, boolean?, PlayerID?) -> nil
```

**Parameters**

- `x1` `number`
- `y1` `number`
- `z1` `number`
- `x2` `number`
- `y2` `number`
- `z2` `number`
- `localOnly` `boolean?` — (Default: `false`)
- `playerId` `PlayerID?`

**Returns**

- `nil`

### Spring.MarkerErasePosition {#Spring.MarkerErasePosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4071-L4083" target="_blank">source</a>]

Issue an erase command for markers on the map.

```lua
Spring.MarkerErasePosition(number, number, number, nil, boolean?, PlayerID?, boolean?) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`
- `unused` `nil` — This argument is ignored.
- `localOnly` `boolean?` — (Default: `false`) do not issue a network message, erase only for the current player
- `playerId` `PlayerID?` — when not specified it uses the issuer playerId
- `alwaysErase` `boolean?` — (Default: `false`) erase any marker when `localOnly` and current player is spectating. Allows spectators to erase players markers locally

**Returns**

- `nil`

### Spring.SetAtmosphere {#Spring.SetAtmosphere}
*function*

Set atmosphere parameters

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4125-L4129" target="_blank">source</a>]

```lua
Spring.SetAtmosphere(AtmosphereParams) -> nil
```

**Parameters**

- `params` [`AtmosphereParams`](AtmosphereParams.md#AtmosphereParams)

### Spring.SetSunDirection {#Spring.SetSunDirection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4193-L4201" target="_blank">source</a>]

```lua
Spring.SetSunDirection(number, number, number, number?) -> nil
```

**Parameters**

- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`
- `intensity` `number?` — (Default: `1.0`)

**Returns**

- `nil`

### Spring.SetSunLighting {#Spring.SetSunLighting}
*function*

Modify sun lighting parameters.

```lua
Spring.SetSunLighting({groundAmbientColor = {1, 0.1, 1}, groundDiffuseColor = {1, 0.1, 1} })
```

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4232-L4241" target="_blank">source</a>]

```lua
Spring.SetSunLighting(SunLightingParams) -> nil
```

**Parameters**

- `params` [`SunLightingParams`](SunLightingParams.md#SunLightingParams)

### Spring.SetMapRenderingParams {#Spring.SetMapRenderingParams}
*function*

Allows to change map rendering params at runtime.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4291-L4296" target="_blank">source</a>]

```lua
Spring.SetMapRenderingParams(MapRenderingParams) -> nil
```

**Parameters**

- `params` [`MapRenderingParams`](MapRenderingParams.md#MapRenderingParams)

**Returns**

- `nil`

### Spring.ForceTesselationUpdate {#Spring.ForceTesselationUpdate}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4357-L4363" target="_blank">source</a>]

```lua
Spring.ForceTesselationUpdate(boolean?, boolean?) -> boolean
```

**Parameters**

- `normal` `boolean?` — (Default: `true`)
- `shadow` `boolean?` — (Default: `false`)

**Returns**

- `updated` `boolean`

### Spring.SendSkirmishAIMessage {#Spring.SendSkirmishAIMessage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4395-L4399" target="_blank">source</a>]

```lua
Spring.SendSkirmishAIMessage(TeamID, string) -> boolean?
```

**Parameters**

- `aiTeam` [`TeamID`](Aliases.md#TeamID)
- `message` `string`

**Returns**

- `ai_processed` `boolean?`

### Spring.SetLogSectionFilterLevel {#Spring.SetLogSectionFilterLevel}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4429-L4433" target="_blank">source</a>]

```lua
Spring.SetLogSectionFilterLevel(string, (string|number)?) -> nil
```

**Parameters**

- `sectionName` `string`
- `logLevel` `(string|number)?`

**Returns**

- `nil`

### Spring.GarbageCollectCtrl {#Spring.GarbageCollectCtrl}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4444-L4455" target="_blank">source</a>]

```lua
Spring.GarbageCollectCtrl(integer?, integer?, integer?, integer?, number?, number?, number?, number?) -> nil
```

**Parameters**

- `itersPerBatch` `integer?`
- `numStepsPerIter` `integer?`
- `minStepsPerIter` `integer?`
- `maxStepsPerIter` `integer?`
- `minLoopRunTime` `number?`
- `maxLoopRunTime` `number?`
- `baseRunTimeMult` `number?`
- `baseMemLoadMult` `number?`

**Returns**

- `nil`

### Spring.SetAutoShowMetal {#Spring.SetAutoShowMetal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4476-L4479" target="_blank">source</a>]

```lua
Spring.SetAutoShowMetal(boolean) -> nil
```

**Parameters**

- `autoShow` `boolean`

**Returns**

- `nil`

### Spring.SetDrawSky {#Spring.SetDrawSky}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4487-L4490" target="_blank">source</a>]

```lua
Spring.SetDrawSky(boolean) -> nil
```

**Parameters**

- `drawSky` `boolean`

**Returns**

- `nil`

### Spring.SetDrawWater {#Spring.SetDrawWater}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4498-L4501" target="_blank">source</a>]

```lua
Spring.SetDrawWater(boolean) -> nil
```

**Parameters**

- `drawWater` `boolean`

**Returns**

- `nil`

### Spring.SetDrawGround {#Spring.SetDrawGround}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4509-L4512" target="_blank">source</a>]

```lua
Spring.SetDrawGround(boolean) -> nil
```

**Parameters**

- `drawGround` `boolean`

**Returns**

- `nil`

### Spring.SetDrawGroundDeferred {#Spring.SetDrawGroundDeferred}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4520-L4524" target="_blank">source</a>]

```lua
Spring.SetDrawGroundDeferred(boolean, boolean?) -> nil
```

**Parameters**

- `drawGroundDeferred` `boolean`
- `drawGroundForward` `boolean?` — allows disabling of the forward pass

**Returns**

- `nil`

### Spring.SetDrawModelsDeferred {#Spring.SetDrawModelsDeferred}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4537-L4543" target="_blank">source</a>]

```lua
Spring.SetDrawModelsDeferred(boolean, boolean, boolean?, boolean?) -> nil
```

**Parameters**

- `drawUnitsDeferred` `boolean`
- `drawFeaturesDeferred` `boolean`
- `drawUnitsForward` `boolean?` — allows disabling of the respective forward passes
- `drawFeaturesForward` `boolean?` — allows disabling of the respective forward passes

**Returns**

- `nil`

### Spring.SetEngineBuildSquareRendering {#Spring.SetEngineBuildSquareRendering}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4561-L4564" target="_blank">source</a>]

```lua
Spring.SetEngineBuildSquareRendering(boolean) -> nil
```

**Parameters**

- `enabled` `boolean`

**Returns**

- `nil`

### Spring.SetVideoCapturingMode {#Spring.SetVideoCapturingMode}
*function*

This doesn't actually record the game in any way, it just regulates the framerate and interpolations.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4572-L4577" target="_blank">source</a>]

```lua
Spring.SetVideoCapturingMode(boolean) -> nil
```

**Parameters**

- `allowCaptureMode` `boolean`

**Returns**

- `nil`

### Spring.SetVideoCapturingTimeOffset {#Spring.SetVideoCapturingTimeOffset}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4585-L4588" target="_blank">source</a>]

```lua
Spring.SetVideoCapturingTimeOffset(boolean) -> nil
```

**Parameters**

- `timeOffset` `boolean`

**Returns**

- `nil`

### Spring.SetWaterParams {#Spring.SetWaterParams}
*function*

Does not need cheating enabled.

Allows to change water params (mostly `BumpWater` ones) at runtime. You may
want to set `BumpWaterUseUniforms` in your `springrc` to 1, then you don't even
need to restart `BumpWater` via `/water 4`.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4641-L4651" target="_blank">source</a>]

```lua
Spring.SetWaterParams(WaterParams) -> nil
```

**Parameters**

- `waterParams` [`WaterParams`](WaterParams.md#WaterParams)

**Returns**

- `nil`

### Spring.PreloadUnitDefModel {#Spring.PreloadUnitDefModel}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4862-L4869" target="_blank">source</a>]

Allow the engine to load the unit's model (and texture) in a background thread.
Wreckages and buildOptions of a unit are automatically preloaded.

```lua
Spring.PreloadUnitDefModel(UnitDefID) -> nil
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)

**Returns**

- `nil`

### Spring.PreloadFeatureDefModel {#Spring.PreloadFeatureDefModel}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4881-L4885" target="_blank">source</a>]

```lua
Spring.PreloadFeatureDefModel(FeatureDefID) -> nil
```

**Parameters**

- `featureDefID` [`FeatureDefID`](Aliases.md#FeatureDefID)

**Returns**

- `nil`

### Spring.PreloadSoundItem {#Spring.PreloadSoundItem}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4897-L4901" target="_blank">source</a>]

```lua
Spring.PreloadSoundItem(string) -> nil
```

**Parameters**

- `name` `string`

**Returns**

- `nil`

### Spring.LoadModelTextures {#Spring.LoadModelTextures}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4913-L4917" target="_blank">source</a>]

```lua
Spring.LoadModelTextures(string?) -> boolean?
```

**Parameters**

- `modelName` `string?`

**Returns**

- `success` `boolean?`

### Spring.CreateGroundDecal {#Spring.CreateGroundDecal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4949-L4953" target="_blank">source</a>]

```lua
Spring.CreateGroundDecal() -> DecalID?
```

**Returns**

- `decalID` `DecalID?`

### Spring.DestroyGroundDecal {#Spring.DestroyGroundDecal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4965-L4970" target="_blank">source</a>]

```lua
Spring.DestroyGroundDecal(DecalID) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `delSuccess` `boolean`

### Spring.SetGroundDecalPosAndDims {#Spring.SetGroundDecalPosAndDims}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L4978-L4988" target="_blank">source</a>]

```lua
Spring.SetGroundDecalPosAndDims(DecalID, number?, number?, number?, number?, number?) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `midPosX` `number?` — (Default: currMidPosX)
- `midPosZ` `number?` — (Default: currMidPosZ)
- `sizeX` `number?` — (Default: currSizeX)
- `sizeZ` `number?` — (Default: currSizeZ)
- `projCubeHeight` `number?` — (Default: calculateProjCubeHeight)

**Returns**

- `decalSet` `boolean`

### Spring.SetGroundDecalQuadPosAndHeight {#Spring.SetGroundDecalQuadPosAndHeight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5028-L5041" target="_blank">source</a>]

Use for non-rectangular decals

```lua
Spring.SetGroundDecalQuadPosAndHeight(DecalID, xz?, xz?, xz?, xz?, number?) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `posTL` `xz?` — (Default: currPosTL)
- `posTR` `xz?` — (Default: currPosTR)
- `posBR` `xz?` — (Default: currPosBR)
- `posBL` `xz?` — (Default: currPosBL)
- `projCubeHeight` `number?` — (Default: calculateProjCubeHeight)

**Returns**

- `decalSet` `boolean`

### Spring.SetGroundDecalRotation {#Spring.SetGroundDecalRotation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5064-L5070" target="_blank">source</a>]

```lua
Spring.SetGroundDecalRotation(DecalID, number?) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `rot` `number?` — (Default: random) in radians

**Returns**

- `decalSet` `boolean`

### Spring.SetGroundDecalTexture {#Spring.SetGroundDecalTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5086-L5093" target="_blank">source</a>]

```lua
Spring.SetGroundDecalTexture(DecalID, string, boolean?) -> boolean?
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `textureName` `string` — The texture has to be on the atlas which seems to mean it's defined as an explosion, unit tracks, or building plate decal on some unit already (no arbitrary textures)
- `isMainTex` `boolean?` — (Default: `true`) If false, it sets the normals/glow map

**Returns**

- `decalSet` `boolean?`

### Spring.SetGroundDecalTextureParams {#Spring.SetGroundDecalTextureParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5102-L5109" target="_blank">source</a>]

```lua
Spring.SetGroundDecalTextureParams(DecalID, number?, number?) -> boolean?
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `texWrapDistance` `number?` — (Default: currTexWrapDistance) if non-zero sets the mode to repeat the texture along the left-right direction of the decal every texWrapFactor elmos
- `texTraveledDistance` `number?` — (Default: currTexTraveledDistance) shifts the texture repetition defined by texWrapFactor so the texture of a next line in the continuous multiline can start where the previous finished. For that it should collect all elmo lengths of the previously set multiline segments.

**Returns**

- `decalSet` `boolean?`

### Spring.SetGroundDecalAlpha {#Spring.SetGroundDecalAlpha}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5126-L5133" target="_blank">source</a>]

```lua
Spring.SetGroundDecalAlpha(DecalID, number?, number?) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `alpha` `number?` — (Default: currAlpha) Between 0 and 1
- `alphaFalloff` `number?` — (Default: currAlphaFalloff) Between 0 and 1, per second

**Returns**

- `decalSet` `boolean`

### Spring.SetGroundDecalNormal {#Spring.SetGroundDecalNormal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5149-L5159" target="_blank">source</a>]

Sets projection cube normal to orient in 3D space.
In case the normal (0,0,0) then normal is picked from the terrain

```lua
Spring.SetGroundDecalNormal(DecalID, number?, number?, number?) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `normalX` `number?` — (Default: `0`)
- `normalY` `number?` — (Default: `0`)
- `normalZ` `number?` — (Default: `0`)

**Returns**

- `decalSet` `boolean`

### Spring.SetGroundDecalTint {#Spring.SetGroundDecalTint}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5181-L5192" target="_blank">source</a>]

Sets the tint of the ground decal. Color = 2 * textureColor * tintColor
Respectively a color of (0.5, 0.5, 0.5, 0.5) is effectively no tint

```lua
Spring.SetGroundDecalTint(DecalID, number?, number?, number?, number?) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `tintColR` `number?` — (Default: curTintColR)
- `tintColG` `number?` — (Default: curTintColG)
- `tintColB` `number?` — (Default: curTintColB)
- `tintColA` `number?` — (Default: curTintColA)

**Returns**

- `decalSet` `boolean`

### Spring.SetGroundDecalMisc {#Spring.SetGroundDecalMisc}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5213-L5224" target="_blank">source</a>]

Sets varios secondary parameters of a decal

```lua
Spring.SetGroundDecalMisc(DecalID, number?, number?, number?, number?, number?) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `dotElimExp` `number?` — (Default: curValue) pow(max(dot(decalProjVector, SurfaceNormal), 0.0), dotElimExp), used to reduce decal artifacts on surfaces non-collinear with the projection vector
- `refHeight` `number?` — (Default: curValue)
- `minHeight` `number?` — (Default: curValue)
- `maxHeight` `number?` — (Default: curValue)
- `forceHeightMode` `number?` — (Default: curValue) in case forceHeightMode==1.0 ==> force relative height: midPoint.y = refHeight + clamp(midPoint.y - refHeight, minHeight); forceHeightMode==2.0 ==> force absolute height: midPoint.y = midPoint.y, clamp(midPoint.y, minHeight, maxHeight); other forceHeightMode values do not enforce the height of the center position

**Returns**

- `decalSet` `boolean`

### Spring.SetGroundDecalCreationFrame {#Spring.SetGroundDecalCreationFrame}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5243-L5253" target="_blank">source</a>]

Use separate min and max for "gradient" style decals such as tank tracks

```lua
Spring.SetGroundDecalCreationFrame(DecalID, number?, number?) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `creationFrameMin` `number?` — (Default: currCreationFrameMin)
- `creationFrameMax` `number?` — (Default: currCreationFrameMax)

**Returns**

- `decalSet` `boolean`

### Spring.SetGroundDecalGlowParams {#Spring.SetGroundDecalGlowParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5269-L5279" target="_blank">source</a>]

Set decal glow parameters

```lua
Spring.SetGroundDecalGlowParams(DecalID, number?, number?) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `glow` `number?` — Between 0 and 1 (Default: currGlow)
- `glowFalloff` `number?` — Between 0 and 1, per second (Default: currGlowFallOff)

**Returns**

- `decalSet` `boolean`

### Spring.SetGroundDecalUserData {#Spring.SetGroundDecalUserData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5295-L5308" target="_blank">source</a>]

Set decal user data. Useful in conjunction with custom decal shaders

```lua
Spring.SetGroundDecalUserData(DecalID, integer, number?, number?, number?, number?) -> boolean
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `udQuad` `integer` — vec4 index, must be within [0;1] for now
- `x` `number?` — Any valid Lua float number (Default: current data)
- `y` `number?` — Any valid Lua float number (Default: current data)
- `z` `number?` — Any valid Lua float number (Default: current data)
- `w` `number?` — Any valid Lua float number (Default: current data)

**Returns**

- `decalSet` `boolean`

### Spring.SDLSetTextInputRect {#Spring.SDLSetTextInputRect}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5337-L5345" target="_blank">source</a>]

```lua
Spring.SDLSetTextInputRect(integer, integer, integer, integer) -> nil
```

**Parameters**

- `x` `integer`
- `y` `integer`
- `width` `integer`
- `height` `integer`

**Returns**

- `nil`

### Spring.SDLStartTextInput {#Spring.SDLStartTextInput}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5357-L5361" target="_blank">source</a>]

```lua
Spring.SDLStartTextInput() -> nil
```

**Returns**

- `nil`

### Spring.SDLStopTextInput {#Spring.SDLStopTextInput}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5368-L5372" target="_blank">source</a>]

```lua
Spring.SDLStopTextInput() -> nil
```

**Returns**

- `nil`

### Spring.SetWindowGeometry {#Spring.SetWindowGeometry}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5385-L5396" target="_blank">source</a>]

```lua
Spring.SetWindowGeometry(integer, integer, integer, integer, integer, boolean, boolean) -> nil
```

**Parameters**

- `displayIndex` `integer`
- `winRelPosX` `integer`
- `winRelPosY` `integer`
- `winSizeX` `integer`
- `winSizeY` `integer`
- `fullScreen` `boolean`
- `borderless` `boolean`

**Returns**

- `nil`

### Spring.SetWindowMinimized {#Spring.SetWindowMinimized}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5415-L5419" target="_blank">source</a>]

```lua
Spring.SetWindowMinimized() -> boolean
```

**Returns**

- `minimized` `boolean`

### Spring.SetWindowMaximized {#Spring.SetWindowMaximized}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5426-L5430" target="_blank">source</a>]

```lua
Spring.SetWindowMaximized() -> boolean
```

**Returns**

- `maximized` `boolean`

### Spring.Reload {#Spring.Reload}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5444-L5447" target="_blank">source</a>]

```lua
Spring.Reload(string) -> nil
```

**Parameters**

- `startScript` `string` — the CONTENT of the script.txt spring should use to start.

**Returns**

- `nil`

### Spring.Restart {#Spring.Restart}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5454-L5461" target="_blank">source</a>]

If this call returns, something went wrong

```lua
Spring.Restart(string, string) -> nil
```

**Parameters**

- `commandline_args` `string` — commandline arguments passed to spring executable.
- `startScript` `string`

**Returns**

- `nil`

### Spring.Start {#Spring.Start}
*function*

Launches a new Spring instance without terminating the existing one.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5469-L5478" target="_blank">source</a>]

If this call returns, something went wrong

```lua
Spring.Start(string, string) -> nil
```

**Parameters**

- `commandline_args` `string` — commandline arguments passed to spring executable.
- `startScript` `string` — the CONTENT of the script.txt spring should use to start (if empty, no start-script is added, you can still point spring to your custom script.txt when you add the file-path to commandline_args.

**Returns**

- `nil`

### Spring.SetWMIcon {#Spring.SetWMIcon}
*function*

Sets the icon for the process which is seen in the OS task-bar and other places (default: spring-logo).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5490-L5502" target="_blank">source</a>]

Note: has to be 24bit or 32bit.
Note: on windows, it has to be 32x32 pixels in size (recommended for cross-platform)
Note: *.bmp images have to be in BGR format (default for m$ ones).
Note: *.ico images are not supported.

```lua
Spring.SetWMIcon(string, boolean?) -> nil
```

**Parameters**

- `iconFileName` `string`
- `autoFree` `boolean?`

**Returns**

- `nil`

### Spring.SetWMCaption {#Spring.SetWMCaption}
*function*

Set the window title for the process

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5520-L5532" target="_blank">source</a>]

```lua
Spring.SetWMCaption(string, string?) -> nil
```

**Parameters**

- `title` `string` — (Default: `"Spring <version>"`)
- `titleShort` `string?` — (Default: `"Spring <version>"`) displayed in the OS task-bar .

> [!NOTE]
> shortTitle is only ever possibly used under X11 (Linux & OS X), but not
> with QT (KDE) and never under Windows.

**Returns**

- `nil`

### Spring.ClearWatchDogTimer {#Spring.ClearWatchDogTimer}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5540-L5543" target="_blank">source</a>]

```lua
Spring.ClearWatchDogTimer(string?) -> nil
```

**Parameters**

- `threadName` `string?` — (Default: main)

**Returns**

- `nil`

### Spring.SetClipboard {#Spring.SetClipboard}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5561-L5564" target="_blank">source</a>]

```lua
Spring.SetClipboard(string) -> nil
```

**Parameters**

- `text` `string`

**Returns**

- `nil`

### Spring.Yield {#Spring.Yield}
*function*

Relinquish control of the game loading thread and OpenGL context back to the UI (LuaIntro).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L5572-L5586" target="_blank">source</a>]

Should be called after each widget/unsynced gadget is loaded in widget/gadget handler. Use it to draw screen updates and process windows events.

```lua
Spring.Yield() -> boolean
```

**Returns**

- `continueYielding` `boolean` — when true caller should continue calling [Spring.Yield](Spring.md#Spring.Yield) during the widgets/gadgets load, when false it shouldn't call it any longer.

### Spring.IsReplay {#Spring.IsReplay}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L485-L490" target="_blank">source</a>]

```lua
Spring.IsReplay() -> boolean
```

**Returns**

- `isReplay` `boolean`

### Spring.GetReplayLength {#Spring.GetReplayLength}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L498-L503" target="_blank">source</a>]

```lua
Spring.GetReplayLength() -> number?
```

**Returns**

- `timeInSeconds` `number?`

### Spring.GetGameName {#Spring.GetGameName}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L518-L523" target="_blank">source</a>]

```lua
Spring.GetGameName() -> string
```

**Returns**

- `name` `string`

### Spring.GetReplayFilePath {#Spring.GetReplayFilePath}
*function*

If a replay is currently being watched, returns its file path.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L530-L535" target="_blank">source</a>]

```lua
Spring.GetReplayFilePath() -> string
```

**Returns**

- `filePath` `string`

### Spring.GetReplayRecordingFilePath {#Spring.GetReplayRecordingFilePath}
*function*

If a replay is being recorded, returns its projected file path.
Note that replay contents are only written there at game exit.
Note also that watching a replay also records a meta-replay
if the DemoFromDemo springsetting is set.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L548-L556" target="_blank">source</a>]

```lua
Spring.GetReplayRecordingFilePath() -> string
```

**Returns**

- `filePath` `string`

### Spring.GetMenuName {#Spring.GetMenuName}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L582-L587" target="_blank">source</a>]

```lua
Spring.GetMenuName() -> string
```

**Returns**

- `name` `string` — name .. version from Modinfo.lua. E.g. "Spring: 1944 test-5640-ac2d15b".

### Spring.GetProfilerTimeRecord {#Spring.GetProfilerTimeRecord}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L601-L614" target="_blank">source</a>]

```lua
Spring.GetProfilerTimeRecord(string, boolean?) -> number, number, number, number, number, table<integer,number>?
```

**Parameters**

- `profilerName` `string`
- `frameData` `boolean?` — (Default: `false`)

**Returns**

- `total` `number` — in ms
- `current` `number` — in ms
- `max_dt` `number`
- `time_pct` `number`
- `peak_pct` `number`
- `frameData` `table<integer,number>?` — Table where key is the frame index and value is duration.

### Spring.GetProfilerRecordNames {#Spring.GetProfilerRecordNames}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L641-L646" target="_blank">source</a>]

```lua
Spring.GetProfilerRecordNames() -> string[]
```

**Returns**

- `profilerNames` `string[]`

### Spring.GetLuaMemUsage {#Spring.GetLuaMemUsage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L663-L675" target="_blank">source</a>]

```lua
Spring.GetLuaMemUsage() -> number, number, number, number, number, number, number, number
```

**Returns**

- `luaHandleAllocedMem` `number` — in kilobytes
- `luaHandleNumAllocs` `number` — divided by 1000
- `luaGlobalAllocedMem` `number` — in kilobytes
- `luaGlobalNumAllocs` `number` — divided by 1000
- `luaUnsyncedGlobalAllocedMem` `number` — in kilobytes
- `luaUnsyncedGlobalNumAllocs` `number` — divided by 1000
- `luaSyncedGlobalAllocedMem` `number` — in kilobytes
- `luaSyncedGlobalNumAllocs` `number` — divided by 1000

### Spring.GetVidMemUsage {#Spring.GetVidMemUsage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L714-L720" target="_blank">source</a>]

```lua
Spring.GetVidMemUsage() -> number, number
```

**Returns**

- `usedMem` `number` — in MB
- `availableMem` `number` — in MB

### Spring.GetTimer {#Spring.GetTimer}
*function*

Get a timer with millisecond resolution

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L768-L772" target="_blank">source</a>]

```lua
Spring.GetTimer() -> integer
```

**Returns**

- `integer`

### Spring.GetTimerMicros {#Spring.GetTimerMicros}
*function*

Get a timer with microsecond resolution

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L780-L784" target="_blank">source</a>]

```lua
Spring.GetTimerMicros() -> integer
```

**Returns**

- `integer`

### Spring.GetFrameTimer {#Spring.GetFrameTimer}
*function*

Get a timer for the start of the frame

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L792-L800" target="_blank">source</a>]

This should give better results for camera interpolations

```lua
Spring.GetFrameTimer(boolean?) -> integer
```

**Parameters**

- `lastFrameTime` `boolean?` — (Default: `false`) whether to use last frame time instead of last frame start

**Returns**

- `integer`

### Spring.DiffTimers {#Spring.DiffTimers}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L812-L820" target="_blank">source</a>]

```lua
Spring.DiffTimers(integer, integer, boolean?, boolean?) -> number
```

**Parameters**

- `endTimer` `integer`
- `startTimer` `integer`
- `returnMs` `boolean?` — (Default: `false`) whether to return `timeAmount` in milliseconds as opposed to seconds
- `fromMicroSecs` `boolean?` — (Default: `false`) whether timers are in microseconds instead of milliseconds

**Returns**

- `timeAmount` `number`

### Spring.GetNumDisplays {#Spring.GetNumDisplays}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L870-L875" target="_blank">source</a>]

```lua
Spring.GetNumDisplays() -> integer
```

**Returns**

- `numDisplays` `integer` — as returned by `SDL_GetNumVideoDisplays`

### Spring.GetViewGeometry {#Spring.GetViewGeometry}
*function*

Get main view geometry (map and game rendering)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L883-L891" target="_blank">source</a>]

```lua
Spring.GetViewGeometry() -> integer, integer, integer, integer
```

**Returns**

- `viewSizeX` `integer` — in px
- `viewSizeY` `integer` — in px
- `viewPosX` `integer` — offset from leftmost screen left border in px
- `viewPosY` `integer` — offset from bottommost screen bottom border in px

### Spring.GetDualViewGeometry {#Spring.GetDualViewGeometry}
*function*

Get dual view geometry (minimap when enabled)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L902-L910" target="_blank">source</a>]

```lua
Spring.GetDualViewGeometry() -> integer, integer, integer, integer
```

**Returns**

- `dualViewSizeX` `integer` — in px
- `dualViewSizeY` `integer` — in px
- `dualViewPosX` `integer` — offset from leftmost screen left border in px
- `dualViewPosY` `integer` — offset from bottommost screen bottom border in px

### Spring.GetWindowGeometry {#Spring.GetWindowGeometry}
*function*

Get main window geometry

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L921-L933" target="_blank">source</a>]

```lua
Spring.GetWindowGeometry() -> integer, integer, integer, integer, integer, integer, integer, integer
```

**Returns**

- `winSizeX` `integer` — in px
- `winSizeY` `integer` — in px
- `winPosX` `integer` — in px
- `winPosY` `integer` — in px
- `windowBorderTop` `integer` — in px
- `windowBorderLeft` `integer` — in px
- `windowBorderBottom` `integer` — in px
- `windowBorderRight` `integer` — in px

### Spring.GetWindowDisplayMode {#Spring.GetWindowDisplayMode}
*function*

Get main window display mode

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L951-L958" target="_blank">source</a>]

```lua
Spring.GetWindowDisplayMode() -> integer, integer, integer, integer
```

**Returns**

- `width` `integer` — in px
- `height` `integer` — in px
- `bits` `integer` — per pixel
- `refresh` `integer` — rate in Hz

### Spring.GetScreenGeometry {#Spring.GetScreenGeometry}
*function*

Get screen geometry

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L974-L993" target="_blank">source</a>]

```lua
Spring.GetScreenGeometry(integer?, boolean?) -> integer, integer, integer, integer, integer, integer, integer, integer, integer?, integer?, integer?, integer?
```

**Parameters**

- `displayIndex` `integer?` — (Default: `-1`)
- `queryUsable` `boolean?` — (Default: `false`)

**Returns**

- `screenSizeX` `integer` — in px
- `screenSizeY` `integer` — in px
- `screenPosX` `integer` — in px
- `screenPosY` `integer` — in px
- `windowBorderTop` `integer` — in px
- `windowBorderLeft` `integer` — in px
- `windowBorderBottom` `integer` — in px
- `windowBorderRight` `integer` — in px
- `screenUsableSizeX` `integer?` — in px
- `screenUsableSizeY` `integer?` — in px
- `screenUsablePosX` `integer?` — in px
- `screenUsablePosY` `integer?` — in px

### Spring.GetMiniMapGeometry {#Spring.GetMiniMapGeometry}
*function*

Get minimap geometry

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1031-L1041" target="_blank">source</a>]

```lua
Spring.GetMiniMapGeometry() -> integer, integer, integer, integer, boolean, boolean
```

**Returns**

- `minimapPosX` `integer` — in px
- `minimapPosY` `integer` — in px
- `minimapSizeX` `integer` — in px
- `minimapSizeY` `integer` — in px
- `minimized` `boolean`
- `maximized` `boolean`

### Spring.GetMiniMapRotation {#Spring.GetMiniMapRotation}
*function*

Get minimap rotation

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1058-L1062" target="_blank">source</a>]

```lua
Spring.GetMiniMapRotation() -> number
```

**Returns**

- `rotation` `number` — in radians

### Spring.GetMiniMapDualScreen {#Spring.GetMiniMapDualScreen}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1074-L1077" target="_blank">source</a>]

```lua
Spring.GetMiniMapDualScreen() -> ("left"|"right"|false)
```

**Returns**

- `position` `("left"|"right"|false)` — `"left"` or `"right"` when dual screen is enabled, otherwise `false`.

### Spring.GetSelectionBox {#Spring.GetSelectionBox}
*function*

Get vertices from currently active selection box

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1096-L1108" target="_blank">source</a>]

Returns nil when selection box is inactive

**See:** [Spring.GetUnitsInScreenRectangle](Spring.md#Spring.GetUnitsInScreenRectangle)

```lua
Spring.GetSelectionBox() -> number?, number?, number?, number?
```

**Returns**

- `left` `number?`
- `top` `number?`
- `right` `number?`
- `bottom` `number?`

### Spring.GetDrawSelectionInfo {#Spring.GetDrawSelectionInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1130-L1134" target="_blank">source</a>]

```lua
Spring.GetDrawSelectionInfo() -> boolean
```

**Returns**

- `boolean`

### Spring.IsAboveMiniMap {#Spring.IsAboveMiniMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1142-L1150" target="_blank">source</a>]

```lua
Spring.IsAboveMiniMap(integer, integer) -> boolean
```

**Parameters**

- `x` `integer`
- `y` `integer`

**Returns**

- `isAbove` `boolean`

### Spring.GetDrawFrame {#Spring.GetDrawFrame}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1174-L1180" target="_blank">source</a>]

```lua
Spring.GetDrawFrame() -> integer, integer
```

**Returns**

- `low_16bit` `integer`
- `high_16bit` `integer`

### Spring.GetFrameTimeOffset {#Spring.GetFrameTimeOffset}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1189-L1200" target="_blank">source</a>]

Ideally, when running 30hz sim, and 60hz rendering, the draw frames should
have and offset of either 0.0 frames, or 0.5 frames.

When draw frames are not integer multiples of sim frames, some interpolation
happens, and this timeoffset shows how far along it is.

```lua
Spring.GetFrameTimeOffset() -> number?
```

**Returns**

- `offset` `number?` — of the current draw frame from the last sim frame, expressed in fractions of a frame

### Spring.GetGameSecondsInterpolated {#Spring.GetGameSecondsInterpolated}
*function*

Gets game time for drawing purposes

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1207-L1214" target="_blank">source</a>]

Returns the game time, taking the interpolated draw frame into account.

```lua
Spring.GetGameSecondsInterpolated() -> number
```

**Returns**

- `time` `number` — in seconds

### Spring.GetLastUpdateSeconds {#Spring.GetLastUpdateSeconds}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1221-L1226" target="_blank">source</a>]

```lua
Spring.GetLastUpdateSeconds() -> number?
```

**Returns**

- `lastUpdateSeconds` `number?`

### Spring.GetVideoCapturingMode {#Spring.GetVideoCapturingMode}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1234-L1239" target="_blank">source</a>]

```lua
Spring.GetVideoCapturingMode() -> boolean
```

**Returns**

- `allowRecord` `boolean`

### Spring.GetPrevFrameSyncChecksum {#Spring.GetPrevFrameSyncChecksum}
*function*

Returns the engine's sync checksum for the previous simframe,
useful for testing. The returned string is NOT convertible to
a number within Lua.

Returns a dummy value if [Platform.hasSyncChecksums](Platform.md#Platform.hasSyncChecksums) is false,
or if no frames were processed yet.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1247-L1259" target="_blank">source</a>]

```lua
Spring.GetPrevFrameSyncChecksum() -> string
```

**Returns**

- `checksum` `string`

### Spring.IsUnitAllied {#Spring.IsUnitAllied}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1282-L1287" target="_blank">source</a>]

```lua
Spring.IsUnitAllied(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `isAllied` `boolean?` — nil with unitID cannot be parsed

### Spring.IsUnitSelected {#Spring.IsUnitSelected}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1306-L1311" target="_blank">source</a>]

```lua
Spring.IsUnitSelected(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `isSelected` `boolean?` — nil when unitID cannot be parsed

### Spring.GetUnitLuaDraw {#Spring.GetUnitLuaDraw}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1324-L1329" target="_blank">source</a>]

```lua
Spring.GetUnitLuaDraw(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `draw` `boolean?` — nil when unitID cannot be parsed

### Spring.GetUnitNoDraw {#Spring.GetUnitNoDraw}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1335-L1340" target="_blank">source</a>]

```lua
Spring.GetUnitNoDraw(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `noDraw` `boolean?` — `nil` when unitID cannot be parsed

### Spring.GetUnitEngineDrawMask {#Spring.GetUnitEngineDrawMask}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1346-L1351" target="_blank">source</a>]

```lua
Spring.GetUnitEngineDrawMask(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `drawMask` `boolean?` — `nil` when unitID cannot be parsed

### Spring.GetUnitAlwaysUpdateMatrix {#Spring.GetUnitAlwaysUpdateMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1357-L1362" target="_blank">source</a>]

```lua
Spring.GetUnitAlwaysUpdateMatrix(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `alwaysUpdateMatrix` `boolean?` — `nil` when unitID cannot be parsed

### Spring.GetUnitDrawFlag {#Spring.GetUnitDrawFlag}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1374-L1379" target="_blank">source</a>]

```lua
Spring.GetUnitDrawFlag(UnitID) -> number?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `drawFlag` `number?` — `nil` when unitID cannot be parsed

### Spring.GetUnitNoMinimap {#Spring.GetUnitNoMinimap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1391-L1396" target="_blank">source</a>]

```lua
Spring.GetUnitNoMinimap(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `noMinimap` `boolean?` — `nil` when unitID cannot be parsed

### Spring.GetUnitNoGroup {#Spring.GetUnitNoGroup}
*function*

Check if a unit is not allowed to be added to a group by a player.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1408-L1414" target="_blank">source</a>]

```lua
Spring.GetUnitNoGroup(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `noGroup` `boolean?` — `true` if the unit is not allowed to be added to a group, `false` if it is allowed to be added to a group, or `nil` when `unitID` is not valid.

### Spring.GetUnitNoSelect {#Spring.GetUnitNoSelect}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1426-L1431" target="_blank">source</a>]

```lua
Spring.GetUnitNoSelect(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `noSelect` `boolean?` — `nil` when `unitID` cannot be parsed.

### Spring.UnitIconGetDraw {#Spring.UnitIconGetDraw}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1444-L1450" target="_blank">source</a>]

```lua
Spring.UnitIconGetDraw(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `drawIcon` `boolean?`

### Spring.GetUnitIconData {#Spring.GetUnitIconData}
*function*

Get unit icon data

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1537-L1544" target="_blank">source</a>]

**See:** [Spring.GetIconData](Spring.md#Spring.GetIconData)

```lua
Spring.GetUnitIconData(UnitID, boolean?) -> IconData?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `fullData` `boolean?` — (Default: false) Whether additional information about the icon is returned, otherwise only `name` and `atlasTexCoords` are returned

**Returns**

- `IconData?` — `nil` if unit is not found or unit currentIconIndex is invalid

### Spring.GetUnitIcon {#Spring.GetUnitIcon}
*function*

Get unit icon name

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1559-L1564" target="_blank">source</a>]

```lua
Spring.GetUnitIcon(UnitID) -> string
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `iconName` `string`

### Spring.GetIconData {#Spring.GetIconData}
*function*

Get icon data

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1581-L1588" target="_blank">source</a>]

**See:** [Spring.GetUnitIconData](Spring.md#Spring.GetUnitIconData)

```lua
Spring.GetIconData(string, boolean?) -> IconData?
```

**Parameters**

- `iconName` `string`
- `fullData` `boolean?` — (Default: false) Whether additional information about the icon is returned, otherwise only `name` and `atlasTexCoords` are returned

**Returns**

- `IconData?` — `nil` if iconName lookup fails

### Spring.GetAllIconDataArray {#Spring.GetAllIconDataArray}
*function*

Get icon data

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1602-L1609" target="_blank">source</a>]

**See:** [Spring.GetIconData](Spring.md#Spring.GetIconData)

```lua
Spring.GetAllIconDataArray(boolean?) -> IconData[]
```

**Parameters**

- `fullData` `boolean?` — (Default: false) Whether additional information about each icon is returned, otherwise only `name` and `atlasTexCoords` are returned

**Returns**

- `iconDataList` `IconData[]`

### Spring.GetUnitSelectionVolumeData {#Spring.GetUnitSelectionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1630-L1644" target="_blank">source</a>]

```lua
Spring.GetUnitSelectionVolumeData(UnitID) -> number?, number, number, number, number, number, integer, integer, integer, boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `scaleX` `number?` — nil when unitID cannot be parsed
- `scaleY` `number`
- `scaleZ` `number`
- `offsetX` `number`
- `offsetY` `number`
- `offsetZ` `number`
- `volumeType` `integer`
- `useContHitTest` `integer`
- `getPrimaryAxis` `integer`
- `ignoreHits` `boolean`

### Spring.GetFeatureLuaDraw {#Spring.GetFeatureLuaDraw}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1657-L1662" target="_blank">source</a>]

```lua
Spring.GetFeatureLuaDraw(FeatureID) -> boolean?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `luaDraw` `boolean?` — `nil` when featureID cannot be parsed

### Spring.GetFeatureNoDraw {#Spring.GetFeatureNoDraw}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1668-L1673" target="_blank">source</a>]

```lua
Spring.GetFeatureNoDraw(FeatureID) -> boolean?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `noDraw` `boolean?` — `nil` when featureID cannot be parsed

### Spring.GetFeatureEngineDrawMask {#Spring.GetFeatureEngineDrawMask}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1679-L1684" target="_blank">source</a>]

```lua
Spring.GetFeatureEngineDrawMask(FeatureID) -> boolean?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `drawMask` `boolean?` — `nil` when featureID cannot be parsed

### Spring.GetFeatureAlwaysUpdateMatrix {#Spring.GetFeatureAlwaysUpdateMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1690-L1695" target="_blank">source</a>]

```lua
Spring.GetFeatureAlwaysUpdateMatrix(FeatureID) -> boolean?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `alwaysUpdateMatrix` `boolean?` — `nil` when featureID cannot be parsed

### Spring.GetFeatureDrawFlag {#Spring.GetFeatureDrawFlag}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1707-L1712" target="_blank">source</a>]

```lua
Spring.GetFeatureDrawFlag(FeatureID) -> number?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `drawFlag` `number?` — `nil` when featureID cannot be parsed

### Spring.GetFeatureSelectionVolumeData {#Spring.GetFeatureSelectionVolumeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1724-L1738" target="_blank">source</a>]

```lua
Spring.GetFeatureSelectionVolumeData(FeatureID) -> number?, number, number, number, number, number, integer, integer, integer, boolean
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `scaleX` `number?` — nil when featureID cannot be parsed
- `scaleY` `number`
- `scaleZ` `number`
- `offsetX` `number`
- `offsetY` `number`
- `offsetZ` `number`
- `volumeType` `integer`
- `useContHitTest` `integer`
- `getPrimaryAxis` `integer`
- `ignoreHits` `boolean`

### Spring.GetUnitTransformMatrix {#Spring.GetUnitTransformMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1773-L1778" target="_blank">source</a>]

```lua
Spring.GetUnitTransformMatrix(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `nil` — when unitID cannot be parsed

### Spring.GetUnitTransformMatrix (overload 1) {#Spring.GetUnitTransformMatrix-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1779-L1799" target="_blank">source</a>]

```lua
Spring.GetUnitTransformMatrix(UnitID) -> number, number, number, number, number, number, number, number, number, number, number, number, number, number, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `m11` `number`
- `m12` `number`
- `m13` `number`
- `m14` `number`
- `m21` `number`
- `m22` `number`
- `m23` `number`
- `m24` `number`
- `m31` `number`
- `m32` `number`
- `m33` `number`
- `m34` `number`
- `m41` `number`
- `m42` `number`
- `m43` `number`
- `m44` `number`

### Spring.GetFeatureTransformMatrix {#Spring.GetFeatureTransformMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1803-L1808" target="_blank">source</a>]

```lua
Spring.GetFeatureTransformMatrix(FeatureID) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `nil` — when featureID cannot be parsed

### Spring.GetFeatureTransformMatrix (overload 1) {#Spring.GetFeatureTransformMatrix-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1809-L1829" target="_blank">source</a>]

```lua
Spring.GetFeatureTransformMatrix(FeatureID) -> number, number, number, number, number, number, number, number, number, number, number, number, number, number, number, number
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `m11` `number`
- `m12` `number`
- `m13` `number`
- `m14` `number`
- `m21` `number`
- `m22` `number`
- `m23` `number`
- `m24` `number`
- `m31` `number`
- `m32` `number`
- `m33` `number`
- `m34` `number`
- `m41` `number`
- `m42` `number`
- `m43` `number`
- `m44` `number`

### Spring.IsUnitInView {#Spring.IsUnitInView}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1839-L1844" target="_blank">source</a>]

```lua
Spring.IsUnitInView(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `inView` `boolean?` — nil when unitID cannot be parsed

### Spring.IsUnitVisible {#Spring.IsUnitVisible}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1857-L1864" target="_blank">source</a>]

```lua
Spring.IsUnitVisible(UnitID, number?, boolean) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `radius` `number?` — unitRadius when not specified
- `checkIcon` `boolean`

**Returns**

- `isVisible` `boolean?` — nil when unitID cannot be parsed

### Spring.IsUnitIcon {#Spring.IsUnitIcon}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1899-L1904" target="_blank">source</a>]

```lua
Spring.IsUnitIcon(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `isUnitIcon` `boolean?` — nil when unitID cannot be parsed

### Spring.IsAABBInView {#Spring.IsAABBInView}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1917-L1927" target="_blank">source</a>]

```lua
Spring.IsAABBInView(number, number, number, number, number, number) -> boolean
```

**Parameters**

- `minX` `number`
- `minY` `number`
- `minZ` `number`
- `maxX` `number`
- `maxY` `number`
- `maxZ` `number`

**Returns**

- `inView` `boolean`

### Spring.IsSphereInView {#Spring.IsSphereInView}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1946-L1954" target="_blank">source</a>]

```lua
Spring.IsSphereInView(number, number, number, number?) -> boolean
```

**Parameters**

- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `radius` `number?` — (Default: `0`)

**Returns**

- `inView` `boolean`

### Spring.GetUnitViewPosition {#Spring.GetUnitViewPosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1967-L1975" target="_blank">source</a>]

```lua
Spring.GetUnitViewPosition(UnitID, boolean?) -> number?, number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `midPos` `boolean?` — (Default: `false`)

**Returns**

- `x` `number?` — nil when unitID cannot be parsed
- `y` `number`
- `z` `number`

### Spring.GetVisibleUnits {#Spring.GetVisibleUnits}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2062-L2069" target="_blank">source</a>]

```lua
Spring.GetVisibleUnits(TeamID?, number?, boolean?) -> UnitID[]?
```

**Parameters**

- `teamID` `TeamID?` — (Default: `-1`)
- `radius` `number?` — (Default: `30`)
- `icons` `boolean?` — (Default: `true`)

**Returns**

- `unitIDs` `UnitID[]?`

### Spring.GetVisibleFeatures {#Spring.GetVisibleFeatures}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2160-L2168" target="_blank">source</a>]

```lua
Spring.GetVisibleFeatures(TeamID?, number?, boolean?, boolean?) -> FeatureID[]?
```

**Parameters**

- `teamID` `TeamID?` — (Default: `-1`)
- `radius` `number?` — (Default: `30`)
- `icons` `boolean?` — (Default: `true`)
- `geos` `boolean?` — (Default: `true`)

**Returns**

- `featureIDs` `FeatureID[]?`

### Spring.GetVisibleProjectiles {#Spring.GetVisibleProjectiles}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2241-L2249" target="_blank">source</a>]

```lua
Spring.GetVisibleProjectiles(AllyTeamID?, boolean?, boolean?, boolean?) -> ProjectileID[]?
```

**Parameters**

- `allyTeamID` `AllyTeamID?` — (Default: `-1`)
- `addSyncedProjectiles` `boolean?` — (Default: `true`)
- `addWeaponProjectiles` `boolean?` — (Default: `true`)
- `addPieceProjectiles` `boolean?` — (Default: `true`)

**Returns**

- `projectileIDs` `ProjectileID[]?`

### Spring.GetRenderUnits {#Spring.GetRenderUnits}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2415-L2422" target="_blank">source</a>]

```lua
Spring.GetRenderUnits(DrawMask, true) -> UnitID[], DrawFlag[]
```

**Parameters**

- `drawMask` [`DrawMask`](Aliases.md#DrawMask) — (Default: `0`) Filter objects by their draw flags.
- `sendMask` `true` — Whether to send objects draw flags as second return

**Returns**

- `unitIDs` `UnitID[]`
- `drawFlags` `DrawFlag[]`

### Spring.GetRenderUnits (overload 1) {#Spring.GetRenderUnits-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2424-L2430" target="_blank">source</a>]

```lua
Spring.GetRenderUnits(DrawMask, false?) -> UnitID[]
```

**Parameters**

- `drawMask` [`DrawMask`](Aliases.md#DrawMask) — (Default: `0`) Filter objects by their draw flags.
- `sendMask` `false?` — Whether to send objects draw flags as second return

**Returns**

- `unitIDs` `UnitID[]`

### Spring.GetRenderUnitsDrawFlagChanged {#Spring.GetRenderUnitsDrawFlagChanged}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2436-L2442" target="_blank">source</a>]

Gets a list of IDs of units that have had their draw flags changed, and the corresponding flags.

```lua
Spring.GetRenderUnitsDrawFlagChanged(true) -> UnitID[], DrawFlag[]
```

**Parameters**

- `sendMask` `true` — Whether to send objects draw flags as second return.

**Returns**

- `ids` `UnitID[]`
- `unitDrawFlags` `DrawFlag[]`

### Spring.GetRenderUnitsDrawFlagChanged (overload 1) {#Spring.GetRenderUnitsDrawFlagChanged-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2444-L2449" target="_blank">source</a>]

Gets a list of IDs of units that have had their draw flags changed, and the corresponding flags.

```lua
Spring.GetRenderUnitsDrawFlagChanged(false?) -> UnitID[]
```

**Parameters**

- `sendMask` `false?` — Whether to send objects draw flags as second return.

**Returns**

- `ids` `UnitID[]`

### Spring.GetRenderFeatures {#Spring.GetRenderFeatures}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2455-L2462" target="_blank">source</a>]

```lua
Spring.GetRenderFeatures(DrawMask, true) -> FeatureID[], DrawFlag[]
```

**Parameters**

- `drawMask` [`DrawMask`](Aliases.md#DrawMask) — (Default: `0`) Filter objects by their draw flags.
- `sendMask` `true` — Whether to send objects draw flags as second return

**Returns**

- `featureIDs` `FeatureID[]`
- `drawFlags` `DrawFlag[]`

### Spring.GetRenderFeatures (overload 1) {#Spring.GetRenderFeatures-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2464-L2470" target="_blank">source</a>]

```lua
Spring.GetRenderFeatures(DrawMask, false?) -> FeatureID[]
```

**Parameters**

- `drawMask` [`DrawMask`](Aliases.md#DrawMask) — (Default: `0`) Filter objects by their draw flags.
- `sendMask` `false?` — Whether to send objects draw flags as second return

**Returns**

- `featureIDs` `FeatureID[]`

### Spring.GetRenderFeaturesDrawFlagChanged {#Spring.GetRenderFeaturesDrawFlagChanged}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2476-L2482" target="_blank">source</a>]

Gets a list of IDs of features that have had their draw flags changed, and the corresponding flags.

```lua
Spring.GetRenderFeaturesDrawFlagChanged(true) -> FeatureID[], DrawFlag[]
```

**Parameters**

- `sendMask` `true` — Whether to send objects draw flags as second return.

**Returns**

- `ids` `FeatureID[]`
- `featureDrawFlags` `DrawFlag[]`

### Spring.GetRenderFeaturesDrawFlagChanged (overload 1) {#Spring.GetRenderFeaturesDrawFlagChanged-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2484-L2489" target="_blank">source</a>]

Gets a list of IDs of features that have had their draw flags changed, and the corresponding flags.

```lua
Spring.GetRenderFeaturesDrawFlagChanged(false?) -> FeatureID[]
```

**Parameters**

- `sendMask` `false?` — Whether to send objects draw flags as second return.

**Returns**

- `ids` `FeatureID[]`

### Spring.ClearUnitsPreviousDrawFlag {#Spring.ClearUnitsPreviousDrawFlag}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2495-L2498" target="_blank">source</a>]

```lua
Spring.ClearUnitsPreviousDrawFlag() -> nil
```

### Spring.ClearFeaturesPreviousDrawFlag {#Spring.ClearFeaturesPreviousDrawFlag}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2505-L2508" target="_blank">source</a>]

```lua
Spring.ClearFeaturesPreviousDrawFlag() -> nil
```

### Spring.GetUnitsInScreenRectangle {#Spring.GetUnitsInScreenRectangle}
*function*

Get units inside a rectangle area on the map

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2515-L2524" target="_blank">source</a>]

```lua
Spring.GetUnitsInScreenRectangle(number, number, number, number, integer?) -> UnitID[]?
```

**Parameters**

- `left` `number`
- `top` `number`
- `right` `number`
- `bottom` `number`
- `allegiance` `integer?` — (Default: `-1`) teamID when > 0, when < 0 one of AllUnits = -1, MyUnits = -2, AllyUnits = -3, EnemyUnits = -4

**Returns**

- `unitIDs` `UnitID[]?`

### Spring.GetFeaturesInScreenRectangle {#Spring.GetFeaturesInScreenRectangle}
*function*

Get features inside a rectangle area on the map

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2600-L2608" target="_blank">source</a>]

```lua
Spring.GetFeaturesInScreenRectangle(number, number, number, number) -> FeatureID[]?
```

**Parameters**

- `left` `number`
- `top` `number`
- `right` `number`
- `bottom` `number`

**Returns**

- `featureIDs` `FeatureID[]?`

### Spring.GetLocalPlayerID {#Spring.GetLocalPlayerID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2656-L2661" target="_blank">source</a>]

```lua
Spring.GetLocalPlayerID() -> PlayerID
```

**Returns**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)

### Spring.GetMyPlayerID {#Spring.GetMyPlayerID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2656-L2661" target="_blank">source</a>]

Alias of GetLocalPlayerID

```lua
Spring.GetMyPlayerID() -> PlayerID
```

**Returns**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)

### Spring.GetLocalTeamID {#Spring.GetLocalTeamID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2669-L2674" target="_blank">source</a>]

```lua
Spring.GetLocalTeamID() -> TeamID
```

**Returns**

- `teamID` [`TeamID`](Aliases.md#TeamID)

### Spring.GetMyTeamID {#Spring.GetMyTeamID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2669-L2674" target="_blank">source</a>]

Alias of GetLocalTeamID

```lua
Spring.GetMyTeamID() -> TeamID
```

**Returns**

- `teamID` [`TeamID`](Aliases.md#TeamID)

### Spring.GetLocalAllyTeamID {#Spring.GetLocalAllyTeamID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2682-L2687" target="_blank">source</a>]

```lua
Spring.GetLocalAllyTeamID() -> AllyTeamID
```

**Returns**

- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)

### Spring.GetMyAllyTeamID {#Spring.GetMyAllyTeamID}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2682-L2687" target="_blank">source</a>]

Alias of GetLocalAllyTeamID

```lua
Spring.GetMyAllyTeamID() -> AllyTeamID
```

**Returns**

- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)

### Spring.GetSpectatingState {#Spring.GetSpectatingState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2695-L2701" target="_blank">source</a>]

```lua
Spring.GetSpectatingState() -> boolean, boolean, boolean
```

**Returns**

- `spectating` `boolean`
- `spectatingFullView` `boolean`
- `spectatingFullSelect` `boolean`

### Spring.GetSelectedUnits {#Spring.GetSelectedUnits}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2714-L2718" target="_blank">source</a>]

```lua
Spring.GetSelectedUnits() -> UnitID[]
```

**Returns**

- `unitIDs` `UnitID[]`

### Spring.GetSelectedUnitsSorted {#Spring.GetSelectedUnitsSorted}
*function*

Get selected units aggregated by unitDefID

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2725-L2730" target="_blank">source</a>]

```lua
Spring.GetSelectedUnitsSorted() -> table<UnitDefID,UnitID[]>, integer
```

**Returns**

- `unitsIDs` `table<UnitDefID,UnitID[]>`
- `countDefs` `integer` — the number of unitDefIDs

### Spring.GetSelectedUnitsCounts {#Spring.GetSelectedUnitsCounts}
*function*

Get an aggregate count of selected units per unitDefID

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2740-L2746" target="_blank">source</a>]

```lua
Spring.GetSelectedUnitsCounts() -> table<UnitDefID,integer>, integer
```

**Returns**

- `unitsCounts` `table<UnitDefID,integer>`
- `countDefs` `integer` — the number of unitDefIDs

### Spring.GetSelectedUnitsCount {#Spring.GetSelectedUnitsCount}
*function*

Returns the amount of selected units

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2756-L2760" target="_blank">source</a>]

```lua
Spring.GetSelectedUnitsCount() -> integer
```

**Returns**

- `selectedUnitsCount` `integer`

### Spring.GetBoxSelectionByEngine {#Spring.GetBoxSelectionByEngine}
*function*

Get if selection box is handled by engine.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2767-L2775" target="_blank">source</a>]

**See:** [Spring.SetBoxSelectionByEngine](Spring.md#Spring.SetBoxSelectionByEngine)

```lua
Spring.GetBoxSelectionByEngine() -> boolean
```

**Returns**

- `isHandledByEngine` `boolean` — `true` if the engine will select units inside selection box on release, otherwise `false`.

### Spring.IsGUIHidden {#Spring.IsGUIHidden}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2786-L2790" target="_blank">source</a>]

```lua
Spring.IsGUIHidden() -> boolean
```

**Returns**

- `boolean`

### Spring.HaveShadows {#Spring.HaveShadows}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2798-L2802" target="_blank">source</a>]

```lua
Spring.HaveShadows() -> boolean
```

**Returns**

- `shadowsLoaded` `boolean`

### Spring.HaveAdvShading {#Spring.HaveAdvShading}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2810-L2815" target="_blank">source</a>]

```lua
Spring.HaveAdvShading() -> boolean, boolean
```

**Returns**

- `useAdvShading` `boolean`
- `groundUseAdvShading` `boolean`

### Spring.GetWaterMode {#Spring.GetWaterMode}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2824-L2830" target="_blank">source</a>]

**See:** rts/Rendering/Env/IWater.h

```lua
Spring.GetWaterMode() -> integer, string
```

**Returns**

- `waterRendererID` `integer`
- `waterRendererName` `string`

### Spring.GetMapDrawMode {#Spring.GetMapDrawMode}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2840-L2844" target="_blank">source</a>]

```lua
Spring.GetMapDrawMode() -> ("normal"|"height"|"metal"|"pathTraversability"|"los")
```

**Returns**

- `("normal"|"height"|"metal"|"pathTraversability"|"los")`

### Spring.GetMapSquareTexture {#Spring.GetMapSquareTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2869-L2878" target="_blank">source</a>]

```lua
Spring.GetMapSquareTexture(integer, integer, integer, string, integer?) -> boolean?
```

**Parameters**

- `texSquareX` `integer`
- `texSquareY` `integer`
- `lodMin` `integer`
- `luaTexName` `string`
- `lodMax` `integer?` — (Default: lodMin)

**Returns**

- `success` `boolean?`

### Spring.GetLosViewColors {#Spring.GetLosViewColors}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2926-L2933" target="_blank">source</a>]

```lua
Spring.GetLosViewColors() -> rgb, rgb, rgb, rgb, rgb
```

**Returns**

- `always` [`rgb`](rgb.md#rgb)
- `LOS` [`rgb`](rgb.md#rgb)
- `radar` [`rgb`](rgb.md#rgb)
- `jam` [`rgb`](rgb.md#rgb)
- `radar2` [`rgb`](rgb.md#rgb)

### Spring.GetNanoProjectileParams {#Spring.GetNanoProjectileParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2954-L2963" target="_blank">source</a>]

```lua
Spring.GetNanoProjectileParams() -> number, number, number, number, number, number
```

**Returns**

- `rotVal` `number` — in degrees
- `rotVel` `number` — in degrees
- `rotAcc` `number` — in degrees
- `rotValRng` `number` — in degrees
- `rotVelRng` `number` — in degrees
- `rotAccRng` `number` — in degrees

### Spring.GetCameraNames {#Spring.GetCameraNames}
*function*

Get available cameras.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2978-L2983" target="_blank">source</a>]

```lua
Spring.GetCameraNames() -> table<string,integer>
```

**Returns**

- `indexByName` `table<string,integer>` — Table where where keys are names and values are indices.

### Spring.GetCameraState {#Spring.GetCameraState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2999-L3004" target="_blank">source</a>]

```lua
Spring.GetCameraState(false) -> CameraName, any ...
```

**Parameters**

- `useTable` `false`

**Returns**

- `name` [`CameraName`](Aliases.md#CameraName)
- `depends` `any ...` — on the current controller mode.

### Spring.GetCameraState (overload 1) {#Spring.GetCameraState-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3005-L3009" target="_blank">source</a>]

```lua
Spring.GetCameraState(true?) -> CameraState
```

**Parameters**

- `useTable` `true?` — (Default: `true`) Return a table instead of multiple values.

**Returns**

- `cameraState` [`CameraState`](CameraState.md#CameraState)

### Spring.GetCameraPosition {#Spring.GetCameraPosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3075-L3080" target="_blank">source</a>]

```lua
Spring.GetCameraPosition() -> number, number, number
```

**Returns**

- `posX` `number`
- `posY` `number`
- `posZ` `number`

### Spring.GetCameraDirection {#Spring.GetCameraDirection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3089-L3094" target="_blank">source</a>]

```lua
Spring.GetCameraDirection() -> number, number, number
```

**Returns**

- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`

### Spring.GetCameraRotation {#Spring.GetCameraRotation}
*function*

Get camera rotation in radians.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3103-L3109" target="_blank">source</a>]

```lua
Spring.GetCameraRotation() -> number, number, number
```

**Returns**

- `rotX` `number` — Rotation around X axis in radians.
- `rotY` `number` — Rotation around Y axis in radians.
- `rotZ` `number` — Rotation around Z axis in radians.

### Spring.GetCameraFOV {#Spring.GetCameraFOV}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3118-L3122" target="_blank">source</a>]

```lua
Spring.GetCameraFOV() -> number, number
```

**Returns**

- `vFOV` `number`
- `hFOV` `number`

### Spring.GetCameraVectors {#Spring.GetCameraVectors}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3142-L3145" target="_blank">source</a>]

```lua
Spring.GetCameraVectors() -> CameraVectors
```

**Returns**

- [`CameraVectors`](CameraVectors.md#CameraVectors)

### Spring.WorldToScreenCoords {#Spring.WorldToScreenCoords}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3169-L3178" target="_blank">source</a>]

```lua
Spring.WorldToScreenCoords(number, number, number) -> number, number, number
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`

**Returns**

- `viewPortX` `number`
- `viewPortY` `number`
- `viewPortZ` `number`

### Spring.TraceScreenRay {#Spring.TraceScreenRay}
*function*

Get information about a ray traced from screen to world position

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3192-L3215" target="_blank">source</a>]

Extended to allow a custom plane, parameters are (0, 1, 0, D=0) where D is the offset D can be specified in the third argument (if all the bools are false) or in the seventh (as shown).

Intersection coordinates are returned in t[4],t[5],t[6] when the ray goes offmap and includeSky is true), or when no unit or feature is hit (or onlyCoords is true).

This will only work for units & objects with the default collision sphere. Per Piece collision and custom collision objects are not supported.

The unit must be selectable, to appear to a screen trace ray.

```lua
Spring.TraceScreenRay(integer, integer, boolean?, boolean?, boolean?, boolean?, number?) -> string?, (UnitID|FeatureID|string|xyz)?, (FeatureID|string)?, xyz?
```

**Parameters**

- `screenX` `integer` — position on x axis in mouse coordinates (origin on left border of view)
- `screenY` `integer` — position on y axis in mouse coordinates (origin on top border of view)
- `onlyCoords` `boolean?` — (Default: `false`) return only description (1st return value) and coordinates (2nd return value)
- `useMinimap` `boolean?` — (Default: `false`) if position arguments are contained by minimap, use the minimap corresponding world position
- `includeSky` `boolean?` — (Default: `false`)
- `ignoreWater` `boolean?` — (Default: `false`)
- `heightOffset` `number?` — (Default: `0`)

**Returns**

- `description` `string?` — of traced position
- `unitID` `(UnitID|FeatureID|string|xyz)?` — or feature, position triple when onlyCoords=true
- `featureID` `(FeatureID|string)?` — or ground
- `coords` `xyz?`

### Spring.GetPixelDir {#Spring.GetPixelDir}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3318-L3326" target="_blank">source</a>]

```lua
Spring.GetPixelDir(integer, integer) -> number, number, number
```

**Parameters**

- `x` `integer`
- `y` `integer`

**Returns**

- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`

### Spring.GetTeamColor {#Spring.GetTeamColor}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3373-L3381" target="_blank">source</a>]

```lua
Spring.GetTeamColor(TeamID) -> number?, number?, number?, number?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `r` `number?` — factor from 0 to 1
- `g` `number?` — factor from 0 to 1
- `b` `number?` — factor from 0 to 1
- `a` `number?` — factor from 0 to 1

### Spring.GetTeamOrigColor {#Spring.GetTeamOrigColor}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3400-L3408" target="_blank">source</a>]

```lua
Spring.GetTeamOrigColor(TeamID) -> number?, number?, number?, number?
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `r` `number?` — factor from 0 to 1
- `g` `number?` — factor from 0 to 1
- `b` `number?` — factor from 0 to 1
- `a` `number?` — factor from 0 to 1

### Spring.GetCustomPaletteColor {#Spring.GetCustomPaletteColor}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3427-L3434" target="_blank">source</a>]

```lua
Spring.GetCustomPaletteColor(integer) -> number?, number?, number?
```

**Parameters**

- `index` `integer` — 0-based index into custom palette

**Returns**

- `r` `number?` — factor from 0 to 1
- `g` `number?` — factor from 0 to 1
- `b` `number?` — factor from 0 to 1

### Spring.GetUnitPaletteIndex {#Spring.GetUnitPaletteIndex}
*function*

Returns the custom palette index for a unit, or nil if using team color.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3447-L3452" target="_blank">source</a>]

```lua
Spring.GetUnitPaletteIndex(UnitID) -> integer?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `customIndex` `integer?` — [0..MAX_CUSTOM_COLORS) if unit uses a custom color, nil if using team color

### Spring.GetFeaturePaletteIndex {#Spring.GetFeaturePaletteIndex}
*function*

Returns the custom palette index for a feature, or nil if using team color.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3469-L3474" target="_blank">source</a>]

```lua
Spring.GetFeaturePaletteIndex(FeatureID) -> integer?
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `customIndex` `integer?` — [0..MAX_CUSTOM_COLORS) if feature uses a custom color, nil if using team color

### Spring.GetDrawSeconds {#Spring.GetDrawSeconds}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3491-L3495" target="_blank">source</a>]

```lua
Spring.GetDrawSeconds() -> integer
```

**Returns**

- `time` `integer` — Time in seconds.

### Spring.GetSoundDevices {#Spring.GetSoundDevices}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3516-L3520" target="_blank">source</a>]

```lua
Spring.GetSoundDevices() -> SoundDeviceSpec[]
```

**Returns**

- `devices` `SoundDeviceSpec[]` — Sound devices.

### Spring.GetSoundStreamTime {#Spring.GetSoundStreamTime}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3536-L3541" target="_blank">source</a>]

```lua
Spring.GetSoundStreamTime() -> number, number
```

**Returns**

- `playTime` `number`
- `time` `number`

### Spring.GetSoundEffectParams {#Spring.GetSoundEffectParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3550-L3554" target="_blank">source</a>]

```lua
Spring.GetSoundEffectParams() -> table?
```

**Returns**

- `soundEffectParams` `table?` — `nil` on headless/no-sound builds or when EFX is unsupported.

### Spring.GetFPS {#Spring.GetFPS}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3641-L3645" target="_blank">source</a>]

```lua
Spring.GetFPS() -> integer
```

**Returns**

- `fps` `integer`

### Spring.GetGameSpeed {#Spring.GetGameSpeed}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3655-L3661" target="_blank">source</a>]

```lua
Spring.GetGameSpeed() -> number, number, boolean
```

**Returns**

- `wantedSpeedFactor` `number`
- `speedFactor` `number`
- `paused` `boolean`

### Spring.GetGameState {#Spring.GetGameState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3670-L3678" target="_blank">source</a>]

```lua
Spring.GetGameState(number?) -> boolean, boolean, boolean, boolean
```

**Parameters**

- `maxLatency` `number?` — (Default: `500`) used for `isSimLagging` return parameter

**Returns**

- `doneLoading` `boolean`
- `isSavedGame` `boolean`
- `isClientPaused` `boolean`
- `isSimLagging` `boolean`

### Spring.GetActiveCommand {#Spring.GetActiveCommand}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3697-L3704" target="_blank">source</a>]

```lua
Spring.GetActiveCommand() -> integer?, integer?, integer?, string?
```

**Returns**

- `cmdIndex` `integer?`
- `cmdID` `integer?`
- `cmdType` `integer?`
- `cmdName` `string?`

### Spring.GetDefaultCommand {#Spring.GetDefaultCommand}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3726-L3733" target="_blank">source</a>]

```lua
Spring.GetDefaultCommand() -> integer?, integer?, integer?, string?
```

**Returns**

- `cmdIndex` `integer?`
- `cmdID` `integer?`
- `cmdType` `integer?`
- `cmdName` `string?`

### Spring.GetActiveCmdDescs {#Spring.GetActiveCmdDescs}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3755-L3759" target="_blank">source</a>]

```lua
Spring.GetActiveCmdDescs() -> CommandDescription[]
```

**Returns**

- `cmdDescs` `CommandDescription[]`

### Spring.GetActiveCmdDesc {#Spring.GetActiveCmdDesc}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3784-L3789" target="_blank">source</a>]

```lua
Spring.GetActiveCmdDesc(integer) -> CommandDescription?
```

**Parameters**

- `cmdIndex` `integer`

**Returns**

- `CommandDescription?`

### Spring.GetCmdDescIndex {#Spring.GetCmdDescIndex}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3808-L3813" target="_blank">source</a>]

```lua
Spring.GetCmdDescIndex(integer) -> integer?
```

**Parameters**

- `cmdID` `integer`

**Returns**

- `cmdDescIndex` `integer?`

### Spring.GetBuildFacing {#Spring.GetBuildFacing}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3847-L3851" target="_blank">source</a>]

```lua
Spring.GetBuildFacing() -> FacingInteger
```

**Returns**

- `buildFacing` [`FacingInteger`](Aliases.md#FacingInteger)

### Spring.GetBuildSpacing {#Spring.GetBuildSpacing}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3862-L3866" target="_blank">source</a>]

```lua
Spring.GetBuildSpacing() -> integer
```

**Returns**

- `buildSpacing` `integer`

### Spring.GetGatherMode {#Spring.GetGatherMode}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3877-L3881" target="_blank">source</a>]

```lua
Spring.GetGatherMode() -> integer
```

**Returns**

- `gatherMode` `integer`

### Spring.GetActivePage {#Spring.GetActivePage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3894-L3899" target="_blank">source</a>]

```lua
Spring.GetActivePage() -> integer, integer
```

**Returns**

- `activePage` `integer`
- `maxPage` `integer`

### Spring.GetMouseState {#Spring.GetMouseState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3917-L3927" target="_blank">source</a>]

```lua
Spring.GetMouseState() -> integer, integer, boolean, boolean, boolean, boolean, boolean
```

**Returns**

- `x` `integer`
- `y` `integer`
- `lmbPressed` `boolean` — left mouse button pressed
- `mmbPressed` `boolean` — middle mouse button pressed
- `rmbPressed` `boolean` — right mouse button pressed
- `offscreen` `boolean`
- `mmbScroll` `boolean`

### Spring.GetMouseCursor {#Spring.GetMouseCursor}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3945-L3950" target="_blank">source</a>]

```lua
Spring.GetMouseCursor() -> string, number
```

**Returns**

- `cursorName` `string`
- `cursorScale` `number`

### Spring.GetMouseStartPosition {#Spring.GetMouseStartPosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3961-L3973" target="_blank">source</a>]

```lua
Spring.GetMouseStartPosition(integer) -> integer, integer, number, number, number, number, number, number
```

**Parameters**

- `button` `integer`

**Returns**

- `x` `integer`
- `y` `integer`
- `camPosX` `number`
- `camPosY` `number`
- `camPosZ` `number`
- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`

### Spring.GetMouseButtonsPressed {#Spring.GetMouseButtonsPressed}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L3996-L4005" target="_blank">source</a>]

Get pressed status for specific buttons.

```lua
Spring.GetMouseButtonsPressed(integer, [integer, ]*) -> boolean ...
```

**Parameters**

- `button1` `integer` — Index of the first button.
- `...` `integer` — Indices for more buttons.

**Returns**

- `Pressed` `boolean ...` — status for the buttons.

### Spring.GetClipboard {#Spring.GetClipboard}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4035-L4039" target="_blank">source</a>]

```lua
Spring.GetClipboard() -> string
```

**Returns**

- `text` `string`

### Spring.IsUserWriting {#Spring.IsUserWriting}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4051-L4055" target="_blank">source</a>]

```lua
Spring.IsUserWriting() -> boolean
```

**Returns**

- `boolean`

### Spring.GetLastMessagePositions {#Spring.GetLastMessagePositions}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4069-L4073" target="_blank">source</a>]

```lua
Spring.GetLastMessagePositions() -> xyz[]
```

**Returns**

- `message` `xyz[]` — positions

### Spring.GetConsoleBuffer {#Spring.GetConsoleBuffer}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4092-L4096" target="_blank">source</a>]

```lua
Spring.GetConsoleBuffer(integer) -> { priority: integer, text: string }[]
```

**Parameters**

- `maxLines` `integer`

**Returns**

- `buffer` `{ priority: integer, text: string }[]`

### Spring.GetCurrentTooltip {#Spring.GetCurrentTooltip}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4128-L4131" target="_blank">source</a>]

```lua
Spring.GetCurrentTooltip() -> string
```

**Returns**

- `tooltip` `string`

### Spring.GetKeyFromScanSymbol {#Spring.GetKeyFromScanSymbol}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4145-L4149" target="_blank">source</a>]

```lua
Spring.GetKeyFromScanSymbol(string?) -> string
```

**Parameters**

- `scanSymbol` `string?`

**Returns**

- `keyName` `string`

### Spring.GetKeyState {#Spring.GetKeyState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4180-L4185" target="_blank">source</a>]

```lua
Spring.GetKeyState(integer) -> boolean
```

**Parameters**

- `keyCode` `integer`

**Returns**

- `pressed` `boolean`

### Spring.GetModKeyState {#Spring.GetModKeyState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4194-L4201" target="_blank">source</a>]

```lua
Spring.GetModKeyState() -> boolean, boolean, boolean, boolean
```

**Returns**

- `alt` `boolean`
- `ctrl` `boolean`
- `meta` `boolean`
- `shift` `boolean`

### Spring.GetPressedKeys {#Spring.GetPressedKeys}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4212-L4216" target="_blank">source</a>]

```lua
Spring.GetPressedKeys() -> table<(integer|string),true>
```

**Returns**

- `keys` `table<(integer|string),true>` — where keys are keyCodes or key names

### Spring.GetPressedScans {#Spring.GetPressedScans}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4243-L4247" target="_blank">source</a>]

```lua
Spring.GetPressedScans() -> table<(integer|string),true>
```

**Returns**

- `scans` `table<(integer|string),true>` — where keys are scanCodes or scan names

### Spring.GetInvertQueueKey {#Spring.GetInvertQueueKey}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4274-L4278" target="_blank">source</a>]

```lua
Spring.GetInvertQueueKey() -> number?
```

**Returns**

- `queueKey` `number?`

### Spring.GetKeyCode {#Spring.GetKeyCode}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4289-L4294" target="_blank">source</a>]

```lua
Spring.GetKeyCode(string) -> integer
```

**Parameters**

- `keySym` `string`

**Returns**

- `keyCode` `integer`

### Spring.GetKeySymbol {#Spring.GetKeySymbol}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4302-L4308" target="_blank">source</a>]

```lua
Spring.GetKeySymbol(integer) -> string, string
```

**Parameters**

- `keyCode` `integer`

**Returns**

- `keyCodeName` `string`
- `keyCodeDefaultName` `string` — name when there are not aliases

### Spring.GetScanSymbol {#Spring.GetScanSymbol}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4318-L4324" target="_blank">source</a>]

```lua
Spring.GetScanSymbol(integer) -> string, string
```

**Parameters**

- `scanCode` `integer`

**Returns**

- `scanCodeName` `string`
- `scanCodeDefaultName` `string` — name when there are not aliases

### Spring.GetKeyBindings {#Spring.GetKeyBindings}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4344-L4349" target="_blank">source</a>]

```lua
Spring.GetKeyBindings(string?, string?) -> KeyBinding[]
```

**Parameters**

- `keySet1` `string?` — filters keybindings bound to this keyset
- `keySet2` `string?` — OR bound to this keyset

**Returns**

- `KeyBinding[]`

### Spring.GetActionHotKeys {#Spring.GetActionHotKeys}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4397-L4402" target="_blank">source</a>]

```lua
Spring.GetActionHotKeys(string) -> string[]?
```

**Parameters**

- `actionName` `string`

**Returns**

- `hotkeys` `string[]?`

### Spring.GetGroupList {#Spring.GetGroupList}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4423-L4427" target="_blank">source</a>]

```lua
Spring.GetGroupList() -> table<GroupID,integer>?
```

**Returns**

- `groupCounts` `table<GroupID,integer>?`

### Spring.GetSelectedGroup {#Spring.GetSelectedGroup}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4451-L4455" target="_blank">source</a>]

```lua
Spring.GetSelectedGroup() -> GroupID
```

**Returns**

- `groupID` [`GroupID`](Aliases.md#GroupID)

### Spring.GetUnitGroup {#Spring.GetUnitGroup}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4463-L4468" target="_blank">source</a>]

```lua
Spring.GetUnitGroup(UnitID) -> GroupID?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `groupID` `GroupID?`

### Spring.GetGroupUnits {#Spring.GetGroupUnits}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4498-L4503" target="_blank">source</a>]

```lua
Spring.GetGroupUnits(GroupID) -> UnitID[]?
```

**Parameters**

- `groupID` [`GroupID`](Aliases.md#GroupID)

**Returns**

- `unitIDs` `UnitID[]?`

### Spring.GetGroupUnitsSorted {#Spring.GetGroupUnitsSorted}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4515-L4520" target="_blank">source</a>]

```lua
Spring.GetGroupUnitsSorted(GroupID) -> table<UnitDefID,UnitID[]>?
```

**Parameters**

- `groupID` [`GroupID`](Aliases.md#GroupID)

**Returns**

- `unitsIDs` `table<UnitDefID,UnitID[]>?`

### Spring.GetGroupUnitsCounts {#Spring.GetGroupUnitsCounts}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4532-L4537" target="_blank">source</a>]

```lua
Spring.GetGroupUnitsCounts(GroupID) -> table<UnitDefID,integer>?
```

**Parameters**

- `groupID` [`GroupID`](Aliases.md#GroupID)

**Returns**

- `unitsCounts` `table<UnitDefID,integer>?`

### Spring.GetGroupUnitsCount {#Spring.GetGroupUnitsCount}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4549-L4554" target="_blank">source</a>]

```lua
Spring.GetGroupUnitsCount(GroupID) -> integer?
```

**Parameters**

- `groupID` [`GroupID`](Aliases.md#GroupID)

**Returns**

- `groupSize` `integer?`

### Spring.GetPlayerRoster {#Spring.GetPlayerRoster}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4586-L4592" target="_blank">source</a>]

```lua
Spring.GetPlayerRoster(integer?, boolean?) -> Roster[]?
```

**Parameters**

- `sortType` `integer?` — return unsorted if unspecified. Disabled = 0, Allies = 1, TeamID = 2, PlayerName = 3, PlayerCPU = 4, PlayerPing = 5
- `showPathingPlayers` `boolean?` — (Default: `false`)

**Returns**

- `playerTable` `Roster[]?`

### Spring.GetPlayerTraffic {#Spring.GetPlayerTraffic}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4622-L4628" target="_blank">source</a>]

```lua
Spring.GetPlayerTraffic(PlayerID, integer?) -> integer
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `packetID` `integer?`

**Returns**

- `traffic` `integer`

### Spring.GetPlayerStatistics {#Spring.GetPlayerStatistics}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4674-L4683" target="_blank">source</a>]

```lua
Spring.GetPlayerStatistics(PlayerID) -> integer?, integer, integer, integer, integer
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)

**Returns**

- `mousePixels` `integer?` — nil when invalid playerID
- `mouseClicks` `integer`
- `keyPresses` `integer`
- `numCommands` `integer`
- `unitCommands` `integer`

### Spring.GetConfigParams {#Spring.GetConfigParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4729-L4733" target="_blank">source</a>]

```lua
Spring.GetConfigParams() -> Configuration[]
```

**Returns**

- `Configuration[]`

### Spring.GetConfigInt {#Spring.GetConfigInt}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4803-L4810" target="_blank">source</a>]

```lua
Spring.GetConfigInt(string, integer) -> integer
```

**Parameters**

- `name` `string`
- `default` `integer` — Default value if `name` is not found

**Returns**

- `integer`

### Spring.GetConfigFloat {#Spring.GetConfigFloat}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4825-L4832" target="_blank">source</a>]

```lua
Spring.GetConfigFloat(string, number) -> number
```

**Parameters**

- `name` `string`
- `default` `number` — Default value if `name` is not found

**Returns**

- `number`

### Spring.GetConfigString {#Spring.GetConfigString}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4847-L4854" target="_blank">source</a>]

```lua
Spring.GetConfigString(string, string) -> string
```

**Parameters**

- `name` `string`
- `default` `string` — Default value if `name` is not found

**Returns**

- `string`

### Spring.GetLogSections {#Spring.GetLogSections}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4869-L4873" target="_blank">source</a>]

```lua
Spring.GetLogSections() -> table<string,integer>
```

**Returns**

- `sections` `table<string,integer>` — where keys are names and loglevel are values. E.g. `{ "KeyBindings" = LOG.INFO, "Font" = LOG.INFO, "Sound" = LOG.WARNING, ... }`

### Spring.GetAllGroundDecals {#Spring.GetAllGroundDecals}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4897-L4902" target="_blank">source</a>]

```lua
Spring.GetAllGroundDecals() -> DecalID[]
```

**Returns**

- `decalIDs` `DecalID[]`

### Spring.GetGroundDecalMiddlePos {#Spring.GetGroundDecalMiddlePos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4931-L4937" target="_blank">source</a>]

```lua
Spring.GetGroundDecalMiddlePos(DecalID) -> number?, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `posX` `number?`
- `posZ` `number`

### Spring.GetGroundDecalQuadPos {#Spring.GetGroundDecalQuadPos}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4952-L4964" target="_blank">source</a>]

```lua
Spring.GetGroundDecalQuadPos(DecalID) -> number?, number, number, number, number, number, number, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `posTL.x` `number?`
- `posTL.z` `number`
- `posTR.x` `number`
- `posTR.z` `number`
- `posBR.x` `number`
- `posBR.z` `number`
- `posBL.x` `number`
- `posBL.z` `number`

### Spring.GetGroundDecalSizeAndHeight {#Spring.GetGroundDecalSizeAndHeight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L4985-L4992" target="_blank">source</a>]

```lua
Spring.GetGroundDecalSizeAndHeight(DecalID) -> number?, number, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `sizeX` `number?`
- `sizeY` `number`
- `projCubeHeight` `number`

### Spring.GetGroundDecalRotation {#Spring.GetGroundDecalRotation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5009-L5014" target="_blank">source</a>]

```lua
Spring.GetGroundDecalRotation(DecalID) -> number?
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `rotation` `number?` — Rotation in radians.

### Spring.GetGroundDecalTexture {#Spring.GetGroundDecalTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5028-L5034" target="_blank">source</a>]

```lua
Spring.GetGroundDecalTexture(DecalID, boolean?) -> string?
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `isMainTex` `boolean?` — (Default: `true`) If `false`, return the normal/glow map.

**Returns**

- `texture` `string?`

### Spring.GetGroundDecalTextures {#Spring.GetGroundDecalTextures}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5043-L5050" target="_blank">source</a>]

**See:** [Spring.GetGroundDecalTexture](Spring.md#Spring.GetGroundDecalTexture)

```lua
Spring.GetGroundDecalTextures(boolean?, boolean?) -> string[]
```

**Parameters**

- `isMainTex` `boolean?` — (Default: `nil`). If `nil` - no filtering is done, if `false` - return normal/glow textures, if `true` - return main color textures.
- `addFilenames` `boolean?` — (Default: `false`). If `true` add the texture filenames in the second table

**Returns**

- `textureNames` `string[]` — All textures on the atlas and available for use in `SetGroundDecalTexture`.

### Spring.GetGroundDecalTextureParams {#Spring.GetGroundDecalTextureParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5071-L5077" target="_blank">source</a>]

```lua
Spring.GetGroundDecalTextureParams(DecalID) -> number?, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `texWrapDistance` `number?` — If non-zero, sets the mode to repeat the texture along the left-right direction of the decal every texWrapFactor elmos.
- `texTraveledDistance` `number` — Shifts the texture repetition defined by texWrapFactor so the texture of a next line in the continuous multiline can start where the previous finished. For that it should collect all elmo lengths of the previously set multiline segments.

### Spring.GetGroundDecalAlpha {#Spring.GetGroundDecalAlpha}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5092-L5098" target="_blank">source</a>]

```lua
Spring.GetGroundDecalAlpha(DecalID) -> number?, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `alpha` `number?` — Between 0 and 1
- `alphaFalloff` `number` — Between 0 and 1, per second

### Spring.GetGroundDecalNormal {#Spring.GetGroundDecalNormal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5112-L5122" target="_blank">source</a>]

If all three equal 0, the decal follows the normals of ground at midpoint

```lua
Spring.GetGroundDecalNormal(DecalID) -> number?, number, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `normal.x` `number?`
- `normal.y` `number`
- `normal.z` `number`

### Spring.GetGroundDecalTint {#Spring.GetGroundDecalTint}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5137-L5147" target="_blank">source</a>]

Gets the tint of the ground decal.
A color of (0.5, 0.5, 0.5, 0.5) is effectively no tint

```lua
Spring.GetGroundDecalTint(DecalID) -> number?, number, number, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `tintR` `number?`
- `tintG` `number`
- `tintB` `number`
- `tintA` `number`

### Spring.GetGroundDecalMisc {#Spring.GetGroundDecalMisc}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5164-L5174" target="_blank">source</a>]

Returns less important parameters of a ground decal

```lua
Spring.GetGroundDecalMisc(DecalID) -> number?, number, number, number, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `dotElimExp` `number?`
- `refHeight` `number`
- `minHeight` `number`
- `maxHeight` `number`
- `forceHeightMode` `number`

### Spring.GetGroundDecalCreationFrame {#Spring.GetGroundDecalCreationFrame}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5190-L5199" target="_blank">source</a>]

Min can be not equal to max for "gradient" style decals, e.g. unit tracks

```lua
Spring.GetGroundDecalCreationFrame(DecalID) -> number?, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `creationFrameMin` `number?`
- `creationFrameMax` `number`

### Spring.GetGroundDecalOwner {#Spring.GetGroundDecalOwner}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5214-L5219" target="_blank">source</a>]

```lua
Spring.GetGroundDecalOwner(DecalID) -> integer?
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `value` `integer?` — If owner is a unit, then this is `unitID`, if owner is
a feature it is `featureID + MAX_UNITS`. If there is no owner, then `nil`.

### Spring.GetGroundDecalGlowParams {#Spring.GetGroundDecalGlowParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5234-L5241" target="_blank">source</a>]

Gets the glow parameters of the ground decal.

```lua
Spring.GetGroundDecalGlowParams(DecalID) -> number?, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `glow` `number?` — Between 0 and 1
- `glowFalloff` `number` — Between 0 and 1, per second

### Spring.GetGroundDecalUserData {#Spring.GetGroundDecalUserData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5258-L5268" target="_blank">source</a>]

Gets the user defined decal data.

```lua
Spring.GetGroundDecalUserData(DecalID, integer) -> number?, number, number, number
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)
- `udQuad` `integer` — vec4 index, must be within [0;1] for now

**Returns**

- `x` `number?`
- `y` `number`
- `z` `number`
- `w` `number`

### Spring.GetGroundDecalType {#Spring.GetGroundDecalType}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5289-L5294" target="_blank">source</a>]

```lua
Spring.GetGroundDecalType(DecalID) -> ("explosion"|"plate"|"lua"|"track"|"unknown")?
```

**Parameters**

- `decalID` [`DecalID`](Aliases.md#DecalID)

**Returns**

- `type` `("explosion"|"plate"|"lua"|"track"|"unknown")?`

### Spring.GetSyncedGCInfo {#Spring.GetSyncedGCInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5331-L5336" target="_blank">source</a>]

```lua
Spring.GetSyncedGCInfo(boolean?) -> integer?
```

**Parameters**

- `collectGC` `boolean?` — (Default: `false`) collect before returning metric

**Returns**

- `GC` `integer?` — values are expressed in Kbytes: #bytes/2^10

### Spring.SolveNURBSCurve {#Spring.SolveNURBSCurve}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L5358-L5366" target="_blank">source</a>]

```lua
Spring.SolveNURBSCurve(integer, number[], number[], integer) -> number[]
```

**Parameters**

- `degree` `integer` — Degree of the curve.
- `controlPoints` `number[]` — Flat array of `x, y, z, weight` quadruples; its length must be a multiple of 4.
- `knots` `number[]` — Knot vector.
- `segments` `integer` — Number of segments to evaluate.

**Returns**

- `points` `number[]` — Flat array of `x, y, z` triples along the curve.

### Spring.Echo {#Spring.Echo}
*function*

Prints values in the spring chat console. Useful for debugging.

Hint: the default print() writes to STDOUT.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUtils.cpp#L1392-L1402" target="_blank">source</a>]

```lua
Spring.Echo(any, [any, ]*) -> nil
```

**Parameters**

- `arg` `any`
- `...` `any`

**Returns**

- `nil`

### Spring.Log {#Spring.Log}
*function*

Logs a message to the logfile/console.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUtils.cpp#L1472-L1479" target="_blank">source</a>]

```lua
Spring.Log(string, (LogLevel|LOG)?, [string, ]*) -> nil
```

**Parameters**

- `section` `string` — Sets an arbitrary section. Level filtering can be applied per-section
- `logLevel` `(LogLevel|LOG)?` — (Default: `"notice"`)
- `...` `string` — messages

**Fields**

- <span id="Spring.UnitRendering"></span> `Spring.UnitRendering` [`ObjectRenderingTable`](ObjectRenderingTable.md#ObjectRenderingTable) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaRules.cpp#L95-L95" target="_blank">source</a>]
- <span id="Spring.FeatureRendering"></span> `Spring.FeatureRendering` [`ObjectRenderingTable`](ObjectRenderingTable.md#ObjectRenderingTable) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaRules.cpp#L101-L101" target="_blank">source</a>]
- <span id="Spring.MoveCtrl"></span> `Spring.MoveCtrl` [`MoveCtrl`](MoveCtrl.md#MoveCtrl) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L390-L390" target="_blank">source</a>]
- <span id="Spring.UnitScript"></span> `Spring.UnitScript` [`UnitScriptTable`](UnitScriptTable.md#UnitScriptTable) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L394-L394" target="_blank">source</a>]
- <span id="Spring.ALL_UNITS"></span> `Spring.ALL_UNITS` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L103-L103" target="_blank">source</a>]
- <span id="Spring.MY_UNITS"></span> `Spring.MY_UNITS` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L105-L105" target="_blank">source</a>]
- <span id="Spring.ALLY_UNITS"></span> `Spring.ALLY_UNITS` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L107-L107" target="_blank">source</a>]
- <span id="Spring.ENEMY_UNITS"></span> `Spring.ENEMY_UNITS` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L109-L109" target="_blank">source</a>]
