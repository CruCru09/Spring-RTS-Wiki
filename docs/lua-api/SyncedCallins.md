---
title: "SyncedCallins"
tags:
  - Lua-API
---

## SyncedCallins {#SyncedCallins}
*class*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L552-L555" target="_blank">source</a>]

Functions called by the Engine (Synced).

**Members**

### SyncedCallins:CommandFallback {#SyncedCallins:CommandFallback}
*function*

Called when the unit reaches an unknown command in its queue (i.e. one not handled by the engine).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L573-L584" target="_blank">source</a>]

```lua
SyncedCallins:CommandFallback(UnitID, UnitDefID, TeamID, integer, number[], CommandOptions, integer) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `cmdID` `integer`
- `cmdParams` `number[]`
- `cmdOptions` [`CommandOptions`](CommandOptions.md#CommandOptions)
- `cmdTag` `integer`

**Returns**

- `removeCmd` `boolean` — whether to remove the command from the queue

### SyncedCallins:AllowCommand {#SyncedCallins:AllowCommand}
*function*

Called when the command is given, before the unit's queue is altered.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L606-L622" target="_blank">source</a>]

The queue remains untouched when a command is blocked, whether it would be queued or replace the queue.

```lua
SyncedCallins:AllowCommand(UnitID, UnitDefID, TeamID, integer, number[], CommandOptions, integer, boolean, boolean) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `cmdID` `integer`
- `cmdParams` `number[]`
- `cmdOptions` [`CommandOptions`](CommandOptions.md#CommandOptions)
- `cmdTag` `integer`
- `synced` `boolean`
- `fromLua` `boolean`

**Returns**

- `allowCmd` `boolean` — whether it should be let into the queue.

### SyncedCallins:AllowUnitCreation {#SyncedCallins:AllowUnitCreation}
*function*

Called just before unit is created.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L650-L662" target="_blank">source</a>]

```lua
SyncedCallins:AllowUnitCreation(UnitDefID, UnitID, TeamID, number, number, number, FacingInteger) -> boolean, boolean
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `builderID` [`UnitID`](Aliases.md#UnitID)
- `builderTeam` [`TeamID`](Aliases.md#TeamID)
- `x` `number`
- `y` `number`
- `z` `number`
- `facing` [`FacingInteger`](Aliases.md#FacingInteger)

**Returns**

- `allow` `boolean`
- `dropOrder` `boolean`

### SyncedCallins:AllowUnitTransfer {#SyncedCallins:AllowUnitTransfer}
*function*

Called just before a unit is transferred to a different team.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L698-L707" target="_blank">source</a>]

```lua
SyncedCallins:AllowUnitTransfer(UnitID, UnitDefID, TeamID, TeamID, boolean) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `oldTeam` [`TeamID`](Aliases.md#TeamID)
- `newTeam` [`TeamID`](Aliases.md#TeamID)
- `capture` `boolean`

**Returns**

- `allow` `boolean` — whether or not the transfer is permitted.

### SyncedCallins:AllowUnitBuildStep {#SyncedCallins:AllowUnitBuildStep}
*function*

Called just before a unit progresses its build percentage.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L735-L744" target="_blank">source</a>]

```lua
SyncedCallins:AllowUnitBuildStep(UnitID, TeamID, UnitID, UnitDefID, number) -> boolean
```

**Parameters**

- `builderID` [`UnitID`](Aliases.md#UnitID)
- `builderTeam` [`TeamID`](Aliases.md#TeamID)
- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `part` `number`

**Returns**

- `allow` `boolean` — whether or not the build makes progress.

### SyncedCallins:AllowUnitCaptureStep {#SyncedCallins:AllowUnitCaptureStep}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L772-L781" target="_blank">source</a>]

```lua
SyncedCallins:AllowUnitCaptureStep(UnitID, TeamID, UnitID, UnitDefID, number) -> boolean
```

**Parameters**

- `builderID` [`UnitID`](Aliases.md#UnitID)
- `builderTeam` [`TeamID`](Aliases.md#TeamID)
- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `part` `number`

**Returns**

- `allow` `boolean` — whether or not the capture makes progress.

### SyncedCallins:AllowUnitTransport {#SyncedCallins:AllowUnitTransport}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L809-L819" target="_blank">source</a>]

```lua
SyncedCallins:AllowUnitTransport(UnitID, UnitDefID, TeamID, UnitID, UnitDefID, TeamID) -> boolean
```

**Parameters**

- `transporterID` [`UnitID`](Aliases.md#UnitID)
- `transporterUnitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `transporterTeam` [`TeamID`](Aliases.md#TeamID)
- `transporteeID` [`UnitID`](Aliases.md#UnitID)
- `transporteeUnitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `transporteeTeam` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `allow` `boolean` — whether or not the transport is allowed

### SyncedCallins:AllowUnitTransportLoad {#SyncedCallins:AllowUnitTransportLoad}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L847-L860" target="_blank">source</a>]

```lua
SyncedCallins:AllowUnitTransportLoad(UnitID, UnitDefID, TeamID, UnitID, UnitDefID, TeamID, number, number, number) -> boolean
```

**Parameters**

- `transporterID` [`UnitID`](Aliases.md#UnitID)
- `transporterUnitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `transporterTeam` [`TeamID`](Aliases.md#TeamID)
- `transporteeID` [`UnitID`](Aliases.md#UnitID)
- `transporteeUnitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `transporteeTeam` [`TeamID`](Aliases.md#TeamID)
- `x` `number`
- `y` `number`
- `z` `number`

**Returns**

- `allow` `boolean` — whether or not the transport load is allowed

### SyncedCallins:AllowUnitTransportUnload {#SyncedCallins:AllowUnitTransportUnload}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L897-L910" target="_blank">source</a>]

```lua
SyncedCallins:AllowUnitTransportUnload(UnitID, UnitDefID, TeamID, UnitID, UnitDefID, TeamID, number, number, number) -> boolean
```

**Parameters**

- `transporterID` [`UnitID`](Aliases.md#UnitID)
- `transporterUnitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `transporterTeam` [`TeamID`](Aliases.md#TeamID)
- `transporteeID` [`UnitID`](Aliases.md#UnitID)
- `transporteeUnitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `transporteeTeam` [`TeamID`](Aliases.md#TeamID)
- `x` `number`
- `y` `number`
- `z` `number`

**Returns**

- `allow` `boolean` — whether or not the transport unload is allowed

### SyncedCallins:AllowUnitCloak {#SyncedCallins:AllowUnitCloak}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L945-L951" target="_blank">source</a>]

```lua
SyncedCallins:AllowUnitCloak(UnitID, UnitID?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `enemyID` `UnitID?`

**Returns**

- `allow` `boolean` — whether unit is allowed to cloak

### SyncedCallins:AllowUnitDecloak {#SyncedCallins:AllowUnitDecloak}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L981-L988" target="_blank">source</a>]

```lua
SyncedCallins:AllowUnitDecloak(UnitID, ObjectID?, integer?) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `objectID` `ObjectID?`
- `weaponNum` `integer?`

**Returns**

- `allow` `boolean` — whether unit is allowed to decloak

### SyncedCallins:AllowUnitKamikaze {#SyncedCallins:AllowUnitKamikaze}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1025-L1031" target="_blank">source</a>]

```lua
SyncedCallins:AllowUnitKamikaze(UnitID, UnitID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `targetID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `allow` `boolean` — whether unit is allowed to selfd

### SyncedCallins:AllowFeatureCreation {#SyncedCallins:AllowFeatureCreation}
*function*

Called just before feature is created.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1055-L1064" target="_blank">source</a>]

```lua
SyncedCallins:AllowFeatureCreation(FeatureDefID, TeamID, number, number, number) -> boolean
```

**Parameters**

- `featureDefID` [`FeatureDefID`](Aliases.md#FeatureDefID)
- `teamID` [`TeamID`](Aliases.md#TeamID)
- `x` `number`
- `y` `number`
- `z` `number`

**Returns**

- `allow` `boolean` — whether or not the creation is permitted

### SyncedCallins:AllowFeatureBuildStep {#SyncedCallins:AllowFeatureBuildStep}
*function*

Called just before a feature changes its build percentage.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1092-L1109" target="_blank">source</a>]

Note that this is also called for resurrecting features, and for refilling features with resources before resurrection.
On reclaim the part values are negative, and on refill and resurrect they are positive.
Part is the percentage the feature be built or reclaimed per frame.
Eg. for a 30 workertime builder, that's a build power of 1 per frame.
For a 50 buildtime feature reclaimed by this builder, part will be 100/-50(/1) = -2%, or -0.02 numerically.

```lua
SyncedCallins:AllowFeatureBuildStep(UnitID, TeamID, FeatureID, FeatureDefID, number) -> boolean
```

**Parameters**

- `builderID` [`UnitID`](Aliases.md#UnitID)
- `builderTeam` [`TeamID`](Aliases.md#TeamID)
- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `featureDefID` [`FeatureDefID`](Aliases.md#FeatureDefID)
- `part` `number`

**Returns**

- `allow` `boolean` — whether or not the change is permitted

### SyncedCallins:AllowResourceLevel {#SyncedCallins:AllowResourceLevel}
*function*

Called when a team sets the sharing level of a resource.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1137-L1144" target="_blank">source</a>]

```lua
SyncedCallins:AllowResourceLevel(TeamID, string, number) -> boolean
```

**Parameters**

- `teamID` [`TeamID`](Aliases.md#TeamID)
- `res` `string`
- `level` `number`

**Returns**

- `allow` `boolean` — whether or not the sharing level is permitted

### SyncedCallins:AllowResourceTransfer {#SyncedCallins:AllowResourceTransfer}
*function*

Called just before resources are transferred between players.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1170-L1178" target="_blank">source</a>]

```lua
SyncedCallins:AllowResourceTransfer(TeamID, TeamID, string, number) -> boolean
```

**Parameters**

- `oldTeamID` [`TeamID`](Aliases.md#TeamID)
- `newTeamID` [`TeamID`](Aliases.md#TeamID)
- `res` `string`
- `amount` `number`

**Returns**

- `allow` `boolean` — whether or not the transfer is permitted.

### SyncedCallins:ResourceExcess {#SyncedCallins:ResourceExcess}
*function*

Called when excess resources are added.
Accumulates all excesses within a single gameframe.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1204-L1210" target="_blank">source</a>]

```lua
SyncedCallins:ResourceExcess(table) -> boolean
```

**Parameters**

- `excesses` `table`

**Returns**

- `handled` `boolean` — whether or not Lua handled the event

### SyncedCallins:AllowDirectUnitControl {#SyncedCallins:AllowDirectUnitControl}
*function*

Determines if this unit can be controlled directly in FPS view.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1241-L1249" target="_blank">source</a>]

```lua
SyncedCallins:AllowDirectUnitControl(UnitID, UnitDefID, TeamID, PlayerID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `playerID` [`PlayerID`](Aliases.md#PlayerID)

**Returns**

- `allow` `boolean`

### SyncedCallins:AllowBuilderHoldFire {#SyncedCallins:AllowBuilderHoldFire}
*function*

Called when a construction unit wants to "use his nano beams".

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1276-L1293" target="_blank">source</a>]

```lua
SyncedCallins:AllowBuilderHoldFire(UnitID, UnitDefID, unknown) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `action` `unknown`

**Returns**

- `actionAllowed` `boolean`

### SyncedCallins:AllowStartPosition {#SyncedCallins:AllowStartPosition}
*function*

Whether a start position should be allowed

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1319-L1344" target="_blank">source</a>]

clamped{X,Y,Z} are the coordinates clamped into start-boxes, raw is where player tried to place their marker.

The readyState can be any one of:

0 - player picked a position,
1 - player clicked ready,
2 - player pressed ready OR the game was force-started (player did not click ready, but is now forcibly readied) or
3 - the player failed to load.
The default 'failed to choose' start-position is the north-west point of their startbox, or (0,0,0) if they do not have a startbox.

```lua
SyncedCallins:AllowStartPosition(PlayerID, TeamID, integer, number, number, number, number, number, number) -> boolean
```

**Parameters**

- `playerID` [`PlayerID`](Aliases.md#PlayerID)
- `teamID` [`TeamID`](Aliases.md#TeamID)
- `readyState` `integer`
- `clampedX` `number`
- `clampedY` `number`
- `clampedZ` `number`
- `rawX` `number`
- `rawY` `number`
- `rawZ` `number`

**Returns**

- `allow` `boolean`

### SyncedCallins:MoveCtrlNotify {#SyncedCallins:MoveCtrlNotify}
*function*

Enable both Spring.MoveCtrl.SetCollideStop and Spring.MoveCtrl.SetTrackGround to enable this call-in.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1377-L1387" target="_blank">source</a>]

```lua
SyncedCallins:MoveCtrlNotify(UnitID, UnitDefID, TeamID, integer) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `data` `integer` — was supposed to indicate the type of notification but currently never has a value other than 1 ("unit hit the ground").

**Returns**

- `engineControl` `boolean` — whether or not the unit should remain script-controlled (false) or return to engine controlled movement (true).

### SyncedCallins:TerraformComplete {#SyncedCallins:TerraformComplete}
*function*

Called when pre-building terrain levelling terraforms are completed (c.f. levelGround)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1415-L1425" target="_blank">source</a>]

```lua
SyncedCallins:TerraformComplete(UnitID, UnitDefID, TeamID, UnitID, UnitDefID, TeamID) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `buildUnitID` [`UnitID`](Aliases.md#UnitID)
- `buildUnitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `buildUnitTeam` [`TeamID`](Aliases.md#TeamID)

**Returns**

- `stop` `boolean` — if true the current build order is terminated

### SyncedCallins:UnitPreDamaged {#SyncedCallins:UnitPreDamaged}
*function*

Called before damage is applied to the unit, allows fine control over how much damage and impulse is applied.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1473-L1496" target="_blank">source</a>]

Called after every damage modification (even `HitByWeaponId`) but before the damage is applied

expects two numbers returned by lua code:
1st is stored under *newDamage if newDamage != NULL
2nd is stored under *impulseMult if impulseMult != NULL

```lua
SyncedCallins:UnitPreDamaged(UnitID, UnitDefID, TeamID, number, boolean, WeaponDefID?, ProjectileID?, UnitID?, UnitDefID?, TeamID?) -> number, number
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `unitTeam` [`TeamID`](Aliases.md#TeamID)
- `damage` `number`
- `paralyzer` `boolean`
- `weaponDefID` `WeaponDefID?` — Synced Only
- `projectileID` `ProjectileID?` — Synced Only
- `attackerID` `UnitID?` — Synced Only
- `attackerDefID` `UnitDefID?` — Synced Only
- `attackerTeam` `TeamID?` — Synced Only

**Returns**

- `newDamage` `number`
- `impulseMult` `number`

### SyncedCallins:FeaturePreDamaged {#SyncedCallins:FeaturePreDamaged}
*function*

Called before damage is applied to the feature.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1570-L1587" target="_blank">source</a>]

Allows fine control over how much damage and impulse is applied.

```lua
SyncedCallins:FeaturePreDamaged(FeatureID, FeatureDefID, TeamID, number, WeaponDefID, ProjectileID, UnitID, UnitDefID, TeamID) -> number, number
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

**Returns**

- `newDamage` `number`
- `impulseMult` `number`

### SyncedCallins:ShieldPreDamaged {#SyncedCallins:ShieldPreDamaged}
*function*

Called before any engine shield-vs-projectile logic executes.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1653-L1672" target="_blank">source</a>]

```lua
SyncedCallins:ShieldPreDamaged(ProjectileID, UnitID, integer, UnitID, boolean, integer?, UnitID?, number, number, number, number, number, number) -> boolean
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID) — `-1` when the weapon type is `BeamLaser` or `LightningCannon`
- `projectileOwnerID` [`UnitID`](Aliases.md#UnitID) — `-1` when the weapon type is `BeamLaser` or `LightningCannon`
- `shieldWeaponNum` `integer`
- `shieldCarrierID` [`UnitID`](Aliases.md#UnitID)
- `bounceProjectile` `boolean`
- `beamEmitterWeaponNum` `integer?` — present only when the weapon type is `BeamLaser` or `LightningCannon`
- `beamEmitterUnitID` `UnitID?` — present only when the weapon type is `BeamLaser` or `LightningCannon`
- `startX` `number`
- `startY` `number`
- `startZ` `number`
- `hitX` `number`
- `hitY` `number`
- `hitZ` `number`

**Returns**

- `handle` `boolean` — if true the gadget handles the collision event and the engine does not remove the projectile

### SyncedCallins:AllowWeaponTargetCheck {#SyncedCallins:AllowWeaponTargetCheck}
*function*

Determines if this weapon can automatically generate targets itself. See also commandFire weaponDef tag.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1733-L1748" target="_blank">source</a>]

Only called for weaponDefIDs registered via [Script.SetWatchAllowTarget](Script.md#Script.SetWatchAllowTarget) or [Script.SetWatchWeapon](Script.md#Script.SetWatchWeapon).

**See:** [Script.SetWatchWeapon](Script.md#Script.SetWatchWeapon)

```lua
SyncedCallins:AllowWeaponTargetCheck(UnitID, integer, WeaponDefID) -> boolean, boolean
```

**Parameters**

- `attackerID` [`UnitID`](Aliases.md#UnitID)
- `attackerWeaponNum` `integer`
- `attackerWeaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)

**Returns**

- `allowCheck` `boolean`
- `ignoreCheck` `boolean`

### SyncedCallins:AllowWeaponTarget {#SyncedCallins:AllowWeaponTarget}
*function*

Controls blocking of a specific target from being considered during a weapon's periodic auto-targeting sweep.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1780-L1797" target="_blank">source</a>]

Only called for weaponDefIDs registered via [Script.SetWatchAllowTarget](Script.md#Script.SetWatchAllowTarget) or [Script.SetWatchWeapon](Script.md#Script.SetWatchWeapon).

**See:** [Script.SetWatchWeapon](Script.md#Script.SetWatchWeapon)

```lua
SyncedCallins:AllowWeaponTarget(UnitID, UnitID, integer, WeaponDefID, number) -> boolean, number
```

**Parameters**

- `attackerID` [`UnitID`](Aliases.md#UnitID)
- `targetID` [`UnitID`](Aliases.md#UnitID)
- `attackerWeaponNum` `integer`
- `attackerWeaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)
- `defPriority` `number`

**Returns**

- `allowed` `boolean`
- `newPriority` `number` — The new priority for this target (if you don't want to change it, return defPriority). Lower priority targets are targeted first.

### SyncedCallins:AllowWeaponInterceptTarget {#SyncedCallins:AllowWeaponInterceptTarget}
*function*

Controls blocking of a specific intercept target from being considered during an interceptor weapon's periodic auto-targeting sweep.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L1850-L1864" target="_blank">source</a>]

Only called for weaponDefIDs registered via [Script.SetWatchAllowTarget](Script.md#Script.SetWatchAllowTarget) or [Script.SetWatchWeapon](Script.md#Script.SetWatchWeapon).

**See:** [Script.SetWatchWeapon](Script.md#Script.SetWatchWeapon)

```lua
SyncedCallins:AllowWeaponInterceptTarget(UnitID, integer, ProjectileID) -> boolean
```

**Parameters**

- `interceptorUnitID` [`UnitID`](Aliases.md#UnitID)
- `interceptorWeaponID` `integer`
- `targetProjectileID` [`ProjectileID`](Aliases.md#ProjectileID)

**Returns**

- `allowed` `boolean`

### SyncedCallins.SendToUnsynced {#SyncedCallins.SendToUnsynced}
*function*

Invoke [UnsyncedCallins:RecvFromSynced](UnsyncedCallins.md#UnsyncedCallins:RecvFromSynced) callin with the given arguments.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2020-L2030" target="_blank">source</a>]

**See:** [UnsyncedCallins:RecvFromSynced](UnsyncedCallins.md#UnsyncedCallins:RecvFromSynced)

```lua
SyncedCallins.SendToUnsynced([(boolean|number|string|table)?, ]*) -> nil
```

**Parameters**

- `...` `(boolean|number|string|table)?` — Arguments. Typically the first argument is the name of a function to call.

Argument tables will be recursively copied and stripped of unsupported types and metatables.
