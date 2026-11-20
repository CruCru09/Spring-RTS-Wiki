---
title: "VAO"
tags:
  - Lua-API
---

## VAO {#VAO}
*class*

Vertex Array Object

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L19-L26" target="_blank">source</a>]

**See:** rts/Lua/LuaVAOImpl.cpp

**Members**

### VAO:Delete {#VAO:Delete}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L40-L44" target="_blank">source</a>]

```lua
VAO:Delete() -> nil
```

**Returns**

- `nil`

### VAO:AttachVertexBuffer {#VAO:AttachVertexBuffer}
*function*

Attaches a VBO to be used as a vertex buffer

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L94-L99" target="_blank">source</a>]

```lua
VAO:AttachVertexBuffer(VBO) -> nil
```

**Parameters**

- `vbo` [`VBO`](VBO.md#VBO)

**Returns**

- `nil`

### VAO:AttachInstanceBuffer {#VAO:AttachInstanceBuffer}
*function*

Attaches a VBO to be used as an instance buffer

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L106-L111" target="_blank">source</a>]

```lua
VAO:AttachInstanceBuffer(VBO) -> nil
```

**Parameters**

- `vbo` [`VBO`](VBO.md#VBO)

**Returns**

- `nil`

### VAO:AttachIndexBuffer {#VAO:AttachIndexBuffer}
*function*

Attaches a VBO to be used as an index buffer

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L118-L123" target="_blank">source</a>]

```lua
VAO:AttachIndexBuffer(VBO) -> nil
```

**Parameters**

- `vbo` [`VBO`](VBO.md#VBO)

**Returns**

- `nil`

### VAO:DrawArrays {#VAO:DrawArrays}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L368-L377" target="_blank">source</a>]

```lua
VAO:DrawArrays(GL, integer?, integer?, integer?, integer?) -> nil
```

**Parameters**

- `glEnum` [`GL`](GL-enum.md#GL) — primitivesMode
- `vertexCount` `integer?`
- `vertexFirst` `integer?`
- `instanceCount` `integer?`
- `instanceFirst` `integer?`

**Returns**

- `nil`

### VAO:DrawElements {#VAO:DrawElements}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L405-L415" target="_blank">source</a>]

```lua
VAO:DrawElements(GL, integer?, integer?, integer?, integer?, integer?) -> nil
```

**Parameters**

- `glEnum` [`GL`](GL-enum.md#GL) — primitivesMode
- `drawCount` `integer?`
- `baseIndex` `integer?`
- `instanceCount` `integer?`
- `baseVertex` `integer?`
- `baseInstance` `integer?`

**Returns**

- `nil`

### VAO:AddUnitsToSubmission {#VAO:AddUnitsToSubmission}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L467-L472" target="_blank">source</a>]

```lua
VAO:AddUnitsToSubmission((UnitID|UnitID[])) -> integer
```

**Parameters**

- `unitIDs` `(UnitID|UnitID[])`

**Returns**

- `submittedCount` `integer`

### VAO:AddFeaturesToSubmission {#VAO:AddFeaturesToSubmission}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L477-L482" target="_blank">source</a>]

```lua
VAO:AddFeaturesToSubmission((FeatureID|FeatureID[])) -> integer
```

**Parameters**

- `featureIDs` `(FeatureID|FeatureID[])`

**Returns**

- `submittedCount` `integer`

### VAO:AddUnitDefsToSubmission {#VAO:AddUnitDefsToSubmission}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L487-L492" target="_blank">source</a>]

```lua
VAO:AddUnitDefsToSubmission((UnitDefID|UnitDefID[])) -> integer
```

**Parameters**

- `unitDefIDs` `(UnitDefID|UnitDefID[])`

**Returns**

- `submittedCount` `integer`

### VAO:AddFeatureDefsToSubmission {#VAO:AddFeatureDefsToSubmission}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L497-L502" target="_blank">source</a>]

```lua
VAO:AddFeatureDefsToSubmission((FeatureDefID|FeatureDefID[])) -> integer
```

**Parameters**

- `featureDefIDs` `(FeatureDefID|FeatureDefID[])`

**Returns**

- `submittedCount` `integer`

### VAO:RemoveFromSubmission {#VAO:RemoveFromSubmission}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L507-L512" target="_blank">source</a>]

```lua
VAO:RemoveFromSubmission(integer) -> nil
```

**Parameters**

- `index` `integer`

**Returns**

- `nil`

### VAO:Submit {#VAO:Submit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAOImpl.cpp#L532-L536" target="_blank">source</a>]

```lua
VAO:Submit() -> nil
```

**Returns**

- `nil`
