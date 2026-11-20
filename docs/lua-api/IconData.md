---
title: "IconData"
tags:
  - Lua-API
---

## IconData {#IconData}
*class*

Icon Data

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1461-L1464" target="_blank">source</a>]

**Fields**

- <span id="IconData.name"></span> `IconData.name` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1480-L1480" target="_blank">source</a>]
- <span id="IconData.fileName"></span> `IconData.fileName` `string?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1483-L1483" target="_blank">source</a>]
- <span id="IconData.size"></span> `IconData.size` `number?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1485-L1485" target="_blank">source</a>]
Relative size of the icon
- <span id="IconData.distance"></span> `IconData.distance` `number?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1487-L1487" target="_blank">source</a>]
When squared used as a icon length multiplier
- <span id="IconData.drawOrder"></span> `IconData.drawOrder` `number?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1489-L1489" target="_blank">source</a>]
Sort priority for icon drawing; icons with higher values are drawn on top of lower ones
- <span id="IconData.radiusAdjust"></span> `IconData.radiusAdjust` `boolean?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1491-L1491" target="_blank">source</a>]
Controls whether the unit radius affects the icon size
- <span id="IconData.srcTexCoords"></span> `IconData.srcTexCoords` `TexCoords?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1494-L1494" target="_blank">source</a>]
- <span id="IconData.atlasTexCoords"></span> `IconData.atlasTexCoords` [`TexCoords`](TexCoords.md#TexCoords) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedRead.cpp#L1509-L1509" target="_blank">source</a>]
atlasIndex points to $icons0 or $icons1 texture
