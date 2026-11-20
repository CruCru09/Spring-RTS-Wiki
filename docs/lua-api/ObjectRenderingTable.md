---
title: "ObjectRenderingTable"
tags:
  - Lua-API
---

## ObjectRenderingTable {#ObjectRenderingTable}
*class*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L10-L12" target="_blank">source</a>]

**Members**

### ObjectRenderingTable.GetLODCount {#ObjectRenderingTable.GetLODCount}
*function*

Get the number of LOD levels and the current LOD.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L136-L142" target="_blank">source</a>]

```lua
ObjectRenderingTable.GetLODCount(ObjectID) -> integer, integer
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)

**Returns**

- `lodCount` `integer`
- `currentLOD` `integer`

### ObjectRenderingTable.SetLODCount {#ObjectRenderingTable.SetLODCount}
*function*

Set the number of LOD levels.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L158-L164" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetLODCount(ObjectID, integer) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `lodCount` `integer`

**Returns**

- `nil`

### ObjectRenderingTable.SetLODLength {#ObjectRenderingTable.SetLODLength}
*function*

Set the LOD transition length for a given level.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L195-L202" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetLODLength(ObjectID, integer, number) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `lodLevel` `integer`
- `lodLength` `number`

**Returns**

- `nil`

### ObjectRenderingTable.SetLODDistance {#ObjectRenderingTable.SetLODDistance}
*function*

Set the LOD transition distance for a given level (scaled for 45-degree FOV).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L210-L217" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetLODDistance(ObjectID, integer, number) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `lodLevel` `integer`
- `lodDistance` `number`

**Returns**

- `nil`

### ObjectRenderingTable.SetPieceList {#ObjectRenderingTable.SetPieceList}
*function*

Set a display list for a piece at a given LOD and material.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L231-L239" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetPieceList(ObjectID, integer, integer, [any, ]*) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `lodLevel` `integer`
- `piece` `integer`
- `...` `any`

**Returns**

- `nil`

### ObjectRenderingTable.GetMaterial {#ObjectRenderingTable.GetMaterial}
*function*

Get a material reference for a LOD level.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L387-L394" target="_blank">source</a>]

```lua
ObjectRenderingTable.GetMaterial(ObjectID, integer, string) -> userdata
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `lodLevel` `integer`
- `materialName` `string`

**Returns**

- `matRef` `userdata`

### ObjectRenderingTable.SetMaterial {#ObjectRenderingTable.SetMaterial}
*function*

Set a material for a LOD level.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L417-L425" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetMaterial(ObjectID, integer, string, table) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `lodLevel` `integer`
- `materialName` `string`
- `materialTable` `table`

**Returns**

- `nil`

### ObjectRenderingTable.SetMaterialLastLOD {#ObjectRenderingTable.SetMaterialLastLOD}
*function*

Set the last LOD level that uses a given material.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L462-L469" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetMaterialLastLOD(ObjectID, string, integer) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `materialName` `string`
- `lastLOD` `integer`

**Returns**

- `nil`

### ObjectRenderingTable.SetMaterialDisplayLists {#ObjectRenderingTable.SetMaterialDisplayLists}
*function*

Set display lists for a material.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L488-L496" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetMaterialDisplayLists(ObjectID, integer, string, table) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `lodLevel` `integer`
- `materialName` `string`
- `displayListTable` `table`

**Returns**

- `nil`

### ObjectRenderingTable.SetDeferredMaterialUniform {#ObjectRenderingTable.SetDeferredMaterialUniform}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L585-L589" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetDeferredMaterialUniform(ObjectID, [any, ]*) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `...` `any` — uniform values

**Returns**

- `nil`

### ObjectRenderingTable.SetForwardMaterialUniform {#ObjectRenderingTable.SetForwardMaterialUniform}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L591-L595" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetForwardMaterialUniform(ObjectID, [any, ]*) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `...` `any` — uniform values

**Returns**

- `nil`

### ObjectRenderingTable.ClearDeferredMaterialUniform {#ObjectRenderingTable.ClearDeferredMaterialUniform}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L634-L638" target="_blank">source</a>]

```lua
ObjectRenderingTable.ClearDeferredMaterialUniform(ObjectID, [any, ]*) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `...` `any` — uniform indices

**Returns**

- `nil`

### ObjectRenderingTable.ClearForwardMaterialUniform {#ObjectRenderingTable.ClearForwardMaterialUniform}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L640-L644" target="_blank">source</a>]

```lua
ObjectRenderingTable.ClearForwardMaterialUniform(ObjectID, [any, ]*) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)
- `...` `any` — uniform indices

**Returns**

- `nil`

### ObjectRenderingTable.SetUnitLuaDraw {#ObjectRenderingTable.SetUnitLuaDraw}
*function*

Enable or disable custom Lua drawing for a unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L666-L672" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetUnitLuaDraw(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `enable` `boolean`

**Returns**

- `nil`

### ObjectRenderingTable.SetFeatureLuaDraw {#ObjectRenderingTable.SetFeatureLuaDraw}
*function*

Enable or disable custom Lua drawing for a feature.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L679-L685" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetFeatureLuaDraw(FeatureID, boolean) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `enable` `boolean`

**Returns**

- `nil`

### ObjectRenderingTable.SetProjectileLuaDraw {#ObjectRenderingTable.SetProjectileLuaDraw}
*function*

Enable or disable custom Lua drawing for a projectile.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L692-L698" target="_blank">source</a>]

```lua
ObjectRenderingTable.SetProjectileLuaDraw(ProjectileID, boolean) -> nil
```

**Parameters**

- `projectileID` [`ProjectileID`](Aliases.md#ProjectileID)
- `enable` `boolean`

**Returns**

- `nil`

### ObjectRenderingTable.Debug {#ObjectRenderingTable.Debug}
*function*

Print debug info about the object's material data.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaObjectRendering.cpp#L730-L735" target="_blank">source</a>]

```lua
ObjectRenderingTable.Debug(ObjectID) -> nil
```

**Parameters**

- `objectID` [`ObjectID`](Aliases.md#ObjectID)

**Returns**

- `nil`
