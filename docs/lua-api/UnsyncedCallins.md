---
title: "UnsyncedCallins"
tags:
  - Lua-API
---

## UnsyncedCallins {#UnsyncedCallins}
*class*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L167-L170" target="_blank">source</a>]

Functions called by the Engine (Unsynced).

**Members**

### UnsyncedCallins:RecvFromSynced {#UnsyncedCallins:RecvFromSynced}
*function*

Receives data sent via `SendToUnsynced` callout.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L178-L182" target="_blank">source</a>]

```lua
UnsyncedCallins:RecvFromSynced([any, ]*) -> nil
```

**Parameters**

- `...` `any`

### UnsyncedCallins:DrawUnit {#UnsyncedCallins:DrawUnit}
*function*

For custom rendering of units

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L209-L216" target="_blank">source</a>]

**Deprecated:** 

```lua
UnsyncedCallins:DrawUnit(UnitID, integer) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `drawMode` `integer`

**Returns**

- `suppressEngineDraw` `boolean`

### UnsyncedCallins:DrawFeature {#UnsyncedCallins:DrawFeature}
*function*

For custom rendering of features

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L246-L253" target="_blank">source</a>]

**Deprecated:** 

```lua
UnsyncedCallins:DrawFeature(FeatureID, integer) -> boolean
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `drawMode` `integer`

**Returns**

- `suppressEngineDraw` `boolean`

### UnsyncedCallins:DrawShield {#UnsyncedCallins:DrawShield}
*function*

For custom rendering of shields.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L282-L290" target="_blank">source</a>]

**Deprecated:** 

```lua
UnsyncedCallins:DrawShield(UnitID, integer, integer) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `weaponID` `integer`
- `drawMode` `integer`

**Returns**

- `suppressEngineDraw` `boolean`

### UnsyncedCallins:DrawProjectile {#UnsyncedCallins:DrawProjectile}
*function*

For custom rendering of weapon (& other) projectiles

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L321-L328" target="_blank">source</a>]

**Deprecated:** 

```lua
UnsyncedCallins:DrawProjectile(ProjectileID, integer) -> boolean
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `drawMode` `integer`

**Returns**

- `suppressEngineDraw` `boolean`

### UnsyncedCallins:DrawMaterial {#UnsyncedCallins:DrawMaterial}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandleSynced.cpp#L359-L366" target="_blank">source</a>]

**Deprecated:** 

```lua
UnsyncedCallins:DrawMaterial(integer, integer) -> boolean
```

**Parameters**

- `uuid` `integer`
- `drawMode` `integer`

**Returns**

- `suppressEngineDraw` `boolean`
