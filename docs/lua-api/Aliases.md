---
title: "Aliases"
tags:
  - Lua-API
---

## RmlUi.EventParametersProxy.TrueFalse {#RmlUi.EventParametersProxy.TrueFalse}

*alias* `(0|1)`

RmlUi uses 0 and 1 to represent boolean values here.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Event.cpp#L87-L92" target="_blank">source</a>]

## GenericMoveTypeBooleanKey {#GenericMoveTypeBooleanKey}

*alias* `("useWantedSpeed[0]"|"useWantedSpeed[1]")`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L706-L710" target="_blank">source</a>]

## ProjectileID {#ProjectileID}

*alias* `integer`

Identifier of a projectile currently present in the simulation.

Synced and unsynced projectiles are numbered independently.

## RmlUi.StyleProxy {#RmlUi.StyleProxy}

*alias* `{ [string]: string }`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L247-L249" target="_blank">source</a>]

## CameraName {#CameraName}

*alias* `("ta"|"spring"|"rot"|"ov"|"free"|"fps"|"dummy")`

## ResourceName {#ResourceName}

*alias* `("metal"|"energy"|"m"|"e")`

## PlayerID {#PlayerID}

*alias* `integer`

Identifier of a player.

Players are numbered from `0`. Note that a player is a human client, which is
not the same thing as a team.

## RmlUi.SelectOptionsProxy {#RmlUi.SelectOptionsProxy}

*alias* `RmlUi.SelectOptionsProxyNode[]`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L243-L245" target="_blank">source</a>]

## FacingInteger {#FacingInteger}

*alias* `(0|1|2|3)`

## TeamID {#TeamID}

*alias* `integer`

Identifier of a team.

