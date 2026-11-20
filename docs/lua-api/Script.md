---
title: "Script"
tags:
  - Lua-API
---

## Script {#Script}
*table*

**Members**

### Script.Kill {#Script.Kill}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L232-L235" target="_blank">source</a>]

```lua
Script.Kill(string?) -> nil
```

**Parameters**

- `killMessage` `string?` — Kill message.

### Script.GetName {#Script.GetName}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4412-L4415" target="_blank">source</a>]

```lua
Script.GetName() -> string
```

**Returns**

- `name` `string`

### Script.GetSynced {#Script.GetSynced}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4423-L4426" target="_blank">source</a>]

```lua
Script.GetSynced() -> boolean
```

**Returns**

- `synced` `boolean`

### Script.GetFullCtrl {#Script.GetFullCtrl}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4434-L4437" target="_blank">source</a>]

```lua
Script.GetFullCtrl() -> boolean
```

**Returns**

- `fullCtrl` `boolean`

### Script.GetFullRead {#Script.GetFullRead}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4445-L4448" target="_blank">source</a>]

```lua
Script.GetFullRead() -> boolean
```

**Returns**

- `fullRead` `boolean`

### Script.GetCtrlTeam {#Script.GetCtrlTeam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4456-L4459" target="_blank">source</a>]

```lua
Script.GetCtrlTeam() -> TeamID
```

**Returns**

