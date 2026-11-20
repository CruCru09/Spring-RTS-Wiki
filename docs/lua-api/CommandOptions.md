---
title: "CommandOptions"
tags:
  - Lua-API
---

## CommandOptions {#CommandOptions}
*class*

Full command options object for reading from a [Command](Command.md#Command).

Note that this has extra fields `internal` and `coded` that are not supported
when creating a command from Lua.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUtils.cpp#L933-L948" target="_blank">source</a>]

**Fields**

- <span id="CommandOptions.coded"></span> `CommandOptions.coded` `(CommandOptionBit|integer)` — Bitmask of command options.
- <span id="CommandOptions.alt"></span> `CommandOptions.alt` `boolean` — Alt key pressed.
- <span id="CommandOptions.ctrl"></span> `CommandOptions.ctrl` `boolean` — Ctrl key pressed.
- <span id="CommandOptions.shift"></span> `CommandOptions.shift` `boolean` — Shift key pressed.
- <span id="CommandOptions.right"></span> `CommandOptions.right` `boolean` — Right mouse key pressed.
- <span id="CommandOptions.meta"></span> `CommandOptions.meta` `boolean` — Meta key (space) pressed.
- <span id="CommandOptions.internal"></span> `CommandOptions.internal` `boolean`
