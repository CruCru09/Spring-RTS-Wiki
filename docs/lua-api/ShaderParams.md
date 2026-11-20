---
title: "ShaderParams"
tags:
  - Lua-API
---

## ShaderParams {#ShaderParams}
*class*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L572-L622" target="_blank">source</a>]

**Fields**

- <span id="ShaderParams.vertex"></span> `ShaderParams.vertex` `string?` — 
The "Vertex" or vertex-shader is your GLSL-Code as string, its written in a
C-Dialect.  This shader is busy deforming the geometry of a unit but it can
not create new polygons. Use it for waves, wobbling surfaces etc.
- <span id="ShaderParams.tcs"></span> `ShaderParams.tcs` `string?` — The "TCS" or Tesselation Control Shader controls how much tessellation a
particular patch gets; it also defines the size of a patch, thus allowing it
to augment data. It can also filter vertex data taken from the vertex shader.
The main purpose of the TCS is to feed the tessellation levels to the
Tessellation primitive generator stage, as well as to feed patch data (as its
output values) to the Tessellation Evaluation Shader stage.
- <span id="ShaderParams.tes"></span> `ShaderParams.tes` `string?` — The "TES" or Tesselation Evaluation Shader takes the abstract patch generated
by the tessellation primitive generation stage, as well as the actual vertex
data for the entire patch, and generates a particular vertex from it. Each
TES invocation generates a single vertex. It can also take per-patch data
provided by the Tessellation Control Shader.
- <span id="ShaderParams.geometry"></span> `ShaderParams.geometry` `string?` — The "Geometry" or Geometry-shader can create new vertices and vertice-stripes
from points.
- <span id="ShaderParams.fragment"></span> `ShaderParams.fragment` `string?` — The "Fragment" or Fragment-shader (sometimes called pixel-Shader) is post
processing the already rendered picture (for example drawing stars on the
sky).

Remember textures are not always 2 dimensional pictures. They can contain
information about the depth, or the third value marks areas and the strength
at which these are processed.
- <span id="ShaderParams.uniform"></span> `ShaderParams.uniform` `UniformParam<number>?`
- <span id="ShaderParams.uniformInt"></span> `ShaderParams.uniformInt` `UniformParam<integer>?`
- <span id="ShaderParams.uniformFloat"></span> `ShaderParams.uniformFloat` `UniformParam<number>?`
- <span id="ShaderParams.uniformMatrix"></span> `ShaderParams.uniformMatrix` `UniformParam<number>?`
- <span id="ShaderParams.geoInputType"></span> `ShaderParams.geoInputType` `integer?` — inType
- <span id="ShaderParams.geoOutputType"></span> `ShaderParams.geoOutputType` `integer?` — outType
- <span id="ShaderParams.geoOutputVerts"></span> `ShaderParams.geoOutputVerts` `integer?` — maxVerts
- <span id="ShaderParams.definitions"></span> `ShaderParams.definitions` `string?` — string of shader #defines"