- `teamID` [`TeamID`](Aliases.md#TeamID)

### Script.GetReadTeam {#Script.GetReadTeam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4467-L4470" target="_blank">source</a>]

```lua
Script.GetReadTeam() -> TeamID
```

**Returns**

- `teamID` [`TeamID`](Aliases.md#TeamID)

### Script.GetReadAllyTeam {#Script.GetReadAllyTeam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4478-L4481" target="_blank">source</a>]

```lua
Script.GetReadAllyTeam() -> AllyTeamID
```

**Returns**

- `allyTeamID` [`AllyTeamID`](Aliases.md#AllyTeamID)

### Script.GetSelectTeam {#Script.GetSelectTeam}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4489-L4492" target="_blank">source</a>]

```lua
Script.GetSelectTeam() -> TeamID
```

**Returns**

- `teamID` [`TeamID`](Aliases.md#TeamID)

### Script.GetGlobal {#Script.GetGlobal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4500-L4503" target="_blank">source</a>]

```lua
Script.GetGlobal() -> integer?
```

**Returns**

- `global` `integer?`

### Script.GetRegistry {#Script.GetRegistry}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4514-L4517" target="_blank">source</a>]

```lua
Script.GetRegistry() -> integer?
```

**Returns**

- `registry` `integer?`

### Script.DelayByFrames {#Script.DelayByFrames}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4534-L4538" target="_blank">source</a>]

```lua
Script.DelayByFrames(integer, unknown) -> nil
```

**Parameters**

- `frameDelay` `integer`
- `fun` `unknown`

### Script.UpdateCallIn {#Script.UpdateCallIn}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4584-L4588" target="_blank">source</a>]

```lua
Script.UpdateCallIn(string) -> nil
```

**Parameters**

- `name` `string`

**Returns**

- `nil`

### Script.GetWatchUnit {#Script.GetWatchUnit}
*function*

Query whether any callins are registered for a unitDefID.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2192-L2200" target="_blank">source</a>]

**See:** [Script.SetWatchUnit](Script.md#Script.SetWatchUnit)

```lua
Script.GetWatchUnit(UnitDefID) -> boolean
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)

**Returns**

- `watched` `boolean` — Watch status.

### Script.GetWatchFeature {#Script.GetWatchFeature}
*function*

Query whether any callins are registered for a featureDefID.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2205-L2213" target="_blank">source</a>]

**See:** [Script.SetWatchFeature](Script.md#Script.SetWatchFeature)

```lua
Script.GetWatchFeature(FeatureDefID) -> boolean
```

**Parameters**

- `featureDefID` [`FeatureDefID`](Aliases.md#FeatureDefID)

**Returns**

- `watched` `boolean` — `true` if callins are registered, otherwise `false`.

### Script.GetWatchWeapon {#Script.GetWatchWeapon}
*function*

Query whether any callins are registered for a weaponDefID.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2218-L2231" target="_blank">source</a>]

Same as calling:
```lua
Script.GetWatchExplosion(weaponDefID) or Script.GetWatchProjectile(weaponDefID) or Script.GetWatchAllowTarget(weaponDefID)
```

**See:** [Script.SetWatchWeapon](Script.md#Script.SetWatchWeapon)

```lua
Script.GetWatchWeapon(WeaponDefID) -> boolean
```

**Parameters**

- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)

**Returns**

- `watched` `boolean` — `true` if watch is enabled for any weaponDefID callins.

### Script.GetWatchExplosion {#Script.GetWatchExplosion}
*function*

Query whether explosion callins are registered for a weaponDefID.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2233-L2241" target="_blank">source</a>]

**See:** [Script.SetWatchExplosion](Script.md#Script.SetWatchExplosion)

```lua
Script.GetWatchExplosion(WeaponDefID) -> boolean
```

**Parameters**

- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)

**Returns**

- `watched` `boolean` — `true` if callins are registered, otherwise `false`.

### Script.GetWatchProjectile {#Script.GetWatchProjectile}
*function*

Query whether projectile callins are registered for a weaponDefID.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2247-L2255" target="_blank">source</a>]

**See:** [Script.SetWatchProjectile](Script.md#Script.SetWatchProjectile)

```lua
Script.GetWatchProjectile(WeaponDefID) -> boolean
```

**Parameters**

- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)

**Returns**

- `watched` `boolean` — `true` if callins are registered, otherwise `false`.

### Script.GetWatchAllowTarget {#Script.GetWatchAllowTarget}
*function*

Query whether weapon targeting callins are registered for a weaponDefID.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2260-L2268" target="_blank">source</a>]

**See:** [Script.SetWatchAllowTarget](Script.md#Script.SetWatchAllowTarget)

```lua
Script.GetWatchAllowTarget(WeaponDefID) -> boolean
```

**Parameters**

- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)

**Returns**

- `watched` `boolean` — `true` if callins are registered, otherwise `false`.

### Script.SetWatchUnit {#Script.SetWatchUnit}
*function*

Register or deregister unitDefID for expensive callins.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2273-L2284" target="_blank">source</a>]

**See:** [Callins:UnitMoveFailed](Callins.md#Callins:UnitMoveFailed)

```lua
Script.SetWatchUnit(UnitDefID, boolean) -> nil
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `watch` `boolean` — Whether to register or deregister.

### Script.SetWatchFeature {#Script.SetWatchFeature}
*function*

Register or deregister featureDefID for expensive callins.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2289-L2298" target="_blank">source</a>]

**See:** [Callins:UnitFeatureCollision](Callins.md#Callins:UnitFeatureCollision)

```lua
Script.SetWatchFeature(FeatureDefID, boolean) -> nil
```

**Parameters**

- `featureDefID` [`FeatureDefID`](Aliases.md#FeatureDefID)
- `watch` `boolean` — Whether to register or deregister.

### Script.SetWatchWeapon {#Script.SetWatchWeapon}
*function*

Register or deregister weaponDefID for all expensive callins.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2303-L2324" target="_blank">source</a>]

Equivalent to calling:

```lua
Script.SetWatchExplosion(weaponDefID)
Script.SetWatchProjectile(weaponDefID)
Script.SetWatchAllowTarget(weaponDefID)
```

Generally it's better to use those methods to avoid registering uneeded callins.

**See:** [Script.SetWatchAllowTarget](Script.md#Script.SetWatchAllowTarget)

```lua
Script.SetWatchWeapon(WeaponDefID, boolean) -> nil
```

**Parameters**

- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)
- `watch` `boolean` — Whether to register or deregister.

### Script.SetWatchExplosion {#Script.SetWatchExplosion}
*function*

Register or deregister weaponDefID for explosion callins.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2326-L2335" target="_blank">source</a>]

**See:** [Callins:Explosion](Callins.md#Callins:Explosion)

```lua
Script.SetWatchExplosion(WeaponDefID, boolean) -> nil
```

**Parameters**

- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)
- `watch` `boolean` — Whether to register or deregister.

### Script.SetWatchProjectile {#Script.SetWatchProjectile}
*function*

Register or deregister weaponDefID for expensive projectile callins.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2341-L2351" target="_blank">source</a>]

**See:** [Callins:ProjectileDestroyed](Callins.md#Callins:ProjectileDestroyed)

```lua
Script.SetWatchProjectile(WeaponDefID, boolean) -> nil
```

**Parameters**

- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID) — weaponDefID for weapons or -1 to watch for debris.
- `watch` `boolean` — Whether to register or deregister.

### Script.SetWatchAllowTarget {#Script.SetWatchAllowTarget}
*function*

Register or deregister weaponDefID for weapon targeting callins.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L2356-L2367" target="_blank">source</a>]

**See:** [SyncedCallins:AllowWeaponInterceptTarget](SyncedCallins.md#SyncedCallins:AllowWeaponInterceptTarget)

```lua
Script.SetWatchAllowTarget(WeaponDefID, boolean) -> nil
```

**Parameters**

- `weaponDefID` [`WeaponDefID`](Aliases.md#WeaponDefID)
- `watch` `boolean` — Whether to register or deregister.

### Script.PermitHelperAIs {#Script.PermitHelperAIs}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaRules.cpp#L120-L124" target="_blank">source</a>]

```lua
Script.PermitHelperAIs(boolean) -> nil
```

**Parameters**

- `permit` `boolean`

### Script.IsEngineMinVersion {#Script.IsEngineMinVersion}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUtils.cpp#L529-L535" target="_blank">source</a>]

```lua
Script.IsEngineMinVersion(integer, integer?, integer?) -> boolean
```

**Parameters**

- `minMajorVer` `integer`
- `minMinorVer` `integer?` — (Default: `0`)
- `minCommits` `integer?` — (Default: `0`)

**Returns**

- `satisfiesMin` `boolean` — `true` if the engine version is greater or equal to the specified version, otherwise `false`.

**Fields**

- <span id="Script.NO_ACCESS_TEAM"></span> `Script.NO_ACCESS_TEAM` -1 — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4389-L4389" target="_blank">source</a>]
- <span id="Script.ALL_ACCESS_TEAM"></span> `Script.ALL_ACCESS_TEAM` -2 — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4391-L4391" target="_blank">source</a>]
