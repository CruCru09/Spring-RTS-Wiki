---
title: "VBO"
tags:
  - Lua-API
---

## VBO {#VBO}
*class*

Vertex Buffer Object

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L37-L43" target="_blank">source</a>]

**Members**

### VBO:Delete {#VBO:Delete}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L111-L115" target="_blank">source</a>]

```lua
VBO:Delete() -> nil
```

**Returns**

- `nil`

### VBO:Define {#VBO:Define}
*function*

Specify the kind of VBO you will be using.

```lua
terrainVertexVBO:Define(numPoints, {{ id = 0, name = "pos", size = 2 }})
```

It is usually an array of vertex/color/uv data, but can also be an array of
instance uniforms.

If you want to specify multiple instances of something to render, you will
need to create another VBO, which also specifies the number of instances you
wish to render, and the size of the data passed to each instance.

If you want say 5 elements, and each element is defined in the layout:

```lua
{id = 0, name = "first", size = 1},{id = 1, name = "second", size = 2}}
```

Then the total size of your VBO will be `5 * (1 + 2)`.

They will be laid out consecutively: `[1,2],[1,2],[1,2],[1,2],[1,2]`.

This is important for when you call [VBO:Upload](VBO.md#VBO:Upload), you need to make sure you
enter your data into the Lua array correctly.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L499-L537" target="_blank">source</a>]

**See:** [VBO:Upload](VBO.md#VBO:Upload)

```lua
VBO:Define(integer, (integer|VBOAttributeDef[])) -> nil
```

**Parameters**

- `size` `integer` — The maximum number of elements this VBO can have.
- `attribs` `(integer|VBOAttributeDef[])`

**Returns**

- `nil`

### VBO:GetBufferSize {#VBO:GetBufferSize}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L585-L591" target="_blank">source</a>]

```lua
VBO:GetBufferSize() -> integer, integer, integer
```

**Returns**

- `elementsCount` `integer`
- `bufferSizeInBytes` `integer`
- `size` `integer`

### VBO:Upload {#VBO:Upload}
*function*

Uploads data into the VBO.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L602-L623" target="_blank">source</a>]

**See:** [VBO:Define](VBO.md#VBO:Define)

```lua
VBO:Upload(number[], integer?, integer?, integer?, integer?) -> number[], integer, (integer|(integer,integer...))
```

**Parameters**

- `vboData` `number[]` — Array of values to upload into the VBO.
- `attributeIndex` `integer?` — (Default: `-1`)

If supplied with non-default value then the data from `vboData` will only be
used to upload the data to this particular attribute.

The whole `vboData` is expected to contain only attributeIndex data.

Otherwise all attributes get updated sequentially across attributes and elements.
- `elemOffset` `integer?` — (Default: `0`) The index in destination VBO (on GPU) at which storing begins.
- `luaStartIndex` `integer?` — (Default: `1`) The index of `vboData` at which copying begins.
- `luaFinishIndex` `integer?` — (Default: `#vboData`) The index of `vboData` at which copying ends.

**Returns**

- `indexData` `number[]`
- `elemOffset` `integer`
- `attrID` `(integer|(integer,integer...))`

### VBO:Download {#VBO:Download}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L666-L677" target="_blank">source</a>]

```lua
VBO:Download(integer?, integer?, integer?, boolean?) -> number[]
```

**Parameters**

- `attributeIndex` `integer?` — (Default: `-1`) when supplied with non-default value: only data
from specified attribute will be downloaded - otherwise all attributes are
downloaded
- `elementOffset` `integer?` — (Default: `0`) download data starting from this element
- `elementCount` `integer?` — number of elements to download
- `forceGPURead` `boolean?` — (Default: `false`) force downloading the data from GPU buffer as opposed
to using shadow RAM buffer

**Returns**

- `vboData` `number[]`

### VBO:ModelsVBO {#VBO:ModelsVBO}
*function*

Binds engine side vertex or index VBO containing models (units, features) data.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1185-L1192" target="_blank">source</a>]

Also fills in VBO definition data as they're set for engine models (no need to do VBO:Define()).

```lua
VBO:ModelsVBO() -> integer?
```

**Returns**

- `size` `integer?` — buffer size in bytes

### VBO:InstanceDataFromUnitDefIDs {#VBO:InstanceDataFromUnitDefIDs}
*function*

Fills in attribute data for each specified unitDefID

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1204-L1229" target="_blank">source</a>]

The instance data in that attribute will contain the offset to bind position
matrix in global matrices SSBO and offset to uniform buffer structure in
global per unit/feature uniform SSBO (unused for Unit/FeatureDefs), as
well as some auxiliary data such as palette index and number of pieces.

Data Layout:
```
SInstanceData:
   , traOffset{ matOffset_ }         // updated during the following draw frames
   , uniOffset{ uniOffset_ }         // updated during the following draw frames
   , info{ paletteIndex, numPieces } // not updated during the following draw frames
   , aux1 { 0u }
```

```lua
VBO:InstanceDataFromUnitDefIDs((UnitDefID|UnitDefID[]), integer, integer?, integer?) -> (integer,integer,integer,integer), integer, integer
```

**Parameters**

- `unitDefIDs` `(UnitDefID|UnitDefID[])`
- `attrID` `integer`
- `teamIdOpt` `integer?`
- `elementOffset` `integer?`

**Returns**

- `instanceData` `(integer,integer,integer,integer)`
- `elementOffset` `integer`
- `attrID` `integer`

### VBO:InstanceDataFromFeatureDefIDs {#VBO:InstanceDataFromFeatureDefIDs}
*function*

Fills in attribute data for each specified featureDefID

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1243-L1268" target="_blank">source</a>]

The instance data in that attribute will contain the offset to bind position
matrix in global matrices SSBO and offset to uniform buffer structure in
global per unit/feature uniform SSBO (unused for Unit/FeatureDefs), as
well as some auxiliary data such as palette index and number of pieces.

Data Layout
```
SInstanceData:
   , traOffset{ matOffset_ }         // updated during the following draw frames
   , uniOffset{ uniOffset_ }         // updated during the following draw frames
   , info{ paletteIndex, numPieces } // not updated during the following draw frames
   , aux1 { 0u }
```

```lua
VBO:InstanceDataFromFeatureDefIDs((FeatureDefID|FeatureDefID[]), integer, integer?, integer?) -> (integer,integer,integer,integer), integer, integer
```

**Parameters**

- `featureDefIDs` `(FeatureDefID|FeatureDefID[])`
- `attrID` `integer`
- `teamIdOpt` `integer?`
- `elementOffset` `integer?`

**Returns**

- `instanceData` `(integer,integer,integer,integer)`
- `elementOffset` `integer`
- `attrID` `integer`

### VBO:InstanceDataFromUnitIDs {#VBO:InstanceDataFromUnitIDs}
*function*

Fills in attribute data for each specified unitID

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1282-L1308" target="_blank">source</a>]

The instance data in that attribute will contain the offset to bind position
matrix in global matrices SSBO and offset to uniform buffer structure in
global per unit/feature uniform SSBO (unused for Unit/FeatureDefs), as
well as some auxiliary data such as palette index and number of pieces.

Data Layout

```
SInstanceData:
   , traOffset{ matOffset_ }         // updated during the following draw frames
   , uniOffset{ uniOffset_ }         // updated during the following draw frames
   , info{ paletteIndex, numPieces } // not updated during the following draw frames
   , aux1 { 0u }
```

```lua
VBO:InstanceDataFromUnitIDs((UnitID|UnitID[]), integer, integer?, integer?) -> (integer,integer,integer,integer), integer, integer
```

**Parameters**

- `unitIDs` `(UnitID|UnitID[])`
- `attrID` `integer`
- `teamIdOpt` `integer?`
- `elementOffset` `integer?`

**Returns**

- `instanceData` `(integer,integer,integer,integer)`
- `elementOffset` `integer`
- `attrID` `integer`

### VBO:InstanceDataFromFeatureIDs {#VBO:InstanceDataFromFeatureIDs}
*function*

Fills in attribute data for each specified featureID

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1320-L1336" target="_blank">source</a>]

The instance data in that attribute will contain the offset to bind position
matrix in global matrices SSBO and offset to uniform buffer structure in
global per unit/feature uniform SSBO (unused for Unit/FeatureDefs), as
well as some auxiliary data such as palette index and number of pieces.

```lua
VBO:InstanceDataFromFeatureIDs((FeatureID|FeatureID[]), integer, integer?, integer?) -> (integer,integer,integer,integer), integer, integer
```

**Parameters**

- `featureIDs` `(FeatureID|FeatureID[])`
- `attrID` `integer`
- `teamIdOpt` `integer?`
- `elementOffset` `integer?`

**Returns**

- `instanceData` `(integer,integer,integer,integer)`
- `elementOffset` `integer`
- `attrID` `integer`

### VBO:MatrixDataFromProjectileIDs {#VBO:MatrixDataFromProjectileIDs}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1348-L1358" target="_blank">source</a>]

```lua
VBO:MatrixDataFromProjectileIDs((ProjectileID|ProjectileID[]), integer, integer?, integer?) -> number[], integer, (integer|(integer,integer...))
```

**Parameters**

- `projectileIDs` `(ProjectileID|ProjectileID[])`
- `attrID` `integer`
- `teamIdOpt` `integer?`
- `elementOffset` `integer?`

**Returns**

- `matDataVec` `number[]` — Flattened 4x4 matrix(es)
- `elemOffset` `integer`
- `attrID` `(integer|(integer,integer...))`

### VBO:BindBufferRange {#VBO:BindBufferRange}
*function*

Bind a range within a buffer object to an indexed buffer target

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1430-L1444" target="_blank">source</a>]

Generally mimics
https://registry.khronos.org/OpenGL-Refpages/gl4/html/glBindBufferRange.xhtml
except offset and size are specified in number of elements / element indices.

```lua
VBO:BindBufferRange(integer, integer?, integer?, GL?) -> integer
```

**Parameters**

- `index` `integer` — should be in the range between
`5 < index < GL_MAX_UNIFORM_BUFFER_BINDINGS` value (usually 31)
- `elementOffset` `integer?`
- `elementCount` `integer?`
- `target` `GL?` — glEnum

**Returns**

- `bindingIndex` `integer` — when successful, -1 otherwise

### VBO:UnbindBufferRange {#VBO:UnbindBufferRange}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1451-L1459" target="_blank">source</a>]

```lua
VBO:UnbindBufferRange(integer, integer?, integer?, GL?) -> integer
```

**Parameters**

- `index` `integer`
- `elementOffset` `integer?`
- `elementCount` `integer?`
- `target` `GL?` — glEnum

**Returns**

- `bindingIndex` `integer` — when successful, -1 otherwise

### VBO:DumpDefinition {#VBO:DumpDefinition}
*function*

Logs the definition of the VBO to the console

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1466-L1470" target="_blank">source</a>]

```lua
VBO:DumpDefinition() -> nil
```

**Returns**

- `nil`

### VBO:CopyTo {#VBO:CopyTo}
*function*

Copy the contents of the VBO to another VBO.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1487-L1496" target="_blank">source</a>]

Destination VBO is expected to have sufficient allocation size, otherwise the copying will gracefully fail.

```lua
VBO:CopyTo(VBO, integer) -> boolean
```

**Parameters**

- `destVBO` [`VBO`](#VBO)
- `copySizeInBytes` `integer`

**Returns**

- `success` `boolean`

### VBO:GetID {#VBO:GetID}
*function*

Gets the OpenGL Buffer ID

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBOImpl.cpp#L1526-L1530" target="_blank">source</a>]

```lua
VBO:GetID() -> integer
```

**Returns**

- `bufferID` `integer`
