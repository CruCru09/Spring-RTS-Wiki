---
title: "Callins"
tags:
  - Lua-API
---

## Callins {#Callins}
*class*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L87-L118" target="_blank">source</a>]

**Members**

### Callins:Initialize {#Callins:Initialize}
*function*

Called when the addon is (re)loaded.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L526-L529" target="_blank">source</a>]

```lua
Callins:Initialize() -> nil
```

### Callins:LoadCode {#Callins:LoadCode}
*function*

Called when the game is (re)loaded.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L531-L534" target="_blank">source</a>]

```lua
Callins:LoadCode() -> nil
```

### Callins:Shutdown {#Callins:Shutdown}
*function*

Called when the addon or the game is shutdown.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L608-L612" target="_blank">source</a>]

```lua
Callins:Shutdown() -> nil
```

**Returns**

- `nil`

### Callins:GotChatMsg {#Callins:GotChatMsg}
*function*

Called when a player issues a UI command e.g. types /foo or /luarules foo.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L630-L635" target="_blank">source</a>]

```lua
Callins:GotChatMsg(string, PlayerID) -> nil
```

**Parameters**

- `msg` `string`
- `playerID` [`PlayerID`](Aliases.md#PlayerID)

### Callins:Load {#Callins:Load}
*function*

Called after `GamePreload` and before `GameStart`. See Lua_SaveLoad.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L662-L666" target="_blank">source</a>]

```lua
Callins:Load(table) -> nil
```

**Parameters**

- `zipReader` `table`

### Callins:GamePreload {#Callins:GamePreload}
*function*

Called before the 0 gameframe.

Is not called when a saved game is loaded.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L724-L729" target="_blank">source</a>]

```lua
Callins:GamePreload() -> nil
```

### Callins:GameStart {#Callins:GameStart}
*function*

Called upon the start of the game.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L747-L752" target="_blank">source</a>]

Is not called when a saved game is loaded.

```lua
Callins:GameStart() -> nil
```

### Callins:GameOver {#Callins:GameOver}
*function*

Called when the game ends

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L770-L774" target="_blank">source</a>]

```lua
Callins:GameOver(AllyTeamID[]) -> nil
```

**Parameters**

- `winningAllyTeams` `AllyTeamID[]` — list of winning allyTeams, if empty the game result was undecided (like when dropping from an host).

### Callins:GamePaused {#Callins:GamePaused}
*function*

Called when the game is paused.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L797-L802" target="_blank">source</a>]

```lua
Callins:GamePaused(PlayerID, boolean) -> nil
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `paused` `boolean`

### Callins:GameFrame {#Callins:GameFrame}
*function*

Called for every game simulation frame (30 per second).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L847-L851" target="_blank">source</a>]

```lua
Callins:GameFrame(integer) -> nil
```

**Parameters**

- `frame` `integer` — Starts at frame 1

### Callins:GameFramePost {#Callins:GameFramePost}
*function*

Called at the end of every game simulation frame

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L881-L885" target="_blank">source</a>]

```lua
Callins:GameFramePost(integer) -> nil
```

**Parameters**

- `frame` `integer` — Starts at frame 1

### Callins:GameID {#Callins:GameID}
*function*

Called once to deliver the gameID

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L905-L909" target="_blank">source</a>]

```lua
Callins:GameID(string) -> nil
```

**Parameters**

- `gameID` `string` — encoded in hex.

### Callins:TeamDied {#Callins:TeamDied}
*function*

Called when a team dies (see [Spring.KillTeam](Spring.md#Spring.KillTeam)).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L936-L940" target="_blank">source</a>]

```lua
Callins:TeamDied(TeamID) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

### Callins:TeamChanged {#Callins:TeamChanged}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L960-L963" target="_blank">source</a>]

```lua
Callins:TeamChanged(TeamID) -> nil
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)

### Callins:PlayerChanged {#Callins:PlayerChanged}
*function*

Called whenever a player's status changes e.g. becoming a spectator.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L983-L987" target="_blank">source</a>]

```lua
Callins:PlayerChanged(PlayerID) -> nil
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)

### Callins:PlayerAdded {#Callins:PlayerAdded}
*function*

Called whenever a new player joins the game.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1007-L1011" target="_blank">source</a>]

```lua
Callins:PlayerAdded(PlayerID) -> nil
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)

### Callins:PlayerRemoved {#Callins:PlayerRemoved}
*function*

Called whenever a player is removed from the game.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1031-L1036" target="_blank">source</a>]

```lua
Callins:PlayerRemoved(PlayerID, integer) -> nil
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `reason` `integer`

### Callins:UnitCreated {#Callins:UnitCreated}
*function*

Called at the moment the unit is created.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1081-L1088" target="_blank">source</a>]