Teams are numbered from `0`; [Spring.GetGaiaTeamID](Spring.md#Spring.GetGaiaTeamID) returns the Gaia team.

## RmlUi.SelectOptionsProxyNode {#RmlUi.SelectOptionsProxyNode}

*alias* `{ element: RmlUi.Element, value: string }`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L251-L253" target="_blank">source</a>]

## UniformArrayType {#UniformArrayType}

*alias* `(1|2|3)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1186-L1191" target="_blank">source</a>]

## LosTable {#LosTable}

*alias* `table<("los"|"radar"|"prevLos"|"contRadar"),boolean>`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2918-L2920" target="_blank">source</a>]

## DrawMask {#DrawMask}

*alias* `integer`

## CommandOptionBit {#CommandOptionBit}

*alias* `(4|8|16|32|64|128)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUtils.cpp#L983-L991" target="_blank">source</a>]

## RmlUi.EventParametersProxy.MouseButton {#RmlUi.EventParametersProxy.MouseButton}

*alias* `(0|1|2)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Event.cpp#L80-L85" target="_blank">source</a>]

## CommandOptionName {#CommandOptionName}

*alias* `("right"|"alt"|"ctrl"|"shift"|"meta")`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUtils.cpp#L993-L1000" target="_blank">source</a>]

## GenericMoveTypeNumberKey {#GenericMoveTypeNumberKey}

*alias* `("maxSpeed"|"maxWantedSpeed"|"maneuverLeash"|"waterline")`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedMoveCtrl.cpp#L698-L704" target="_blank">source</a>]

## HashType {#HashType}

*alias* `(0|1)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L903-L907" target="_blank">source</a>]

## DecalID {#DecalID}

*alias* `integer`

Identifier of a ground decal.

## float3 {#float3}

*alias* [`xyz`](xyz.md#xyz)

## BuildOrderBlockedStatus {#BuildOrderBlockedStatus}

*alias* `(0|1|2|3)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L8145-L8151" target="_blank">source</a>]

## UnitDefID {#UnitDefID}

*alias* `integer`

Identifier of a unit definition, i.e. an index into `UnitDefs`.

Valid IDs start at `1`; `0` is not a valid unit definition.

## MatrixName {#MatrixName}

*alias* `("view"|"projection"|"viewprojection"|"viewinverse"|"projectioninverse"|"viewprojectioninverse"|"billboard"|"shadow"...)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGLUtils.cpp#L140-L154" target="_blank">source</a>]

## DrawFlag {#DrawFlag}

*alias* `(0|1|2|4|8|16|32|128)`

Drawing Flags

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L2394-L2406" target="_blank">source</a>]

## UnitID {#UnitID}

*alias* `integer`

Identifier of a unit currently present in the simulation.

IDs are drawn from a pool and are recycled, so the ID of a dead unit may
later be handed out to a different unit.

## Heading {#Heading}

*alias* `integer`

Integer in range `[-32768, 32767]` that represents a 2D (xz plane) unit
orientation.

```
                  F(N=2) = H(-32768 / 32767)

                         ^
                         |
                         |
 F(W=3) = H(-16384)  <---o--->  F(E=1) = H(16384)
                         |
                         |
                         v

                  F(S=0) = H(0)
```

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L4222-L4240" target="_blank">source</a>]

## float2 {#float2}

*alias* [`xy`](xy.md#xy)

## RmlUi.ElementStyleProxy {#RmlUi.ElementStyleProxy}

*alias* `{ [string]: string }`

Gets the rcss styles associated with an element. As far as I can tell, the values will always be a string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L135-L138" target="_blank">source</a>]

## Facing {#Facing}

*alias* `(0|1|2|3|"s"|"e"|"n"|"w"...)`

## float4 {#float4}

*alias* [`xyzw`](xyzw.md#xyzw)

## ResourceUsage {#ResourceUsage}

*alias* `table<ResourceName,number>`

## RmlUi.EventID {#RmlUi.EventID}

*alias* `(0|1|2|3|4|5|6|7...)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L198-L235" target="_blank">source</a>]

## AllyTeamID {#AllyTeamID}

*alias* `integer`

Identifier of an allyteam.

Allyteams are numbered from `0`.

## RmlUi.ElementAttributesProxy {#RmlUi.ElementAttributesProxy}

*alias* `{ [string]: (string|number|boolean) }`

Contains all the attributes of an element: The stuff in the opening tag i.e. `<span class="my-class">`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L130-L133" target="_blank">source</a>]

## TargetType {#TargetType}

*alias* `(0|1|2|3)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedRead.cpp#L5746-L5752" target="_blank">source</a>]

## CreateCommandOptions {#CreateCommandOptions}

*alias* `(CommandOptionName[]|table<CommandOptionName,boolean>|CommandOptionBit|integer)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUtils.cpp#L1002-L1008" target="_blank">source</a>]

## RmlUi.MouseButton {#RmlUi.MouseButton}

*alias* `(0|1|2)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L118-L123" target="_blank">source</a>]

## WeaponDefID {#WeaponDefID}

*alias* `integer`

Identifier of a weapon definition, i.e. an index into `WeaponDefs`,
or a negated `CSolidObject::DamageType`

## FeatureID {#FeatureID}

*alias* `integer`

Identifier of a feature currently present in the simulation.

IDs are drawn from a pool and are recycled, so the ID of a destroyed feature
may later be handed out to a different feature.

## CreateCommandParams {#CreateCommandParams}

*alias* `(number[]|number)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUtils.cpp#L1101-L1105" target="_blank">source</a>]

## ObjectID {#ObjectID}

*alias* `(UnitID|FeatureID)`

Identifier of a solid object, i.e. either a unit or a feature.

Unit and feature IDs live in separate ranges, so which of the two is meant
follows from context: [Spring.UnitRendering](Spring.md#Spring.UnitRendering) functions take a unit ID where
[Spring.FeatureRendering](Spring.md#Spring.FeatureRendering) functions take a feature ID, and callins that pass
an object ID pass the type alongside it.

## SoundChannel {#SoundChannel}

*alias* `("general"|"battle"|"sfx"|"unitreply"|"voice"|"userinterface"|"ui"|0...)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L784-L797" target="_blank">source</a>]

## GroupID {#GroupID}

*alias* `integer`

Identifier of a unit (control) group.

Groups are per-team. IDs `0` to `9` are the hot-key groups that players can
create and select directly; IDs from `10` up are "special" groups that can
only be created programmatically. Interfaces that accept or return a group
for a unit use `-1` to mean "no group".

## StorageName {#StorageName}

*alias* `("metalStorage"|"energyStorage"|"ms"|"es")`

## CameraMode {#CameraMode}

*alias* `(0|1|2|3|4|5|6)`

## RmlUi.ElementChildNodesProxy {#RmlUi.ElementChildNodesProxy}

*alias* `RmlUi.Element[]`

Contains a list of all child elements.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L125-L128" target="_blank">source</a>]

## LogLevel {#LogLevel}

*alias* `(integer|"debug"|"info"|"notice"|"warning"|"deprecated"|"error"|"fatal")`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUtils.cpp#L1434-L1444" target="_blank">source</a>]

## FeatureDefID {#FeatureDefID}

*alias* `integer`

Identifier of a feature definition, i.e. an index into `FeatureDefs`.

## Attachment {#Attachment}

*alias* `("depth"|"stencil"|"color0"|"color1"|"color2"|"color3"|"color4"|"color5"...)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L104-L124" target="_blank">source</a>]

## ModType {#ModType}

*alias* `(0|1|3|4)`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L148-L154" target="_blank">source</a>]
