---
title: "UniformParam"
tags:
  - Lua-API
---

## UniformParam {#UniformParam}
*class*

Inherits `{ [string]: (T|T[]) }`

A table of uniform name to value.

The Uniforms are the values you send along with the shader-program. To use
them in the shader-program declare them like this: `uniform float frame;`

Specify a Lua array to initialize GLSL arrays.

The engine will automatically fill in an appropriately named uniform for team
colour if it is declared;

```glsl
uniform vec4 teamColor;
```

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L553-L570" target="_blank">source</a>]
