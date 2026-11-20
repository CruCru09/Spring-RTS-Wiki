---
title: "MoveCtrl"
tags:
  - Lua-API
---

## MoveCtrl {#MoveCtrl}
*class*

**Members**

### MoveCtrl.IsEnabled {#MoveCtrl.IsEnabled}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L140-L144" target="_blank">source</a>]

```lua
MoveCtrl.IsEnabled(UnitID) -> boolean?
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

**Returns**

- `isEnabled` `boolean?`

### MoveCtrl.Enable {#MoveCtrl.Enable}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L157-L160" target="_blank">source</a>]

```lua
MoveCtrl.Enable(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### MoveCtrl.Disable {#MoveCtrl.Disable}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L173-L176" target="_blank">source</a>]

```lua
MoveCtrl.Disable(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### MoveCtrl.SetTag {#MoveCtrl.SetTag}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L191-L195" target="_blank">source</a>]

```lua
MoveCtrl.SetTag(UnitID, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `tag` `integer`

### MoveCtrl.GetTag {#MoveCtrl.GetTag}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L208-L212" target="_blank">source</a>]

```lua
MoveCtrl.GetTag(integer?) -> integer?
```

**Parameters**

- `tag` `integer?`

**Returns**

- `tag` `integer?` — `nil` if the unit is not using a script move type.

### MoveCtrl.SetProgressState {#MoveCtrl.SetProgressState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L229-L239" target="_blank">source</a>]

```lua
MoveCtrl.SetProgressState(UnitID, (0|1|2|"done"|"active"|"failed")) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `state` `(0|1|2|"done"|"active"|"failed")`

### MoveCtrl.SetExtrapolate {#MoveCtrl.SetExtrapolate}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L279-L283" target="_blank">source</a>]

```lua
MoveCtrl.SetExtrapolate(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `extrapolate` `boolean`

### MoveCtrl.SetPhysics {#MoveCtrl.SetPhysics}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L298-L310" target="_blank">source</a>]

```lua
MoveCtrl.SetPhysics(UnitID, number, number, number, number, number, number, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `posX` `number` — Position X component.
- `posY` `number` — Position Y component.
- `posZ` `number` — Position Z component.
- `velX` `number` — Velocity X component.
- `velY` `number` — Velocity Y component.
- `velZ` `number` — Velocity Z component.
- `rotX` `number` — Rotation X component.
- `rotY` `number` — Rotation Y component.
- `rotZ` `number` — Rotation Z component.

### MoveCtrl.SetPosition {#MoveCtrl.SetPosition}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L329-L335" target="_blank">source</a>]

```lua
MoveCtrl.SetPosition(UnitID, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `posX` `number` — Position X component.
- `posY` `number` — Position Y component.
- `posZ` `number` — Position Z component.

### MoveCtrl.SetVelocity {#MoveCtrl.SetVelocity}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L352-L358" target="_blank">source</a>]

```lua
MoveCtrl.SetVelocity(UnitID, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `velX` `number` — Velocity X component.
- `velY` `number` — Velocity Y component.
- `velZ` `number` — Velocity Z component.

### MoveCtrl.SetRelativeVelocity {#MoveCtrl.SetRelativeVelocity}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L375-L381" target="_blank">source</a>]

```lua
MoveCtrl.SetRelativeVelocity(UnitID, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `relVelX` `number` — Relative velocity X component.
- `relVelY` `number` — Relative velocity Y component.
- `relVelZ` `number` — Relative velocity Z component.

### MoveCtrl.SetRotation {#MoveCtrl.SetRotation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L398-L404" target="_blank">source</a>]

```lua
MoveCtrl.SetRotation(UnitID, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `rotX` `number` — Rotation X component.
- `rotY` `number` — Rotation Y component.
- `rotZ` `number` — Rotation Z component.

### MoveCtrl.SetRotationOffset {#MoveCtrl.SetRotationOffset}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L421-L424" target="_blank">source</a>]

**Deprecated:** 

```lua
MoveCtrl.SetRotationOffset() -> nil
```

### MoveCtrl.SetRotationVelocity {#MoveCtrl.SetRotationVelocity}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L432-L438" target="_blank">source</a>]

```lua
MoveCtrl.SetRotationVelocity(UnitID, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `rotVelX` `number` — Rotation velocity X component.
- `rotVelY` `number` — Rotation velocity Y component.
- `rotVelZ` `number` — Rotation velocity Z component.

### MoveCtrl.SetHeading {#MoveCtrl.SetHeading}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L454-L458" target="_blank">source</a>]

```lua
MoveCtrl.SetHeading(UnitID, Heading) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `heading` [`Heading`](Aliases.md#Heading)

### MoveCtrl.SetTrackSlope {#MoveCtrl.SetTrackSlope}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L475-L479" target="_blank">source</a>]

```lua
MoveCtrl.SetTrackSlope(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `trackSlope` `boolean`

### MoveCtrl.SetTrackGround {#MoveCtrl.SetTrackGround}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L492-L496" target="_blank">source</a>]

```lua
MoveCtrl.SetTrackGround(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `trackGround` `boolean`

### MoveCtrl.SetTrackLimits {#MoveCtrl.SetTrackLimits}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L509-L513" target="_blank">source</a>]

```lua
MoveCtrl.SetTrackLimits(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `trackLimits` `boolean`

### MoveCtrl.SetGroundOffset {#MoveCtrl.SetGroundOffset}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L526-L530" target="_blank">source</a>]

```lua
MoveCtrl.SetGroundOffset(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `groundOffset` `number`

### MoveCtrl.SetGravity {#MoveCtrl.SetGravity}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L543-L547" target="_blank">source</a>]

```lua
MoveCtrl.SetGravity(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `gravityFactor` `number`

### MoveCtrl.SetDrag {#MoveCtrl.SetDrag}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L560-L564" target="_blank">source</a>]

```lua
MoveCtrl.SetDrag(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `drag` `number`

### MoveCtrl.SetWindFactor {#MoveCtrl.SetWindFactor}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L577-L581" target="_blank">source</a>]

```lua
MoveCtrl.SetWindFactor(UnitID, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `windFactor` `number`

### MoveCtrl.SetLimits {#MoveCtrl.SetLimits}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L594-L603" target="_blank">source</a>]

```lua
MoveCtrl.SetLimits(UnitID, number, number, number, number, number, number) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `minX` `number` — Minimum position X component.
- `minY` `number` — Minimum position Y component.
- `minZ` `number` — Minimum position Z component.
- `maxX` `number` — Maximum position X component.
- `maxY` `number` — Maximum position Y component.
- `maxZ` `number` — Maximum position Z component.

### MoveCtrl.SetNoBlocking {#MoveCtrl.SetNoBlocking}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L619-L623" target="_blank">source</a>]

```lua
MoveCtrl.SetNoBlocking(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `noBlocking` `boolean`

### MoveCtrl.SetCollideStop {#MoveCtrl.SetCollideStop}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L642-L646" target="_blank">source</a>]

```lua
MoveCtrl.SetCollideStop(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `collideStop` `boolean`

### MoveCtrl.SetLimitsStop {#MoveCtrl.SetLimitsStop}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L659-L663" target="_blank">source</a>]

```lua
MoveCtrl.SetLimitsStop(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `limitsStop` `boolean`

### MoveCtrl.SetGunshipMoveTypeData {#MoveCtrl.SetGunshipMoveTypeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L798-L803" target="_blank">source</a>]

```lua
MoveCtrl.SetGunshipMoveTypeData(UnitID, HoverAirMoveType) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `moveType` [`HoverAirMoveType`](HoverAirMoveType.md#HoverAirMoveType)

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetGunshipMoveTypeData (overload 1) {#MoveCtrl.SetGunshipMoveTypeData-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L804-L816" target="_blank">source</a>]

```lua
MoveCtrl.SetGunshipMoveTypeData(UnitID, (GenericMoveTypeBooleanKey|"collide"|"dontLand"|"airStrafe"|"useSmoothMesh"|"bankingAllowed"), boolean) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `key` `(GenericMoveTypeBooleanKey|"collide"|"dontLand"|"airStrafe"|"useSmoothMesh"|"bankingAllowed")`
- `value` `boolean`

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetGunshipMoveTypeData (overload 2) {#MoveCtrl.SetGunshipMoveTypeData-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L817-L832" target="_blank">source</a>]

```lua
MoveCtrl.SetGunshipMoveTypeData(UnitID, (GenericMoveTypeNumberKey|"wantedHeight"|"accRate"|"decRate"|"turnRate"|"altitudeRate"|"currentBank"|"currentPitch"...), number) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `key` `(GenericMoveTypeNumberKey|"wantedHeight"|"accRate"|"decRate"|"turnRate"|"altitudeRate"|"currentBank"|"currentPitch"...)`
- `value` `number`

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetAirMoveTypeData {#MoveCtrl.SetAirMoveTypeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L860-L865" target="_blank">source</a>]

```lua
MoveCtrl.SetAirMoveTypeData(UnitID, StrafeAirMoveType) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `moveType` [`StrafeAirMoveType`](StrafeAirMoveType.md#StrafeAirMoveType)

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetAirMoveTypeData (overload 1) {#MoveCtrl.SetAirMoveTypeData-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L866-L876" target="_blank">source</a>]

```lua
MoveCtrl.SetAirMoveTypeData(UnitID, (GenericMoveTypeBooleanKey|"collide"|"useSmoothMesh"|"loopbackAttack"), boolean) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `key` `(GenericMoveTypeBooleanKey|"collide"|"useSmoothMesh"|"loopbackAttack")`
- `value` `boolean`

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetAirMoveTypeData (overload 2) {#MoveCtrl.SetAirMoveTypeData-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L877-L897" target="_blank">source</a>]

```lua
MoveCtrl.SetAirMoveTypeData(UnitID, (GenericMoveTypeNumberKey|"wantedHeight"|"turnRadius"|"accRate"|"decRate"|"maxAcc"|"maxDec"|"maxBank"...), number) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `key` `(GenericMoveTypeNumberKey|"wantedHeight"|"turnRadius"|"accRate"|"decRate"|"maxAcc"|"maxDec"|"maxBank"...)`
- `value` `number`

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetAirMoveTypeData (overload 3) {#MoveCtrl.SetAirMoveTypeData-3}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L898-L905" target="_blank">source</a>]

```lua
MoveCtrl.SetAirMoveTypeData(UnitID, ("maneuverBlockTime"), integer) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `key` `("maneuverBlockTime")`
- `value` `integer`

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetGroundMoveTypeData {#MoveCtrl.SetGroundMoveTypeData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L929-L934" target="_blank">source</a>]

```lua
MoveCtrl.SetGroundMoveTypeData(UnitID, GroundMoveType) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `moveType` [`GroundMoveType`](GroundMoveType.md#GroundMoveType)

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetGroundMoveTypeData (overload 1) {#MoveCtrl.SetGroundMoveTypeData-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L935-L945" target="_blank">source</a>]

```lua
MoveCtrl.SetGroundMoveTypeData(UnitID, (GenericMoveTypeBooleanKey|"atGoal"|"atEndOfPath"|"pushResistant"), boolean) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `key` `(GenericMoveTypeBooleanKey|"atGoal"|"atEndOfPath"|"pushResistant")`
- `value` `boolean`

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetGroundMoveTypeData (overload 2) {#MoveCtrl.SetGroundMoveTypeData-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L946-L962" target="_blank">source</a>]

```lua
MoveCtrl.SetGroundMoveTypeData(UnitID, (GenericMoveTypeNumberKey|"turnRate"|"turnAccel"|"accRate"|"decRate"|"myGravity"|"maxReverseDist"|"minReverseAngle"...), number) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `key` `(GenericMoveTypeNumberKey|"turnRate"|"turnAccel"|"accRate"|"decRate"|"myGravity"|"maxReverseDist"|"minReverseAngle"...)`
- `value` `number`

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetGroundMoveTypeData (overload 3) {#MoveCtrl.SetGroundMoveTypeData-3}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L963-L970" target="_blank">source</a>]

```lua
MoveCtrl.SetGroundMoveTypeData(UnitID, ("minScriptChangeHeading"), integer) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `key` `("minScriptChangeHeading")`
- `value` `integer`

**Returns**

- `numAssignedValues` `integer`

### MoveCtrl.SetMoveDef {#MoveCtrl.SetMoveDef}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L981-L986" target="_blank">source</a>]

```lua
MoveCtrl.SetMoveDef(UnitID, (integer|string)) -> boolean
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `moveDef` `(integer|string)` — Name or path type of the MoveDef.

**Returns**

- `success` `boolean` — `true` if the `MoveDef` was set, `false` if `unitID` or `moveDef` were invalid, or if the unit does not support a `MoveDef`.
