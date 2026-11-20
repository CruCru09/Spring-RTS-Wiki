---
title: "UnitScriptTable"
tags:
  - Lua-API
---

## UnitScriptTable {#UnitScriptTable}
*class*

**Members**

### UnitScriptTable.CreateScript {#UnitScriptTable.CreateScript}
*function*

Create a Lua unit script for the given unit, replacing any existing script.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1154-L1160" target="_blank">source</a>]

```lua
UnitScriptTable.CreateScript(UnitID, table<string,function>) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `callIns` `table<string,function>`

**Returns**

- `nil`

### UnitScriptTable.UpdateCallIn {#UnitScriptTable.UpdateCallIn}
*function*

Update or remove a callIn on a unit script.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1189-L1196" target="_blank">source</a>]

```lua
UnitScriptTable.UpdateCallIn(UnitID, string, function?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `callin` `string`
- `func` `function?`

**Returns**

- `nil`

### UnitScriptTable.CallAsUnit {#UnitScriptTable.CallAsUnit}
*function*

Execute a function in the context of a unit's script environment.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1221-L1228" target="_blank">source</a>]

```lua
UnitScriptTable.CallAsUnit(UnitID, function, [any, ]*) -> any ...
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `func` `function`
- `...` `any` — arguments passed to func

**Returns**

- `values` `any ...` — returned by func

### UnitScriptTable.GetUnitCOBValue {#UnitScriptTable.GetUnitCOBValue}
*function*

Get a COB/script value for a unit (synced gadget API).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1297-L1304" target="_blank">source</a>]

```lua
UnitScriptTable.GetUnitCOBValue(UnitID, integer, [number, ]*) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `val` `integer` — COB value ID (use COB constants)
- `...` `number` — optional extra args for certain COB values

**Returns**

- `value` `integer`

### UnitScriptTable.GetUnitValue {#UnitScriptTable.GetUnitValue}
*function*

Get a COB/script value. Must be called from within a UnitScript callin.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1317-L1322" target="_blank">source</a>]

```lua
UnitScriptTable.GetUnitValue(integer) -> integer
```

**Parameters**

- `val` `integer` — COB value ID (use COB constants)

**Returns**

- `value` `integer`

### UnitScriptTable.SetUnitCOBValue {#UnitScriptTable.SetUnitCOBValue}
*function*

Set a COB/script value for a unit (synced gadget API).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1354-L1361" target="_blank">source</a>]

```lua
UnitScriptTable.SetUnitCOBValue(UnitID, integer, (integer|boolean)) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `val` `integer` — COB value ID (use COB constants)
- `param` `(integer|boolean)` — value to set

**Returns**

- `nil`

### UnitScriptTable.SetUnitValue {#UnitScriptTable.SetUnitValue}
*function*

Set a COB/script value. Must be called from within a UnitScript callin.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1374-L1380" target="_blank">source</a>]

```lua
UnitScriptTable.SetUnitValue(integer, (integer|boolean)) -> nil
```

**Parameters**

- `val` `integer` — COB value ID (use COB constants)
- `param` `(integer|boolean)` — value to set

**Returns**

- `nil`

### UnitScriptTable.SetPieceVisibility {#UnitScriptTable.SetPieceVisibility}
*function*

Set visibility of a piece. Must be called from within a UnitScript callin.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1391-L1397" target="_blank">source</a>]

```lua
UnitScriptTable.SetPieceVisibility(integer, boolean) -> nil
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `visible` `boolean`

**Returns**

- `nil`

### UnitScriptTable.EmitSfx {#UnitScriptTable.EmitSfx}
*function*

Emit a special effect at a piece. Must be called from within a UnitScript callin.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1415-L1421" target="_blank">source</a>]

```lua
UnitScriptTable.EmitSfx(integer, (integer|string)) -> nil
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `type` `(integer|string)` — SFX type constant or CEG name

**Returns**

- `nil`

### UnitScriptTable.AttachUnit {#UnitScriptTable.AttachUnit}
*function*

Attach a unit to a piece of another unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1438-L1444" target="_blank">source</a>]

```lua
UnitScriptTable.AttachUnit(integer, UnitID) -> nil
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `transporteeID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `nil`

### UnitScriptTable.DropUnit {#UnitScriptTable.DropUnit}
*function*

Drop a transported unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1462-L1467" target="_blank">source</a>]

```lua
UnitScriptTable.DropUnit(UnitID) -> nil
```

**Parameters**

- `transporteeID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `nil`

### UnitScriptTable.Explode {#UnitScriptTable.Explode}
*function*

Explode a piece with the given flags.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1485-L1491" target="_blank">source</a>]

```lua
UnitScriptTable.Explode(integer, integer) -> nil
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `flags` `integer` — SFX explosion flags (bitfield)

**Returns**

- `nil`

### UnitScriptTable.ShowFlare {#UnitScriptTable.ShowFlare}
*function*

Show a flare at a piece.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1506-L1511" target="_blank">source</a>]

```lua
UnitScriptTable.ShowFlare(integer) -> nil
```

**Parameters**

- `piece` `integer` — 1-indexed piece number

**Returns**

- `nil`

### UnitScriptTable.Spin {#UnitScriptTable.Spin}
*function*

Start spinning a piece around an axis.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1525-L1533" target="_blank">source</a>]

```lua
UnitScriptTable.Spin(integer, integer, number, number?) -> nil
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `axis` `integer` — axis (1=x, 2=y, 3=z)
- `speed` `number` — angular speed in radians/frame
- `accel` `number?` — angular acceleration (Default: `0`, instant)

**Returns**

- `nil`

### UnitScriptTable.StopSpin {#UnitScriptTable.StopSpin}
*function*

Stop spinning a piece.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1551-L1558" target="_blank">source</a>]

```lua
UnitScriptTable.StopSpin(integer, integer, number?) -> nil
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `axis` `integer` — axis (1=x, 2=y, 3=z)
- `decel` `number?` — angular deceleration (Default: `0`, instant)

**Returns**

- `nil`

### UnitScriptTable.Turn {#UnitScriptTable.Turn}
*function*

Turn a piece to an angle. If speed is 0 or omitted, turns instantly.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1575-L1583" target="_blank">source</a>]

```lua
UnitScriptTable.Turn(integer, integer, number, number?) -> nil
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `axis` `integer` — axis (1=x, 2=y, 3=z)
- `destination` `number` — target angle in radians
- `speed` `number?` — angular speed (Default: `0`, instant)

**Returns**

- `nil`

### UnitScriptTable.Move {#UnitScriptTable.Move}
*function*

Move a piece along an axis. If speed is 0 or omitted, moves instantly.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1607-L1615" target="_blank">source</a>]

```lua
UnitScriptTable.Move(integer, integer, number, number?) -> nil
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `axis` `integer` — axis (1=x, 2=y, 3=z)
- `destination` `number` — target position
- `speed` `number?` — movement speed (Default: `0`, instant)

**Returns**

- `nil`

### UnitScriptTable.Scale {#UnitScriptTable.Scale}
*function*

Scale a piece. If speed is 0 or omitted, scales instantly.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1638-L1645" target="_blank">source</a>]

```lua
UnitScriptTable.Scale(integer, number, number?) -> nil
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `destination` `number` — target scale factor
- `speed` `number?` — scaling speed (Default: `0`, instant)

**Returns**

- `nil`

### UnitScriptTable.IsInTurn {#UnitScriptTable.IsInTurn}
*function*

Check if a piece is currently turning.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1738-L1744" target="_blank">source</a>]

```lua
UnitScriptTable.IsInTurn(integer, integer) -> boolean
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `axis` `integer` — axis (1=x, 2=y, 3=z)

**Returns**

- `boolean`

### UnitScriptTable.IsInMove {#UnitScriptTable.IsInMove}
*function*

Check if a piece is currently moving.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1752-L1758" target="_blank">source</a>]

```lua
UnitScriptTable.IsInMove(integer, integer) -> boolean
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `axis` `integer` — axis (1=x, 2=y, 3=z)

**Returns**

- `boolean`

### UnitScriptTable.IsInSpin {#UnitScriptTable.IsInSpin}
*function*

Check if a piece is currently spinning.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1766-L1772" target="_blank">source</a>]

```lua
UnitScriptTable.IsInSpin(integer, integer) -> boolean
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `axis` `integer` — axis (1=x, 2=y, 3=z)

**Returns**

- `boolean`

### UnitScriptTable.IsInScale {#UnitScriptTable.IsInScale}
*function*

Check if a piece is currently scaling.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1779-L1784" target="_blank">source</a>]

```lua
UnitScriptTable.IsInScale(integer) -> boolean
```

**Parameters**

- `piece` `integer` — 1-indexed piece number

**Returns**

- `boolean`

### UnitScriptTable.WaitForTurn {#UnitScriptTable.WaitForTurn}
*function*

Check whether the calling thread needs to wait for a turn to finish.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1817-L1823" target="_blank">source</a>]

```lua
UnitScriptTable.WaitForTurn(integer, integer) -> boolean
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `axis` `integer` — axis (1=x, 2=y, 3=z)

**Returns**

- `needsWait` `boolean`

### UnitScriptTable.WaitForMove {#UnitScriptTable.WaitForMove}
*function*

Check whether the calling thread needs to wait for a move to finish.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1831-L1837" target="_blank">source</a>]

```lua
UnitScriptTable.WaitForMove(integer, integer) -> boolean
```

**Parameters**

- `piece` `integer` — 1-indexed piece number
- `axis` `integer` — axis (1=x, 2=y, 3=z)

**Returns**

- `needsWait` `boolean`

### UnitScriptTable.WaitForScale {#UnitScriptTable.WaitForScale}
*function*

Check whether the calling thread needs to wait for a scale to finish.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1844-L1849" target="_blank">source</a>]

```lua
UnitScriptTable.WaitForScale(integer) -> boolean
```

**Parameters**

- `piece` `integer` — 1-indexed piece number

**Returns**

- `needsWait` `boolean`

### UnitScriptTable.SetDeathScriptFinished {#UnitScriptTable.SetDeathScriptFinished}
*function*

Signal that the Killed callin has finished. Must be called from Killed.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1869-L1874" target="_blank">source</a>]

```lua
UnitScriptTable.SetDeathScriptFinished(integer?) -> nil
```

**Parameters**

- `wreckLevel` `integer?` — (Default: `-1`)

**Returns**

- `nil`

### UnitScriptTable.GetPieceTranslation {#UnitScriptTable.GetPieceTranslation}
*function*

Get the local translation of a piece relative to its rest position.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1892-L1899" target="_blank">source</a>]

```lua
UnitScriptTable.GetPieceTranslation(integer) -> number, number, number
```

**Parameters**

- `piece` `integer` — 1-indexed piece number

**Returns**

- `x` `number`
- `y` `number`
- `z` `number`

### UnitScriptTable.GetPieceRotation {#UnitScriptTable.GetPieceRotation}
*function*

Get the rotation of a piece in radians.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1911-L1918" target="_blank">source</a>]

```lua
UnitScriptTable.GetPieceRotation(integer) -> number, number, number
```

**Parameters**

- `piece` `integer` — 1-indexed piece number

**Returns**

- `rx` `number`
- `ry` `number`
- `rz` `number`

### UnitScriptTable.GetPieceScale {#UnitScriptTable.GetPieceScale}
*function*

Get the scale factor of a piece.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1929-L1934" target="_blank">source</a>]

```lua
UnitScriptTable.GetPieceScale(integer) -> number
```

**Parameters**

- `piece` `integer` — 1-indexed piece number

**Returns**

- `scale` `number`

### UnitScriptTable.GetPiecePosDir {#UnitScriptTable.GetPiecePosDir}
*function*

Get the world-space emit position and direction of a piece.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1947-L1957" target="_blank">source</a>]

```lua
UnitScriptTable.GetPiecePosDir(integer) -> number, number, number, number, number, number
```

**Parameters**

- `piece` `integer` — 1-indexed piece number

**Returns**

- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `dirX` `number`
- `dirY` `number`
- `dirZ` `number`

### UnitScriptTable.GetActiveUnitID {#UnitScriptTable.GetActiveUnitID}
*function*

Get the unit ID of the currently executing unit script.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Sim/Units/Scripts/LuaUnitScript.cpp#L1980-L1984" target="_blank">source</a>]

```lua
UnitScriptTable.GetActiveUnitID() -> UnitID?
```

**Returns**

- `unitID` `UnitID?`
