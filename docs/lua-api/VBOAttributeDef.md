---
title: "VBOAttributeDef"
tags:
  - Lua-API
---

## VBOAttributeDef {#VBOAttributeDef}
*class*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L461-L497" target="_blank">source</a>]

**Fields**

- <span id="VBOAttributeDef.id"></span> `VBOAttributeDef.id` `integer?`
- <span id="VBOAttributeDef.name"></span> `VBOAttributeDef.name` `string?` — The location in the vertex shader layout e.g.: layout (location = 0) in vec2
aPos. optional attrib, specifies location in the vertex shader. If not
specified the implementation will increment the counter starting from 0.
There can be maximum 16 attributes (so id of 15 is max).

(Default: `attr#` where `#` is `id`)

The name for this VBO, only used for debugging.
- <span id="VBOAttributeDef.size"></span> `VBOAttributeDef.size` `integer?`
- <span id="VBOAttributeDef.type"></span> `VBOAttributeDef.type` `GL?` — Defaults to to 4 for VBO. The number of floats that constitute 1 element in
this buffer. e.g. for the previous layout (location = 0) in vec2 aPos, it
would be size = 2.

(Default: [GL.FLOAT](GL-enum.md#GL.FLOAT)) The datatype of this element.

Accepts the following:
- [GL.BYTE](GL-enum.md#GL.BYTE)
- [GL.UNSIGNED_BYTE](GL-enum.md#GL.UNSIGNED_BYTE)
- [GL.SHORT](GL-enum.md#GL.SHORT)
- [GL.UNSIGNED_SHORT](GL-enum.md#GL.UNSIGNED_SHORT)
- [GL.INT](GL-enum.md#GL.INT)
- [GL.UNSIGNED_INT](GL-enum.md#GL.UNSIGNED_INT)
- [GL.FLOAT](GL-enum.md#GL.FLOAT)
- <span id="VBOAttributeDef.normalized"></span> `VBOAttributeDef.normalized` `boolean?` — (Defaults: `false`)

It's possible to submit normals without normalizing them first, normalized
will make sure data is normalized.