```lua
Callins:UnitCreated(UnitID, UnitDefID, TeamID, UnitID?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `builderID` `UnitID?`

### Callins:UnitFinished {#Callins:UnitFinished}
*function*

Called at the moment the unit is completed.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1112-L1118" target="_blank">source</a>]

```lua
Callins:UnitFinished(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitFromFactory {#Callins:UnitFromFactory}
*function*

Called when a factory finishes construction of a unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1131-L1140" target="_blank">source</a>]

```lua
Callins:UnitFromFactory(UnitID, UnitDefID, TeamID, UnitID, UnitDefID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `factID` [`UnitID`](Aliases.md#UnitID)
- `factDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `userOrders` `boolean`

### Callins:UnitReverseBuilt {#Callins:UnitReverseBuilt}
*function*

Called when a living unit becomes a nanoframe again.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1165-L1171" target="_blank">source</a>]

```lua
Callins:UnitReverseBuilt(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitConstructionDecayed {#Callins:UnitConstructionDecayed}
*function*

Called when a unit being built starts decaying.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1180-L1189" target="_blank">source</a>]

```lua
Callins:UnitConstructionDecayed(UnitID, UnitDefID, TeamID, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `timeSinceLastBuild` `number`
- `iterationPeriod` `number`
- `part` `number`

### Callins:UnitDestroyed {#Callins:UnitDestroyed}
*function*

Called when a unit is destroyed.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1213-L1223" target="_blank">source</a>]

```lua
Callins:UnitDestroyed(UnitID, UnitDefID, TeamID, UnitID?, UnitDefID?, TeamID?, WeaponDefID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `attackerID` `UnitID?` — Subject to visibility rules
- `attackerDefID` `UnitDefID?` — Subject to visibility rules
- `attackerTeam` `TeamID?` — Subject to visibility rules
- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)

### Callins:UnitTaken {#Callins:UnitTaken}
*function*

Called when a unit is transferred between teams. This is called before `UnitGiven` and in that moment unit is still assigned to the oldTeam.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1251-L1258" target="_blank">source</a>]

```lua
Callins:UnitTaken(UnitID, UnitDefID, TeamID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `oldTeam` [`TeamID`](Aliases.md#TeamID)
- `newTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitGiven {#Callins:UnitGiven}
*function*

Called when a unit is transferred between teams. This is called after `UnitTaken` and in that moment unit is assigned to the newTeam.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1280-L1287" target="_blank">source</a>]

```lua
Callins:UnitGiven(UnitID, UnitDefID, TeamID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `newTeam` [`TeamID`](Aliases.md#TeamID)
- `oldTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitIdle {#Callins:UnitIdle}
*function*

Called when a unit is idle (empty command queue).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1309-L1315" target="_blank">source</a>]

```lua
Callins:UnitIdle(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitCommand {#Callins:UnitCommand}
*function*

Called after when a unit accepts a command, after `AllowCommand` returns true.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1323-L1333" target="_blank">source</a>]

```lua
Callins:UnitCommand(UnitID, UnitDefID, TeamID, integer, table, CommandOptions, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `cmdID` `integer`
- `cmdParams` `table`
- `options` [`CommandOptions`](CommandOptions.md#CommandOptions)
- `cmdTag` `integer`

### Callins:UnitCmdDone {#Callins:UnitCmdDone}
*function*

Called when a unit completes a command.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1357-L1367" target="_blank">source</a>]

```lua
Callins:UnitCmdDone(UnitID, UnitDefID, TeamID, integer, table, CommandOptions, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `cmdID` `integer`
- `cmdParams` `table`
- `options` [`CommandOptions`](CommandOptions.md#CommandOptions)
- `cmdTag` `integer`

### Callins:UnitDamaged {#Callins:UnitDamaged}
*function*

Called when a unit is damaged (after UnitPreDamaged).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1387-L1400" target="_blank">source</a>]

```lua
Callins:UnitDamaged(UnitID, UnitDefID, TeamID, number, number, WeaponDefID, ProjectileID, UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `damage` `number`
- `paralyzer` `number`
- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)
- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `attackerID` [`UnitID`](Aliases.md#UnitID)
- `attackerDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `attackerTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitStunned {#Callins:UnitStunned}
*function*

Called when a unit changes its stun status.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1435-L1442" target="_blank">source</a>]

```lua
Callins:UnitStunned(UnitID, UnitDefID, TeamID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `stunned` `boolean`

### Callins:UnitExperience {#Callins:UnitExperience}
*function*

Called when a unit gains experience greater or equal to the minimum limit set by calling [Spring.SetExperienceGrade](Spring.md#Spring.SetExperienceGrade).

Should be called more reliably with small values of experience grade.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1466-L1478" target="_blank">source</a>]

```lua
Callins:UnitExperience(UnitID, UnitDefID, TeamID, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `experience` `number`
- `oldExperience` `number`

### Callins:UnitHarvestStorageFull {#Callins:UnitHarvestStorageFull}
*function*

Called when a unit's harvestStorage is full (according to its unitDef's entry).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1502-L1508" target="_blank">source</a>]

```lua
Callins:UnitHarvestStorageFull(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitSeismicPing {#Callins:UnitSeismicPing}
*function*

Called when a unit emits a seismic ping.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1518-L1531" target="_blank">source</a>]

See `seismicSignature`.

```lua
Callins:UnitSeismicPing(number, number, number, number, AllyTeamID, UnitID, UnitDefID) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`
- `strength` `number`
- `allyTeam` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)

### Callins:UnitEnteredRadar {#Callins:UnitEnteredRadar}
*function*

Called when a unit enters radar of an allyteam.

Also called when a unit enters LOS without any radar coverage.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1585-L1595" target="_blank">source</a>]

```lua
Callins:UnitEnteredRadar(UnitID, TeamID, AllyTeamID, UnitDefID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `allyTeam` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)

### Callins:UnitEnteredLos {#Callins:UnitEnteredLos}
*function*

Called when a unit enters LOS of an allyteam.

Its called after the unit is in LOS, so you can query that unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1604-L1614" target="_blank">source</a>]

```lua
Callins:UnitEnteredLos(UnitID, TeamID, AllyTeamID, UnitDefID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `allyTeam` [`AllyTeamID`](Aliases.md#AllyTeamID) — who's LOS the unit entered.
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)

### Callins:UnitLeftRadar {#Callins:UnitLeftRadar}
*function*

Called when a unit leaves radar of an allyteam.

Also called when a unit leaves LOS without any radar coverage.
For widgets, this is called just after a unit leaves radar coverage, so
widgets cannot get the position of units that left their radar.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1622-L1634" target="_blank">source</a>]

```lua
Callins:UnitLeftRadar(UnitID, TeamID, AllyTeamID, UnitDefID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `allyTeam` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)

### Callins:UnitLeftLos {#Callins:UnitLeftLos}
*function*

Called when a unit leaves LOS of an allyteam.

For widgets, this one is called just before the unit leaves los, so you can still get the position of a unit that left los.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1643-L1653" target="_blank">source</a>]

```lua
Callins:UnitLeftLos(UnitID, TeamID, AllyTeamID, UnitDefID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `allyTeam` [`AllyTeamID`](Aliases.md#AllyTeamID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)

### Callins:UnitLoaded {#Callins:UnitLoaded}
*function*

Called when a unit is loaded by a transport.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1667-L1675" target="_blank">source</a>]

```lua
Callins:UnitLoaded(UnitID, UnitDefID, TeamID, UnitID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `transportID` [`UnitID`](Aliases.md#UnitID)
- `transportTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitUnloaded {#Callins:UnitUnloaded}
*function*

Called when a unit is unloaded by a transport.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1699-L1707" target="_blank">source</a>]

```lua
Callins:UnitUnloaded(UnitID, UnitDefID, TeamID, UnitID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `transportID` [`UnitID`](Aliases.md#UnitID)
- `transportTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitEnteredUnderwater {#Callins:UnitEnteredUnderwater}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1737-L1743" target="_blank">source</a>]

```lua
Callins:UnitEnteredUnderwater(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitEnteredWater {#Callins:UnitEnteredWater}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1751-L1757" target="_blank">source</a>]

```lua
Callins:UnitEnteredWater(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitLeftAir {#Callins:UnitLeftAir}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1765-L1772" target="_blank">source</a>]

```lua
Callins:UnitLeftAir(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitLeftUnderwater {#Callins:UnitLeftUnderwater}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1780-L1787" target="_blank">source</a>]

```lua
Callins:UnitLeftUnderwater(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitLeftWater {#Callins:UnitLeftWater}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1794-L1801" target="_blank">source</a>]

```lua
Callins:UnitLeftWater(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitEnteredAir {#Callins:UnitEnteredAir}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1809-L1816" target="_blank">source</a>]

```lua
Callins:UnitEnteredAir(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitCloaked {#Callins:UnitCloaked}
*function*

Called when a unit cloaks.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1824-L1831" target="_blank">source</a>]

```lua
Callins:UnitCloaked(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitDecloaked {#Callins:UnitDecloaked}
*function*

Called when a unit decloaks.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1839-L1846" target="_blank">source</a>]

```lua
Callins:UnitDecloaked(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitUnitCollision {#Callins:UnitUnitCollision}
*function*

Called when two units collide.

Both units must be registered with [Script.SetWatchUnit](Script.md#Script.SetWatchUnit).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1854-L1861" target="_blank">source</a>]

```lua
Callins:UnitUnitCollision(UnitID, UnitID) -> nil
```

**Parameters**

- `colliderID` [`UnitID`](Aliases.md#UnitID)
- `collideeID` [`UnitID`](Aliases.md#UnitID)

### Callins:UnitFeatureCollision {#Callins:UnitFeatureCollision}
*function*

Called when a unit collides with a feature.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1905-L1913" target="_blank">source</a>]

The unit must be registered with [Script.SetWatchUnit](Script.md#Script.SetWatchUnit) and the feature registered with [Script.SetWatchFeature](Script.md#Script.SetWatchFeature).

```lua
Callins:UnitFeatureCollision(UnitID, UnitID) -> nil
```

**Parameters**

- `colliderID` [`UnitID`](Aliases.md#UnitID)
- `collideeID` [`UnitID`](Aliases.md#UnitID)

### Callins:UnitMoveFailed {#Callins:UnitMoveFailed}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1958-L1965" target="_blank">source</a>]

```lua
Callins:UnitMoveFailed(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:UnitArrivedAtGoal {#Callins:UnitArrivedAtGoal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1980-L1987" target="_blank">source</a>]

```lua
Callins:UnitArrivedAtGoal(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:RenderUnitDestroyed {#Callins:RenderUnitDestroyed}
*function*

Called just before a unit is invalid, after it finishes its death animation.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L1997-L2004" target="_blank">source</a>]

```lua
Callins:RenderUnitDestroyed(UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:FeatureCreated {#Callins:FeatureCreated}
*function*

Called when a feature is created.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2035-L2041" target="_blank">source</a>]

```lua
Callins:FeatureCreated(FeatureID, AllyTeamID) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)

### Callins:FeatureDestroyed {#Callins:FeatureDestroyed}
*function*

Called when a feature is destroyed.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2062-L2068" target="_blank">source</a>]

```lua
Callins:FeatureDestroyed(FeatureID, AllyTeamID) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)

### Callins:FeatureDamaged {#Callins:FeatureDamaged}
*function*

Called when a feature is damaged.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2089-L2102" target="_blank">source</a>]

```lua
Callins:FeatureDamaged(FeatureID, FeatureDefID, TeamID, number, WeaponDefID, ProjectileID, UnitID, UnitDefID, TeamID) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `featureDefID` [`FeatureDefID`](Aliases.md#FeatureDefID)
- `featureTeam` [`TeamID`](Aliases.md#TeamID)
- `damage` `number`
- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)
- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `attackerID` [`UnitID`](Aliases.md#UnitID)
- `attackerDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `attackerTeam` [`TeamID`](Aliases.md#TeamID)

### Callins:ProjectileCreated {#Callins:ProjectileCreated}
*function*

Called when the projectile is created.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2144-L2156" target="_blank">source</a>]

Note that weaponDefID is missing if the projectile is spawned as part of a burst, but [Spring.GetProjectileDefID](Spring.md#Spring.GetProjectileDefID) and `Spring.GetProjectileName` still work in callin scope using proID.

**See:** [Script.SetWatchWeapon](Script.md#Script.SetWatchWeapon)

```lua
Callins:ProjectileCreated(ProjectileID, UnitID, WeaponDefID) -> nil
```

**Parameters**

- `proID` [`ProjectileID`](Aliases.md#ProjectileID)
- `proOwnerID` [`UnitID`](Aliases.md#UnitID)
- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)

### Callins:ProjectileDestroyed {#Callins:ProjectileDestroyed}
*function*

Called when the projectile is destroyed.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2196-L2205" target="_blank">source</a>]

**See:** [Script.SetWatchWeapon](Script.md#Script.SetWatchWeapon)

```lua
Callins:ProjectileDestroyed(ProjectileID, UnitID, WeaponDefID) -> nil
```

**Parameters**

- `proID` [`ProjectileID`](Aliases.md#ProjectileID)
- `ownerID` [`UnitID`](Aliases.md#UnitID)
- `proWeaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)

### Callins:Explosion {#Callins:Explosion}
*function*

Called when an explosion occurs.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2262-L2279" target="_blank">source</a>]

Only called for weaponDefIDs registered via Script.SetWatchExplosion or Script.SetWatchWeapon.

**See:** [Script.SetWatchWeapon](Script.md#Script.SetWatchWeapon)

```lua
Callins:Explosion(WeaponDefID, number, number, number, UnitID, ProjectileID) -> boolean
```

**Parameters**

- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)
- `px` `number`
- `py` `number`
- `pz` `number`
- `attackerID` [`UnitID`](Aliases.md#UnitID)
- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `noGfx` `boolean` — if then no graphical effects are drawn by the engine for this explosion.

### Callins:StockpileChanged {#Callins:StockpileChanged}
*function*

Called when a units stockpile of weapons increases or decreases.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2328-L2338" target="_blank">source</a>]

```lua
Callins:StockpileChanged(UnitID, UnitDefID, TeamID, integer, integer, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `weaponNum` `integer`
- `oldCount` `integer`
- `newCount` `integer`

### Callins:RecvLuaMsg {#Callins:RecvLuaMsg}
*function*

Receives messages from unsynced sent via [Spring.SendLuaRulesMsg](Spring.md#Spring.SendLuaRulesMsg) or [Spring.SendLuaUIMsg](Spring.md#Spring.SendLuaUIMsg).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2363-L2368" target="_blank">source</a>]

```lua
Callins:RecvLuaMsg(string, PlayerID) -> nil
```

**Parameters**

- `msg` `string`
- `playerID` [`PlayerID`](Aliases.md#PlayerID)

### Callins:Save {#Callins:Save}
*function*

Called when a chat command '/save' or '/savegame' is received.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2499-L2503" target="_blank">source</a>]

```lua
Callins:Save(table) -> nil
```

**Parameters**

- `zip` `table` — a userdatum representing the savegame zip file. See Lua_SaveLoad.

### Callins:UnsyncedHeightMapUpdate {#Callins:UnsyncedHeightMapUpdate}
*function*

Called when the unsynced copy of the height-map is altered.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2525-L2532" target="_blank">source</a>]

```lua
Callins:UnsyncedHeightMapUpdate() -> integer, integer, integer, integer
```

**Returns**

- `x1` `integer`
- `z1` `integer`
- `x2` `integer`
- `z2` `integer`

### Callins:Update {#Callins:Update}
*function*

Called for every draw frame (including when the game is paused) and at least once per sim frame except when catching up.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2552-L2556" target="_blank">source</a>]

```lua
Callins:Update(number) -> nil
```

**Parameters**

- `dt` `number` — the time since the last update.

### Callins:ViewResize {#Callins:ViewResize}
*function*

Called whenever the window is resized.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2573-L2578" target="_blank">source</a>]

```lua
Callins:ViewResize(integer, integer) -> nil
```

**Parameters**

- `viewSizeX` `integer`
- `viewSizeY` `integer`

### Callins:FontsChanged {#Callins:FontsChanged}
*function*

Called whenever fonts are updated. Signals the game display lists
and other caches should be discarded.

Gets called before other Update and Draw callins.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2612-L2618" target="_blank">source</a>]

```lua
Callins:FontsChanged() -> nil
```

### Callins:SunChanged {#Callins:SunChanged}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2633-L2635" target="_blank">source</a>]

```lua
Callins:SunChanged() -> nil
```

### Callins:NanoParticleUpdate {#Callins:NanoParticleUpdate}
*function*

Batched nano particle lifecycle changes.

Only sent while the `NanoParticlesGL4` and `NanoParticlesUpdateLuaUI`
springsettings are both on, and only for the sampled fraction of particles
set by `NanoParticlesUpdateLuaUISampleRate` - one event per particle per
frame would overwhelm any consumer. Intended for deferred-lighting widgets.

Events are passed as one flat numeric array to keep the marshalling cost
down. Each event occupies 13 consecutive entries:
`{operation, lightID, px, py, pz, vx, vy, vz, remainingLife, r, g, b, builderBuildSpeed}`.

Operations are 1 = spawn, 2 = update, 3 = remove, 4 = reset.

A particle's lifetime is fixed when it spawns, so `remainingLife` is exact and
consumers are expected to expire their own state from it; operation 3 is
reserved and currently never sent. A reset means every previously reported
lightID is gone and any state keyed on them should be dropped; it is always
the first event of its batch.

Particles are not projectiles and have no projectile ID; `lightID` is unique,
negative, and only valid until the particle expires or a reset arrives.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2649-L2675" target="_blank">source</a>]

```lua
Callins:NanoParticleUpdate(number[], integer, integer) -> nil
```

**Parameters**

- `events` `number[]` — Flat event records.
- `eventCount` `integer` — Number of records in `events`.
- `gameFrame` `integer` — Current simulation frame.

### Callins:DefaultCommand {#Callins:DefaultCommand}
*function*

Used to set the default command when a unit is selected.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2712-L2719" target="_blank">source</a>]

```lua
Callins:DefaultCommand(("unit"|"feature"), ObjectID, integer) -> integer
```

**Parameters**

- `type` `("unit"|"feature")` — The type of the object pointed at.
- `id` [`ObjectID`](Aliases.md#ObjectID) — The `unitID` or `featureID`.
- `cmd` `integer` — The current command ID.

**Returns**

- `cmdID` `integer` — The command ID to use as the default, or nil to keep the current ID.

### Callins:DrawGenesis {#Callins:DrawGenesis}
*function*

Use this callin to update textures, shaders, etc.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2806-L2812" target="_blank">source</a>]

Doesn't render to screen!
Also available to LuaMenu.

```lua
Callins:DrawGenesis() -> nil
```

### Callins:DrawWorld {#Callins:DrawWorld}
*function*

Spring draws command queues, 'map stuff', and map marks.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2815-L2818" target="_blank">source</a>]

```lua
Callins:DrawWorld() -> nil
```

### Callins:DrawWorldPreUnit {#Callins:DrawWorldPreUnit}
*function*

Spring draws units, features, some water types, cloaked units, and the sun.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2821-L2824" target="_blank">source</a>]

```lua
Callins:DrawWorldPreUnit() -> nil
```

### Callins:DrawPreDecals {#Callins:DrawPreDecals}
*function*

Called before decals are drawn

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2827-L2830" target="_blank">source</a>]

```lua
Callins:DrawPreDecals() -> nil
```

### Callins:DrawWaterPost {#Callins:DrawWaterPost}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2833-L2835" target="_blank">source</a>]

```lua
Callins:DrawWaterPost() -> nil
```

### Callins:DrawShadowPassTransparent {#Callins:DrawShadowPassTransparent}
*function*

Invoked after semi-transparent shadows pass is about to conclude

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2838-L2842" target="_blank">source</a>]

This callin has depth and color buffer of shadowmap bound via FBO as well as the FFP state to do "semi-transparent" shadows pass (traditionally only used to draw shadows of shadow casting semi-transparent particles). Can be used to draw nice colored shadows.

```lua
Callins:DrawShadowPassTransparent() -> nil
```

### Callins:DrawWorldShadow {#Callins:DrawWorldShadow}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2845-L2847" target="_blank">source</a>]

```lua
Callins:DrawWorldShadow() -> nil
```

### Callins:DrawWorldReflection {#Callins:DrawWorldReflection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2850-L2852" target="_blank">source</a>]

```lua
Callins:DrawWorldReflection() -> nil
```

### Callins:DrawWorldRefraction {#Callins:DrawWorldRefraction}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2855-L2857" target="_blank">source</a>]

```lua
Callins:DrawWorldRefraction() -> nil
```

### Callins:DrawGroundPreForward {#Callins:DrawGroundPreForward}
*function*

Runs at the start of the forward pass when a custom map shader has been assigned via [Spring.SetMapShader](Spring.md#Spring.SetMapShader) (convenient for setting uniforms).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2860-L2863" target="_blank">source</a>]

```lua
Callins:DrawGroundPreForward() -> nil
```

### Callins:DrawGroundPostForward {#Callins:DrawGroundPostForward}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2866-L2868" target="_blank">source</a>]

```lua
Callins:DrawGroundPostForward() -> nil
```

### Callins:DrawGroundPreDeferred {#Callins:DrawGroundPreDeferred}
*function*

Runs at the start of the deferred pass when a custom map shader has been assigned via [Spring.SetMapShader](Spring.md#Spring.SetMapShader) (convenient for setting uniforms).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2871-L2874" target="_blank">source</a>]

```lua
Callins:DrawGroundPreDeferred() -> nil
```

### Callins:DrawGroundDeferred {#Callins:DrawGroundDeferred}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2877-L2879" target="_blank">source</a>]

```lua
Callins:DrawGroundDeferred() -> nil
```

### Callins:DrawGroundPostDeferred {#Callins:DrawGroundPostDeferred}
*function*

This runs at the end of its respective deferred pass.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2882-L2887" target="_blank">source</a>]

Allows proper frame compositing (with ground flashes/decals/foliage/etc, which are drawn between it and `DrawWorldPreUnit`) via [gl.CopyToTexture](gl.md#gl.CopyToTexture).

```lua
Callins:DrawGroundPostDeferred() -> nil
```

### Callins:DrawUnitsPostDeferred {#Callins:DrawUnitsPostDeferred}
*function*

Runs at the end of the unit deferred pass.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2890-L2895" target="_blank">source</a>]

Informs Lua code it should make use of the $model_gbuffer_* textures before another pass overwrites them (and to allow proper blending with e.g. cloaked objects which are drawn between these events and DrawWorld via gl.CopyToTexture). N.B. The *PostDeferred events are only sent (and only have a real purpose) if forward drawing is disabled.

```lua
Callins:DrawUnitsPostDeferred() -> nil
```

### Callins:DrawFeaturesPostDeferred {#Callins:DrawFeaturesPostDeferred}
*function*

Runs at the end of the feature deferred pass to inform Lua code it should make use of the $model_gbuffer_* textures before another pass overwrites them (and to allow proper blending with e.g. cloaked objects which are drawn between these events and DrawWorld via gl.CopyToTexture). N.B. The *PostDeferred events are only sent (and only have a real purpose) if forward drawing is disabled.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2898-L2901" target="_blank">source</a>]

```lua
Callins:DrawFeaturesPostDeferred() -> nil
```

### Callins:DrawShadowUnitsLua {#Callins:DrawShadowUnitsLua}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2904-L2906" target="_blank">source</a>]

```lua
Callins:DrawShadowUnitsLua() -> nil
```

### Callins:DrawShadowFeaturesLua {#Callins:DrawShadowFeaturesLua}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2909-L2911" target="_blank">source</a>]

```lua
Callins:DrawShadowFeaturesLua() -> nil
```

### Callins:DrawBuildSquare {#Callins:DrawBuildSquare}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2914-L2923" target="_blank">source</a>]

Called when build square data is computed, before engine rendering.
Grid dimensions can be inferred from UnitDefs[unitDefID].xsize and UnitDefs[unitDefID].zsize.
Grid origin in square coords: x - xsize/2, z - zsize/2 (accounting for facing).

```lua
Callins:DrawBuildSquare(UnitDefID, integer, integer, number, table) -> nil
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `x` `integer` — build position x
- `z` `integer` — build position z
- `facing` `number` — build facing
- `statuses` `table` — flat 1D row-major array of BuildSquareStatus values: BLOCKED=0, OCCUPIED=1, RECLAIMABLE=2, OPEN=3

### Callins:DrawWorldPreParticles {#Callins:DrawWorldPreParticles}
*function*

DrawWorldPreParticles is called multiples times per draw frame.
Each call has a different permutation of values for drawAboveWater, drawBelowWater, drawReflection, and drawRefraction.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2949-L2958" target="_blank">source</a>]

```lua
Callins:DrawWorldPreParticles(boolean, boolean, boolean, boolean) -> nil
```

**Parameters**

- `drawAboveWater` `boolean`
- `drawBelowWater` `boolean`
- `drawReflection` `boolean`
- `drawRefraction` `boolean`

### Callins:DrawScreen {#Callins:DrawScreen}
*function*

Also available to LuaMenu.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L2997-L3002" target="_blank">source</a>]

```lua
Callins:DrawScreen(integer, integer) -> nil
```

**Parameters**

- `viewSizeX` `integer`
- `viewSizeY` `integer`

### Callins:DrawScreenEffects {#Callins:DrawScreenEffects}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3014-L3018" target="_blank">source</a>]

```lua
Callins:DrawScreenEffects(integer, integer) -> nil
```

**Parameters**

- `viewSizeX` `integer`
- `viewSizeY` `integer`

### Callins:DrawScreenPost {#Callins:DrawScreenPost}
*function*

Similar to DrawScreenEffects, this can be used to alter the contents of a frame after it has been completely rendered (i.e. World, MiniMap, Menu, UI).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3030-L3038" target="_blank">source</a>]

Note: This callin is invoked after the software rendered cursor (configuration variable HardwareCursor=0) is drawn.

```lua
Callins:DrawScreenPost(integer, integer) -> nil
```

**Parameters**

- `viewSizeX` `integer`
- `viewSizeY` `integer`

### Callins:DrawInMiniMap {#Callins:DrawInMiniMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3050-L3055" target="_blank">source</a>]

```lua
Callins:DrawInMiniMap(integer, integer) -> nil
```

**Parameters**

- `sx` `integer` — relative to the minimap's position and scale.
- `sy` `integer` — relative to the minimap's position and scale.

### Callins:DrawInMiniMapBackground {#Callins:DrawInMiniMapBackground}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3078-L3083" target="_blank">source</a>]

```lua
Callins:DrawInMiniMapBackground(integer, integer) -> nil
```

**Parameters**

- `sx` `integer` — relative to the minimap's position and scale.
- `sy` `integer` — relative to the minimap's position and scale.

### Callins:GameProgress {#Callins:GameProgress}
*function*

Called every 60 frames, calculating delta between `GameFrame` and `GameProgress`.

Can give an ETA about catching up with simulation for mid-game join players.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3153-L3159" target="_blank">source</a>]

```lua
Callins:GameProgress(integer) -> nil
```

**Parameters**

- `serverFrameNum` `integer`

### Callins:KeyBindingsChanged {#Callins:KeyBindingsChanged}
*function*

Called after a keybinding command runs.

Called when:

- A keybinding command runs, e.g. `bind k action`. This may fire even when nothing actually changed (e.g. a redundant bind), so treat it as "a binding command ran", not a guarantee that bindings differ. An operation covering multiple keybindings fires a single event at the end, e.g. `keyreload`.
- Any operation that changes how actions are retrieved from input triggers happened, e.g. `fakemeta space`.

Nothing is passed; call [Spring.GetKeyBindings](Spring.md#Spring.GetKeyBindings) to read the current state.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3196-L3206" target="_blank">source</a>]

```lua
Callins:KeyBindingsChanged() -> nil
```

### Callins:KeyMapChanged {#Callins:KeyMapChanged}
*function*

Called when the keymap changes

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3222-L3227" target="_blank">source</a>]

Can be caused due to a change in language or keyboard

```lua
Callins:KeyMapChanged() -> nil
```

### Callins:KeyPress {#Callins:KeyPress}
*function*

Called repeatedly when a key is pressed down.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3264-L3278" target="_blank">source</a>]

Return true if you don't want other callins or the engine to also receive this keypress. A list of key codes can be seen at the SDL wiki.

```lua
Callins:KeyPress(integer, KeyModifiers, boolean, string, integer, integer, table?) -> boolean
```

**Parameters**

- `keyCode` `integer`
- `mods` [`KeyModifiers`](KeyModifiers.md#KeyModifiers)
- `isRepeat` `boolean` — If you want an action to occur only once check for isRepeat == false.
- `label` `string` — the name of the key
- `utf32char` `integer` — (deprecated) always 0
- `scanCode` `integer`
- `actionList` `table?` — the list of actions for this keypress, when available

**Returns**

- `halt` `boolean` — whether to halt the chain for consumers of the keypress

### Callins:KeyRelease {#Callins:KeyRelease}
*function*

Called when the key is released.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3332-L3344" target="_blank">source</a>]

```lua
Callins:KeyRelease(integer, KeyModifiers, string, integer, integer, table?) -> boolean
```

**Parameters**

- `keyCode` `integer`
- `mods` [`KeyModifiers`](KeyModifiers.md#KeyModifiers)
- `label` `string` — the name of the key
- `utf32char` `integer` — (deprecated) always 0
- `scanCode` `integer`
- `actionList` `table?` — the list of actions for this keyrelease, when available

**Returns**

- `boolean`

### Callins:TextInput {#Callins:TextInput}
*function*

Called whenever a key press results in text input.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3393-L3398" target="_blank">source</a>]

```lua
Callins:TextInput(string) -> nil
```

**Parameters**

- `utf8char` `string`

### Callins:TextEditing {#Callins:TextEditing}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3421-L3428" target="_blank">source</a>]

```lua
Callins:TextEditing(string, integer, integer) -> nil
```

**Parameters**

- `utf8` `string`
- `start` `integer`
- `length` `integer`

### Callins:MousePress {#Callins:MousePress}
*function*

Called when a mouse button is pressed.

The button parameter supports up to 7 buttons. Must return true for `MouseRelease` and other functions to be called.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3451-L3460" target="_blank">source</a>]

```lua
Callins:MousePress(integer, integer, integer) -> boolean
```

**Parameters**

- `x` `integer`
- `y` `integer`
- `button` `integer`

**Returns**

- `becomeMouseOwner` `boolean`

### Callins:MouseRelease {#Callins:MouseRelease}
*function*

Called when a mouse button is released.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3484-L3494" target="_blank">source</a>]

Please note that in order to have Spring call `Spring.MouseRelease`, you need to have a `Spring.MousePress` call-in in the same addon that returns true.

```lua
Callins:MouseRelease(integer, integer, integer) -> boolean
```

**Parameters**

- `x` `integer`
- `y` `integer`
- `button` `integer`

**Returns**

- `becomeMouseOwner` `boolean`

### Callins:MouseMove {#Callins:MouseMove}
*function*

Called when the mouse is moved.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3513-L3522" target="_blank">source</a>]

```lua
Callins:MouseMove(integer, integer, integer, integer, integer) -> nil
```

**Parameters**

- `x` `integer` — final x position
- `y` `integer` — final y position
- `dx` `integer` — distance travelled in x
- `dy` `integer` — distance travelled in y
- `button` `integer`

### Callins:MouseWheel {#Callins:MouseWheel}
*function*

Called when the mouse wheel is moved.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3548-L3554" target="_blank">source</a>]

```lua
Callins:MouseWheel(boolean, number) -> nil
```

**Parameters**

- `up` `boolean` — the direction
- `value` `number` — the amount travelled

### Callins:IsAbove {#Callins:IsAbove}
*function*

Called every `Update`.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3575-L3584" target="_blank">source</a>]

Must return true for `Mouse*` events and `Spring.GetToolTip` to be called.

```lua
Callins:IsAbove(integer, integer) -> boolean
```

**Parameters**

- `x` `integer`
- `y` `integer`

**Returns**

- `isAbove` `boolean`

### Callins:GetTooltip {#Callins:GetTooltip}
*function*

Called when `Spring.IsAbove` returns true.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3606-L3612" target="_blank">source</a>]

```lua
Callins:GetTooltip(integer, integer) -> string
```

**Parameters**

- `x` `integer`
- `y` `integer`

**Returns**

- `tooltip` `string`

### Callins:ActiveCommandChanged {#Callins:ActiveCommandChanged}
*function*

Called when a command is issued.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3634-L3639" target="_blank">source</a>]

```lua
Callins:ActiveCommandChanged(integer?, integer?) -> nil
```

**Parameters**

- `cmdId` `integer?`
- `cmdType` `integer?`

### Callins:CameraRotationChanged {#Callins:CameraRotationChanged}
*function*

Called whenever the camera rotation changes

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3660-L3666" target="_blank">source</a>]

```lua
Callins:CameraRotationChanged(number, number, number) -> nil
```

**Parameters**

- `rotX` `number` — Camera rotation around the x axis in radians.
- `rotY` `number` — Camera rotation around the y axis in radians.
- `rotZ` `number` — Camera rotation around the z axis in radians.

### Callins:CameraPositionChanged {#Callins:CameraPositionChanged}
*function*

Called whenever the camera position changes

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3683-L3689" target="_blank">source</a>]

```lua
Callins:CameraPositionChanged(number, number, number) -> nil
```

**Parameters**

- `posX` `number` — Camera position x in world coordinates
- `posY` `number` — Camera position y in world coordinates
- `posZ` `number` — Camera position z in world coordinates

### Callins:MiniMapRotationChanged {#Callins:MiniMapRotationChanged}
*function*

Called when the MiniMap rotation changes

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3707-L3712" target="_blank">source</a>]

```lua
Callins:MiniMapRotationChanged(number, number) -> nil
```

**Parameters**

- `newRot` `number` — MiniMap rotation in radians
- `oldRot` `number` — MiniMap old rotation in radians

### Callins:MiniMapStateChanged {#Callins:MiniMapStateChanged}
*function*

Called when the MiniMap minimizes or maximizes changes

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3729-L3735" target="_blank">source</a>]

```lua
Callins:MiniMapStateChanged(boolean, boolean, boolean) -> nil
```

**Parameters**

- `isMinimized` `boolean`
- `isMaximized` `boolean`
- `isSlaved` `boolean`

### Callins:MiniMapGeometryChanged {#Callins:MiniMapGeometryChanged}
*function*

Called when the MiniMap Geometry changes

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3756-L3767" target="_blank">source</a>]

```lua
Callins:MiniMapGeometryChanged(integer, integer, integer, integer, integer, integer, integer, integer) -> nil
```

**Parameters**

- `newPosX` `integer` — in pixels
- `newPosY` `integer` — in pixels
- `newDimX` `integer` — in pixels
- `newDimY` `integer` — in pixels
- `oldPosX` `integer` — in pixels
- `oldPosY` `integer` — in pixels
- `oldDimX` `integer` — in pixels
- `oldDimY` `integer` — in pixels

### Callins:CommandNotify {#Callins:CommandNotify}
*function*

Called when a command is issued.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3791-L3798" target="_blank">source</a>]

```lua
Callins:CommandNotify(integer, table, CommandOptions) -> boolean
```

**Parameters**

- `cmdID` `integer`
- `cmdParams` `table`
- `options` [`CommandOptions`](CommandOptions.md#CommandOptions)

**Returns**

- `delete` `boolean` — Returning true deletes the command and does not send it through the network.

### Callins:AllowQuit {#Callins:AllowQuit}
*function*

Called when the window is about to be closed (close button, Alt+F4, or a quit request from the OS).

Every unsynced handle is asked and one `false` is enough to keep the game running. [Spring.Quit](Spring.md#Spring.Quit) and `/quitforce` do not ask, so a game that vetoed can still quit later and the user can always force an exit. One click can trigger this twice, once per SDL event. Not asked while the game is still loading, so LuaIntro never receives it.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3827-L3833" target="_blank">source</a>]

```lua
Callins:AllowQuit() -> boolean
```

**Returns**

- `allow` `boolean` — false keeps the game running

### Callins:AddConsoleLine {#Callins:AddConsoleLine}
*function*

Called when text is entered into the console (e.g. [Spring.Echo](Spring.md#Spring.Echo)).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3853-L3858" target="_blank">source</a>]

```lua
Callins:AddConsoleLine(string, integer) -> nil
```

**Parameters**

- `msg` `string`
- `priority` `integer`

### Callins:GroupChanged {#Callins:GroupChanged}
*function*

Called when a unit is added to or removed from a control group.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3876-L3880" target="_blank">source</a>]

```lua
Callins:GroupChanged(GroupID) -> nil
```

**Parameters**

- `groupID` [`GroupID`](Aliases.md#GroupID)

### Callins:WorldTooltip {#Callins:WorldTooltip}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3896-L3901" target="_blank">source</a>]

```lua
Callins:WorldTooltip("unit", UnitID) -> string
```

**Parameters**

- `type` `"unit"`
- `unitId` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `tooltip` `string`

### Callins:WorldTooltip (overload 1) {#Callins:WorldTooltip-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3902-L3907" target="_blank">source</a>]

```lua
Callins:WorldTooltip("feature", FeatureID) -> string
```

**Parameters**

- `type` `"feature"`
- `featureId` [`FeatureID`](Aliases.md#FeatureID)

**Returns**

- `tooltip` `string`

### Callins:WorldTooltip (overload 2) {#Callins:WorldTooltip-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3908-L3915" target="_blank">source</a>]

```lua
Callins:WorldTooltip("ground", number, number, number) -> string
```

**Parameters**

- `type` `"ground"`
- `posX` `number`
- `posY` `number`
- `posZ` `number`

**Returns**

- `tooltip` `string`

### Callins:WorldTooltip (overload 3) {#Callins:WorldTooltip-3}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3916-L3920" target="_blank">source</a>]

```lua
Callins:WorldTooltip("selection") -> string
```

**Parameters**

- `type` `"selection"`

**Returns**

- `tooltip` `string`

### Callins:MapDrawCmd {#Callins:MapDrawCmd}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3964-L3972" target="_blank">source</a>]

```lua
Callins:MapDrawCmd(PlayerID, "point", number, number, number, string) -> nil
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `type` `"point"`
- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `label` `string`

### Callins:MapDrawCmd (overload 1) {#Callins:MapDrawCmd-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3973-L3983" target="_blank">source</a>]

```lua
Callins:MapDrawCmd(PlayerID, "line", number, number, number, number, number, number) -> nil
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `type` `"line"`
- `pos1X` `number`
- `pos1Y` `number`
- `pos1Z` `number`
- `pos2X` `number`
- `pos2Y` `number`
- `pos2Z` `number`

### Callins:MapDrawCmd (overload 2) {#Callins:MapDrawCmd-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L3984-L3992" target="_blank">source</a>]

```lua
Callins:MapDrawCmd(PlayerID, "erase", number, number, number, number) -> nil
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `type` `"erase"`
- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `radius` `number`

### Callins:GameSetup {#Callins:GameSetup}
*function*

Fired when the pregame stage is reached

Pregame is the stage where player readiness is managed before a game starts.
Game only starts once all players are ready.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4067-L4078" target="_blank">source</a>]

```lua
Callins:GameSetup(READY_MESSAGE, boolean, table<PlayerID,READY_STATE>) -> boolean?, boolean?
```

**Parameters**

- `state` [`READY_MESSAGE`](READY_MESSAGE.md#READY_MESSAGE) — the current message the engine would display to the player
- `ready` `boolean` — whether the player is currently ready or not
- `playerStates` `table<PlayerID,READY_STATE>` — indexed by playerID

**Returns**

- `gameHandled` `boolean?` — disables the engine ui when true
- `newReady` `boolean?` — whether the player is ready (ignored unless `gameHandled = true`)

### Callins:RecvSkirmishAIMessage {#Callins:RecvSkirmishAIMessage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4121-L4125" target="_blank">source</a>]

```lua
Callins:RecvSkirmishAIMessage(TeamID, string) -> nil
```

**Parameters**

- `aiTeam` [`TeamID`](Aliases.md#TeamID)
- `dataStr` `string`

### Callins:DownloadQueued {#Callins:DownloadQueued}
*function*

Called when a Pr-downloader download is queued

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4166-L4172" target="_blank">source</a>]

```lua
Callins:DownloadQueued(integer, string, string) -> nil
```

**Parameters**

- `id` `integer`
- `name` `string`
- `type` `string`

### Callins:DownloadStarted {#Callins:DownloadStarted}
*function*

Called when a Pr-downloader download is started via VFS.DownloadArchive.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4194-L4198" target="_blank">source</a>]

```lua
Callins:DownloadStarted(integer) -> nil
```

**Parameters**

- `id` `integer`

### Callins:DownloadFinished {#Callins:DownloadFinished}
*function*

Called when a Pr-downloader download finishes successfully.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4217-L4221" target="_blank">source</a>]

```lua
Callins:DownloadFinished(integer) -> nil
```

**Parameters**

- `id` `integer`

### Callins:DownloadFailed {#Callins:DownloadFailed}
*function*

Called when a Pr-downloader download fails to complete.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4240-L4245" target="_blank">source</a>]

```lua
Callins:DownloadFailed(integer, integer) -> nil
```

**Parameters**

- `id` `integer`
- `errorID` `integer`

### Callins:DownloadProgress {#Callins:DownloadProgress}
*function*

Called incrementally during a Pr-downloader download.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4265-L4271" target="_blank">source</a>]

```lua
Callins:DownloadProgress(integer, integer, integer) -> nil
```

**Parameters**

- `id` `integer`
- `downloaded` `integer`
- `total` `integer`
