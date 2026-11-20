---
title: "gl"
tags:
  - Lua-API
---

## gl {#gl}
*table*

Callouts for OpenGL API

Only setters and getters for OpenGL usage in Recoil, see [GL](GL-enum.md#GL) for constants.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L89-L95" target="_blank">source</a>]

**See:** [GL](GL-enum.md#GL)

**Members**

### gl.CreateFBO {#gl.CreateFBO}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L468-L472" target="_blank">source</a>]

```lua
gl.CreateFBO(FBODescription) -> FBO
```

**Parameters**

- `fboDesc` [`FBODescription`](FBODescription.md#FBODescription)

**Returns**

- `fbo` [`FBO`](FBO.md#FBO)

### gl.DeleteFBO {#gl.DeleteFBO}
*function*

This doesn't delete the attached objects!

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L543-L548" target="_blank">source</a>]

```lua
gl.DeleteFBO(FBO) -> nil
```

**Parameters**

- `fbo` [`FBO`](FBO.md#FBO)

### gl.IsValidFBO {#gl.IsValidFBO}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L561-L567" target="_blank">source</a>]

```lua
gl.IsValidFBO(FBO, GL?) -> boolean, GL?
```

**Parameters**

- `fbo` [`FBO`](FBO.md#FBO)
- `target` `GL?`

**Returns**

- `valid` `boolean`
- `status` `GL?`

### gl.ActiveFBO {#gl.ActiveFBO}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L602-L607" target="_blank">source</a>]

```lua
gl.ActiveFBO(FBO, fun(...), [any, ]*) -> nil
```

**Parameters**

- `fbo` [`FBO`](FBO.md#FBO)
- `func` `fun(...)`
- `...` `any` — args

### gl.ActiveFBO (overload 1) {#gl.ActiveFBO-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L608-L614" target="_blank">source</a>]

```lua
gl.ActiveFBO(FBO, GL?, fun(...), [any, ]*) -> nil
```

**Parameters**

- `fbo` [`FBO`](FBO.md#FBO)
- `target` `GL?`
- `func` `fun(...)`
- `...` `any` — args

### gl.RawBindFBO {#gl.RawBindFBO}
*function*

Bind default or specified via rawFboId numeric id of FBO

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L678-L686" target="_blank">source</a>]

```lua
gl.RawBindFBO(nil, GL?, integer?) -> nil
```

**Parameters**

- `fbo` `nil`
- `target` `GL?` — (Default: `GL_FRAMEBUFFER_EXT`)
- `rawFboId` `integer?` — (Default: `0`)

**Returns**

- `nil`

### gl.RawBindFBO (overload 1) {#gl.RawBindFBO-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L687-L692" target="_blank">source</a>]

```lua
gl.RawBindFBO(FBO, GL?) -> integer
```

**Parameters**

- `fbo` [`FBO`](FBO.md#FBO)
- `target` `GL?` — (Default: `fbo.target`)

**Returns**

- `previouslyBoundRawFboId` `integer`

### gl.BlitFBO {#gl.BlitFBO}
*function*

needs `GLAD_GL_EXT_framebuffer_blit`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L720-L733" target="_blank">source</a>]

```lua
gl.BlitFBO(integer, integer, integer, integer, integer, integer, integer, integer, GL?, GL?) -> nil
```

**Parameters**

- `x0Src` `integer`
- `y0Src` `integer`
- `x1Src` `integer`
- `y1Src` `integer`
- `x0Dst` `integer`
- `y0Dst` `integer`
- `x1Dst` `integer`
- `y1Dst` `integer`
- `mask` `GL?` — (Default: GL_COLOR_BUFFER_BIT)
- `filter` `GL?` — (Default: GL_NEAREST)

### gl.BlitFBO (overload 1) {#gl.BlitFBO-1}
*function*

needs `GLAD_GL_EXT_framebuffer_blit`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L734-L749" target="_blank">source</a>]

```lua
gl.BlitFBO(FBO, integer, integer, integer, integer, FBO, integer, integer, integer, integer, GL?, GL?) -> nil
```

**Parameters**

- `fboSrc` [`FBO`](FBO.md#FBO)
- `x0Src` `integer`
- `y0Src` `integer`
- `x1Src` `integer`
- `y1Src` `integer`
- `fboDst` [`FBO`](FBO.md#FBO)
- `x0Dst` `integer`
- `y0Dst` `integer`
- `x1Dst` `integer`
- `y1Dst` `integer`
- `mask` `GL?` — (Default: GL_COLOR_BUFFER_BIT)
- `filter` `GL?` — (Default: GL_NEAREST)

### gl.ClearAttachmentFBO {#gl.ClearAttachmentFBO}
*function*

needs `Platform.glVersionNum >= 30`
Clears the "attachment" of the currently bound FBO type "target" with "clearValues"

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFBOs.cpp#L819-L830" target="_blank">source</a>]

```lua
gl.ClearAttachmentFBO(GL?, (GL|Attachment), number?, number?, number?, number?) -> boolean
```

**Parameters**

- `target` `GL?` — (Default: [GL.FRAMEBUFFER](GL-enum.md#GL.FRAMEBUFFER))
- `attachment` `(GL|Attachment)` — (e.g. `"color0"` or [GL.COLOR_ATTACHMENT0](GL-enum.md#GL.COLOR_ATTACHMENT0))
- `clearValue0` `number?` — (Default: `0`)
- `clearValue1` `number?` — (Default: `0`)
- `clearValue2` `number?` — (Default: `0`)
- `clearValue3` `number?` — (Default: `0`)

**Returns**

- `success` `boolean`

### gl.LoadFont {#gl.LoadFont}
*function*

Load a font from a file.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L195-L203" target="_blank">source</a>]

```lua
gl.LoadFont(string, integer?, integer?, number?) -> LuaFont
```

**Parameters**

- `fontFile` `string`
- `size` `integer?`
- `outlineWidth` `integer?`
- `outlineWeight` `number?`

**Returns**

- `font` [`LuaFont`](LuaFont.md#LuaFont)

### gl.DeleteFont {#gl.DeleteFont}
*function*

Delete a font object.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L220-L224" target="_blank">source</a>]

```lua
gl.DeleteFont(LuaFont) -> nil
```

**Parameters**

- `font` [`LuaFont`](LuaFont.md#LuaFont)

### gl.AddFallbackFont {#gl.AddFallbackFont}
*function*

Adds a fallback font for the font rendering engine.

Fonts added first will have higher priority.
When a glyph isn't found when rendering a font, the fallback fonts
will be searched first, otherwise os fonts will be used.

The application should listen for the unsynced 'FontsChanged' callin so
modules can clear any already reserved display lists or other relevant
caches.

Note the callin won't be executed at the time of calling this method,
but later, on the Update cycle (before other Update and Draw callins).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L231-L247" target="_blank">source</a>]

```lua
gl.AddFallbackFont(string) -> boolean
```

**Parameters**

- `filePath` `string` — VFS path to the file, for example "fonts/myfont.ttf". Uses VFS.RAW_FIRST access mode.

**Returns**

- `success` `boolean`

### gl.ClearFallbackFonts {#gl.ClearFallbackFonts}
*function*

Clears all fallback fonts.

See the note at 'AddFallbackFont' about the 'FontsChanged' callin,
it also applies when calling this method.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L259-L266" target="_blank">source</a>]

```lua
gl.ClearFallbackFonts() -> nil
```

**Returns**

- `nil`

### gl.HasExtension {#gl.HasExtension}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1154-L1158" target="_blank">source</a>]

```lua
gl.HasExtension(string) -> boolean
```

**Parameters**

- `ext` `string`

**Returns**

- `boolean`

### gl.GetNumber {#gl.GetNumber}
*function*

Get the value or values of a selected parameter.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1166-L1173" target="_blank">source</a>]

```lua
gl.GetNumber(GL, integer?) -> number ...
```

**Parameters**

- `pname` [`GL`](GL-enum.md#GL)
- `count` `integer?` — (Default: `1`) Number of values to return, in range [1, 64].

**Returns**

- `number ...`

### gl.GetString {#gl.GetString}
*function*

Get a string describing the current OpenGL connection.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1191-L1196" target="_blank">source</a>]

```lua
gl.GetString(GL) -> string
```

**Parameters**

- `pname` [`GL`](GL-enum.md#GL)

**Returns**

- `value` `string` — `"[NULL]"` if the driver returns no string for `pname`.

### gl.GetScreenViewTrans {#gl.GetScreenViewTrans}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1212-L1217" target="_blank">source</a>]

```lua
gl.GetScreenViewTrans() -> number, number, number
```

**Returns**

- `x` `number`
- `y` `number`
- `z` `number`

### gl.GetViewSizes {#gl.GetViewSizes}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1227-L1231" target="_blank">source</a>]

```lua
gl.GetViewSizes() -> integer, integer
```

**Returns**

- `x` `integer`
- `y` `integer`

### gl.GetViewRange {#gl.GetViewRange}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1240-L1246" target="_blank">source</a>]

```lua
gl.GetViewRange() -> number, number, number, number
```

**Returns**

- `nearPlaneDist` `number`
- `farPlaneDist` `number`
- `minViewRange` `number`
- `maxViewRange` `number`

### gl.SlaveMiniMap {#gl.SlaveMiniMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1262-L1265" target="_blank">source</a>]

```lua
gl.SlaveMiniMap(boolean) -> nil
```

**Parameters**

- `newMode` `boolean`

### gl.ConfigMiniMap {#gl.ConfigMiniMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1277-L1283" target="_blank">source</a>]

```lua
gl.ConfigMiniMap(integer, integer, integer, integer) -> nil
```

**Parameters**

- `px` `integer`
- `py` `integer`
- `sx` `integer`
- `sy` `integer`

### gl.DrawMiniMap {#gl.DrawMiniMap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1299-L1302" target="_blank">source</a>]

```lua
gl.DrawMiniMap(boolean?) -> nil
```

**Parameters**

- `defaultTransform` `boolean?` — (Default: `true`)

### gl.DrawMiniMapIcons {#gl.DrawMiniMapIcons}
*function*

Draws all unit icons visible to the given perspective (as on the minimap: team
colors, radar dots, LOS rules, ghost dimming) for a map-space rectangle, without
involving the actual minimap.

The rectangle is mapped onto the unit square under the current transform:
(left,top) -> (0,0), (right,bottom) -> (1,1). Callers position, scale, rotate or
flip the result via their own matrices, e.g. inside gl.RenderToTexture; when rotating,
also pass the angle as `rotation` so the icons stay upright. Blending, scissor and
viewport state are left to the caller.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1333-L1354" target="_blank">source</a>]

```lua
gl.DrawMiniMapIcons(number, number, number, number, number, integer?, boolean?, boolean?, number?) -> nil
```

**Parameters**

- `left` `number` — map-space rectangle edges in elmos; left < right and top < bottom (top = smaller z) are required, mirror via your own transform instead
- `top` `number`
- `right` `number`
- `bottom` `number`
- `iconSize` `number` — base icon half-size in elmos, scaled per icon by its icontypes.lua size
- `allyTeam` `integer?` — (Default: your allyTeam) perspective to render; other allyteams require a full-read handle
- `fullView` `boolean?` — (Default: true when spectating in full view with a full-read handle) draw every unit at its true position; true requires a full-read handle, false is always allowed
- `highlightSelected` `boolean?` — (Default: true) draw the local player's selected units white. Other players' selections are unknown to the engine — when rendering another perspective, pass false and overlay that viewer's selection yourself
- `rotation` `number?` — (Default: 0) counter-clockwise screen rotation in radians that you apply to the result, with the rectangle drawn minimap-style before it ((left,top) at the top-left). Each icon is turned back by it to stay upright and icons stack by the rotated screen vertical; positions are left to your transform. For a minimap replacement pass Spring.GetMiniMapRotation()

### gl.BeginText {#gl.BeginText}
*function*

Begin a block of text commands.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1421-L1435" target="_blank">source</a>]

Text can be drawn without Start/End, but when doing several operations it's more optimal
if done inside a block.

Also allows disabling automatic setting of the blend mode. Otherwise the font will always print
with `BlendFunc(GL.SRC_ALPHA, GL.ONE_MINUS_SRC_ALPHA)`.

**See:** [gl.BlendFuncSeparate](gl.md#gl.BlendFuncSeparate)

```lua
gl.BeginText(boolean?) -> nil
```

**Parameters**

- `userDefinedBlending` `boolean?` — When `true` doesn't set the gl.BlendFunc automatically. Defaults to `false`.

### gl.EndText {#gl.EndText}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1445-L1447" target="_blank">source</a>]

```lua
gl.EndText() -> nil
```

### gl.Text {#gl.Text}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1455-L1480" target="_blank">source</a>]

```lua
gl.Text(string, number, number, number?, string?) -> nil
```

**Parameters**

- `text` `string`
- `x` `number`
- `y` `number`
- `size` `number?`
- `options` `string?` — concatenated string of option characters.

- horizontal alignment:
- 'c' = center
- 'r' = right
- vertical alignment:
- 'a' = ascender
- 't' = top
- 'v' = vertical center
- 'x' = baseline
- 'b' = bottom
- 'd' = descender
- decorations:
- 'o' = black outline
- 'O' = white outline
- 's' = shadow
- other:
- 'n' = don't round vertex coords to nearest integer (font may get blurry)

**Returns**

- `nil`

### gl.GetTextWidth {#gl.GetTextWidth}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1536-L1540" target="_blank">source</a>]

```lua
gl.GetTextWidth(string) -> number
```

**Parameters**

- `text` `string`

**Returns**

- `width` `number`

### gl.GetTextHeight {#gl.GetTextHeight}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1551-L1557" target="_blank">source</a>]

```lua
gl.GetTextHeight(string) -> number, number, integer
```

**Parameters**

- `text` `string`

**Returns**

- `height` `number`
- `descender` `number`
- `lines` `integer`

### gl.Unit {#gl.Unit}
*function*

Draw the unit, applying transform.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1752-L1761" target="_blank">source</a>]

```lua
gl.Unit(UnitID, boolean?, integer?, boolean?, boolean?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `doRawDraw` `boolean?` — (Default: `false`)
- `useLuaMat` `integer?`
- `noLuaCall` `boolean?` — (Default: `false`) Skip the `DrawUnit` callin.
- `fullModel` `boolean?` — (Default: `true`)

### gl.UnitRaw {#gl.UnitRaw}
*function*

Draw the unit without applying transform.

Also skips the `DrawUnit` callin by default so any
recursion is blocked.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1764-L1776" target="_blank">source</a>]

```lua
gl.UnitRaw(UnitID, boolean?, integer?, boolean?, boolean?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `doRawDraw` `boolean?` — (Default: `false`)
- `useLuaMat` `integer?`
- `noLuaCall` `boolean?` — (Default: `true`) Skip the `DrawUnit` callin.
- `fullModel` `boolean?` — (Default: `true`)

### gl.UnitTextures {#gl.UnitTextures}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1779-L1783" target="_blank">source</a>]

```lua
gl.UnitTextures(UnitID, boolean) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `push` `boolean` — If `true`, push the render state; if `false`, pop it.

### gl.UnitShape {#gl.UnitShape}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1791-L1798" target="_blank">source</a>]

```lua
gl.UnitShape(UnitDefID, TeamID, boolean?, boolean?, boolean?) -> nil
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `teamID` [`TeamID`](Aliases.md#TeamID)
- `rawState` `boolean?` — (Default: `true`)
- `toScreen` `boolean?` — (Default: `false`)
- `opaque` `boolean?` — (Default: `true`) If `true`, draw opaque; if `false`, draw alpha.

### gl.UnitShapeTextures {#gl.UnitShapeTextures}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1806-L1810" target="_blank">source</a>]

```lua
gl.UnitShapeTextures(UnitDefID, boolean) -> nil
```

**Parameters**

- `unitDefID` [`UnitDefID`](Aliases.md#UnitDefID)
- `push` `boolean` — If `true`, push the render state; if `false`, pop it.

### gl.UnitMultMatrix {#gl.UnitMultMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1819-L1822" target="_blank">source</a>]

```lua
gl.UnitMultMatrix(UnitID) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)

### gl.UnitPiece {#gl.UnitPiece}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1837-L1841" target="_blank">source</a>]

```lua
gl.UnitPiece(UnitID, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceID` `integer`

### gl.UnitPieceMatrix {#gl.UnitPieceMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1848-L1852" target="_blank">source</a>]

```lua
gl.UnitPieceMatrix(UnitID, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceID` `integer`

### gl.UnitPieceMultMatrix {#gl.UnitPieceMultMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1855-L1859" target="_blank">source</a>]

```lua
gl.UnitPieceMultMatrix(UnitID, integer) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `pieceID` `integer`

### gl.Feature {#gl.Feature}
*function*

Draw the feature, applying transform.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1920-L1928" target="_blank">source</a>]

```lua
gl.Feature(FeatureID, boolean?, integer?, boolean?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `doRawDraw` `boolean?` — (Default: `false`)
- `useLuaMat` `integer?`
- `noLuaCall` `boolean?` — (Default: `false`) Skip the `DrawFeature` callin.

### gl.FeatureRaw {#gl.FeatureRaw}
*function*

Draw the unit without applying transform.

Also skips the `DrawFeature` callin by default so any
recursion is blocked.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1931-L1942" target="_blank">source</a>]

```lua
gl.FeatureRaw(FeatureID, boolean?, integer?, boolean?) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `doRawDraw` `boolean?` — (Default: `false`)
- `useLuaMat` `integer?`
- `noLuaCall` `boolean?` — (Default: `true`) Skip the `DrawFeature` callin.

### gl.FeatureTextures {#gl.FeatureTextures}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1945-L1949" target="_blank">source</a>]

```lua
gl.FeatureTextures(FeatureID, boolean) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `push` `boolean` — If `true`, push the render state; if `false`, pop it.

### gl.FeatureShape {#gl.FeatureShape}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1957-L1964" target="_blank">source</a>]

```lua
gl.FeatureShape(FeatureDefID, TeamID, boolean?, boolean?, boolean?) -> nil
```

**Parameters**

- `featureDefID` [`FeatureDefID`](Aliases.md#FeatureDefID)
- `teamID` [`TeamID`](Aliases.md#TeamID)
- `rawState` `boolean?` — (Default: `true`)
- `toScreen` `boolean?` — (Default: `false`)
- `opaque` `boolean?` — (Default: `true`) If `true`, draw opaque; if `false`, draw alpha.

### gl.FeatureShapeTextures {#gl.FeatureShapeTextures}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1972-L1976" target="_blank">source</a>]

```lua
gl.FeatureShapeTextures(FeatureDefID, boolean) -> nil
```

**Parameters**

- `featureDefID` [`FeatureDefID`](Aliases.md#FeatureDefID)
- `push` `boolean` — If `true`, push the render state; if `false`, pop it.

### gl.FeatureMultMatrix {#gl.FeatureMultMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L1985-L1988" target="_blank">source</a>]

```lua
gl.FeatureMultMatrix(FeatureID) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)

### gl.FeaturePiece {#gl.FeaturePiece}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2003-L2007" target="_blank">source</a>]

```lua
gl.FeaturePiece(FeatureID, integer) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceID` `integer`

### gl.FeaturePieceMatrix {#gl.FeaturePieceMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2015-L2019" target="_blank">source</a>]

```lua
gl.FeaturePieceMatrix(FeatureID, integer) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceID` `integer`

### gl.FeaturePieceMultMatrix {#gl.FeaturePieceMultMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2023-L2027" target="_blank">source</a>]

```lua
gl.FeaturePieceMultMatrix(FeatureID, integer) -> nil
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `pieceID` `integer`

### gl.DrawListAtUnit {#gl.DrawListAtUnit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2040-L2052" target="_blank">source</a>]

```lua
gl.DrawListAtUnit(UnitID, integer, boolean?, number?, number?, number?, number?, number?, number?, number?) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `listIndex` `integer`
- `useMidPos` `boolean?` — (Default: `true`)
- `scaleX` `number?` — (Default: `1.0`)
- `scaleY` `number?` — (Default: `1.0`)
- `scaleZ` `number?` — (Default: `1.0`)
- `degrees` `number?` — (Default: `0.0`)
- `rotX` `number?` — (Default: `0.0`)
- `rotY` `number?` — (Default: `1.0`)
- `rotZ` `number?` — (Default: `0.0`)

### gl.DrawFuncAtUnit {#gl.DrawFuncAtUnit}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2097-L2103" target="_blank">source</a>]

```lua
gl.DrawFuncAtUnit(UnitID, boolean?, unknown, [any, ]*) -> nil
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `useMidPos` `boolean?` — (Default: `true`)
- `fun` `unknown`
- `...` `any` — Arguments passed to function.

### gl.DrawGroundCircle {#gl.DrawGroundCircle}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2140-L2147" target="_blank">source</a>]

```lua
gl.DrawGroundCircle(number, number, number, number, integer) -> nil
```

**Parameters**

- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `radius` `number`
- `resolution` `integer`

### gl.DrawGroundCircle (overload 1) {#gl.DrawGroundCircle-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2148-L2158" target="_blank">source</a>]

```lua
gl.DrawGroundCircle(number, number, number, number, integer, number, number?, WeaponDefID?) -> nil
```

**Parameters**

- `posX` `number`
- `posY` `number`
- `posZ` `number`
- `radius` `number`
- `resolution` `integer`
- `slope` `number`
- `gravity` `number?`
- `weaponDefID` `WeaponDefID?`

### gl.DrawGroundQuad {#gl.DrawGroundQuad}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2199-L2207" target="_blank">source</a>]

```lua
gl.DrawGroundQuad(number, number, number, number, nil, boolean?) -> nil
```

**Parameters**

- `x0` `number`
- `z0` `number`
- `x1` `number`
- `z1` `number`
- `useNorm` `nil` — No longer used.
- `useTxcd` `boolean?` — (Default: `false`)

### gl.DrawGroundQuad (overload 1) {#gl.DrawGroundQuad-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2208-L2219" target="_blank">source</a>]

```lua
gl.DrawGroundQuad(number, number, number, number, nil, number, number, number, number) -> nil
```

**Parameters**

- `x0` `number`
- `z0` `number`
- `x1` `number`
- `z1` `number`
- `useNorm` `nil` — No longer used.
- `tu0` `number`
- `tv0` `number`
- `tu1` `number`
- `tv1` `number`

### gl.Shape {#gl.Shape}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2409-L2413" target="_blank">source</a>]

```lua
gl.Shape(GL, VertexData[]) -> nil
```

**Parameters**

- `type` [`GL`](GL-enum.md#GL)
- `vertices` `VertexData[]`

### gl.BeginEnd {#gl.BeginEnd}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2455-L2460" target="_blank">source</a>]

```lua
gl.BeginEnd(GL, unknown, [any, ]*) -> nil
```

**Parameters**

- `primMode` [`GL`](GL-enum.md#GL)
- `fun` `unknown`
- `...` `any` — Arguments passed to function.

### gl.Vertex {#gl.Vertex}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2492-L2495" target="_blank">source</a>]

```lua
gl.Vertex(xy) -> nil
```

**Parameters**

- `v` [`xy`](xy.md#xy)

### gl.Vertex (overload 1) {#gl.Vertex-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2496-L2499" target="_blank">source</a>]

```lua
gl.Vertex(xyz) -> nil
```

**Parameters**

- `v` [`xyz`](xyz.md#xyz)

### gl.Vertex (overload 2) {#gl.Vertex-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2500-L2503" target="_blank">source</a>]

```lua
gl.Vertex(xyzw) -> nil
```

**Parameters**

- `v` [`xyzw`](xyzw.md#xyzw)

### gl.Vertex (overload 3) {#gl.Vertex-3}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2504-L2510" target="_blank">source</a>]

```lua
gl.Vertex(number, number, number?, number?) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number?`
- `w` `number?`

### gl.Normal {#gl.Normal}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2574-L2577" target="_blank">source</a>]

```lua
gl.Normal(xyz) -> nil
```

**Parameters**

- `v` [`xyz`](xyz.md#xyz)

### gl.Normal (overload 1) {#gl.Normal-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2578-L2583" target="_blank">source</a>]

```lua
gl.Normal(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`

### gl.TexCoord {#gl.TexCoord}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2622-L2625" target="_blank">source</a>]

```lua
gl.TexCoord((number)) -> nil
```

**Parameters**

- `coord` `(number)`

### gl.TexCoord (overload 1) {#gl.TexCoord-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2626-L2629" target="_blank">source</a>]

```lua
gl.TexCoord(xy) -> nil
```

**Parameters**

- `coord` [`xy`](xy.md#xy)

### gl.TexCoord (overload 2) {#gl.TexCoord-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2630-L2633" target="_blank">source</a>]

```lua
gl.TexCoord(xyz) -> nil
```

**Parameters**

- `coord` [`xyz`](xyz.md#xyz)

### gl.TexCoord (overload 3) {#gl.TexCoord-3}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2634-L2637" target="_blank">source</a>]

```lua
gl.TexCoord(xyzw) -> nil
```

**Parameters**

- `coord` [`xyzw`](xyzw.md#xyzw)

### gl.TexCoord (overload 4) {#gl.TexCoord-4}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2638-L2644" target="_blank">source</a>]

```lua
gl.TexCoord(number, number?, number?, number?) -> nil
```

**Parameters**

- `s` `number`
- `t` `number?`
- `r` `number?`
- `q` `number?`

### gl.MultiTexCoord {#gl.MultiTexCoord}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2713-L2717" target="_blank">source</a>]

```lua
gl.MultiTexCoord(integer, (number)) -> nil
```

**Parameters**

- `texNum` `integer`
- `coord` `(number)`

### gl.MultiTexCoord (overload 1) {#gl.MultiTexCoord-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2718-L2722" target="_blank">source</a>]

```lua
gl.MultiTexCoord(integer, xy) -> nil
```

**Parameters**

- `texNum` `integer`
- `coord` [`xy`](xy.md#xy)

### gl.MultiTexCoord (overload 2) {#gl.MultiTexCoord-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2723-L2727" target="_blank">source</a>]

```lua
gl.MultiTexCoord(integer, xyz) -> nil
```

**Parameters**

- `texNum` `integer`
- `coord` [`xyz`](xyz.md#xyz)

### gl.MultiTexCoord (overload 3) {#gl.MultiTexCoord-3}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2728-L2732" target="_blank">source</a>]

```lua
gl.MultiTexCoord(integer, xyzw) -> nil
```

**Parameters**

- `texNum` `integer`
- `coord` [`xyzw`](xyzw.md#xyzw)

### gl.MultiTexCoord (overload 4) {#gl.MultiTexCoord-4}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2733-L2740" target="_blank">source</a>]

```lua
gl.MultiTexCoord(integer, number, number?, number?, number?) -> nil
```

**Parameters**

- `texNum` `integer`
- `s` `number`
- `t` `number?`
- `r` `number?`
- `q` `number?`

### gl.SecondaryColor {#gl.SecondaryColor}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2815-L2818" target="_blank">source</a>]

```lua
gl.SecondaryColor(rgb) -> nil
```

**Parameters**

- `color` [`rgb`](rgb.md#rgb)

### gl.SecondaryColor (overload 1) {#gl.SecondaryColor-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2819-L2824" target="_blank">source</a>]

```lua
gl.SecondaryColor(number, number, number) -> nil
```

**Parameters**

- `r` `number`
- `g` `number`
- `b` `number`

### gl.FogCoord {#gl.FogCoord}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2863-L2866" target="_blank">source</a>]

```lua
gl.FogCoord(number) -> nil
```

**Parameters**

- `coord` `number`

### gl.EdgeFlag {#gl.EdgeFlag}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2878-L2881" target="_blank">source</a>]

```lua
gl.EdgeFlag(boolean) -> nil
```

**Parameters**

- `flag` `boolean`

### gl.Rect {#gl.Rect}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2896-L2902" target="_blank">source</a>]

```lua
gl.Rect(number, number, number, number) -> nil
```

**Parameters**

- `x1` `number`
- `y1` `number`
- `x2` `number`
- `y2` `number`

### gl.TexRect {#gl.TexRect}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2915-L2923" target="_blank">source</a>]

```lua
gl.TexRect(number, number, number, number, boolean?, boolean?) -> nil
```

**Parameters**

- `x1` `number`
- `y1` `number`
- `x2` `number`
- `y2` `number`
- `flipSCoords` `boolean?`
- `flipTCoords` `boolean?`

### gl.TexRect (overload 1) {#gl.TexRect-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2924-L2934" target="_blank">source</a>]

```lua
gl.TexRect(number, number, number, number, number, number, number, number) -> nil
```

**Parameters**

- `x1` `number`
- `y1` `number`
- `x2` `number`
- `y2` `number`
- `s1` `number`
- `t1` `number`
- `s2` `number`
- `t2` `number`

### gl.DispatchCompute {#gl.DispatchCompute}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L2990-L2996" target="_blank">source</a>]

```lua
gl.DispatchCompute(integer?, integer, integer, integer?) -> nil
```

**Parameters**

- `numGroupX` `integer?`
- `numGroupY` `integer`
- `numGroupZ` `integer`
- `barriers` `integer?` — (Default: `0`)

### gl.MemoryBarrier {#gl.MemoryBarrier}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3029-L3032" target="_blank">source</a>]

```lua
gl.MemoryBarrier(integer?) -> nil
```

**Parameters**

- `barriers` `integer?` — (Default: `4`)

### gl.Color {#gl.Color}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3050-L3056" target="_blank">source</a>]

```lua
gl.Color(number, number, number, number?) -> nil
```

**Parameters**

- `r` `number` — Red.
- `g` `number` — Green.
- `b` `number` — Blue.
- `a` `number?` — (Default: `1.0`) Alpha.

### gl.Color (overload 1) {#gl.Color-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3057-L3060" target="_blank">source</a>]

```lua
gl.Color(rgba) -> nil
```

**Parameters**

- `color` [`rgba`](rgba.md#rgba) — Color with alpha.

### gl.Color (overload 2) {#gl.Color-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3061-L3064" target="_blank">source</a>]

```lua
gl.Color(rgb) -> nil
```

**Parameters**

- `color` [`rgb`](rgb.md#rgb) — Color.

### gl.Material {#gl.Material}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3113-L3116" target="_blank">source</a>]

```lua
gl.Material(Material) -> nil
```

**Parameters**

- `material` [`Material`](Material.md#Material)

### gl.ResetState {#gl.ResetState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3186-L3188" target="_blank">source</a>]

```lua
gl.ResetState() -> nil
```

### gl.ResetMatrices {#gl.ResetMatrices}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3197-L3199" target="_blank">source</a>]

```lua
gl.ResetMatrices() -> nil
```

### gl.Lighting {#gl.Lighting}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3215-L3218" target="_blank">source</a>]

```lua
gl.Lighting(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.ShadeModel {#gl.ShadeModel}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3232-L3235" target="_blank">source</a>]

```lua
gl.ShadeModel(GL) -> nil
```

**Parameters**

- `model` [`GL`](GL-enum.md#GL)

### gl.Scissor {#gl.Scissor}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3244-L3247" target="_blank">source</a>]

```lua
gl.Scissor(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.Scissor (overload 1) {#gl.Scissor-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3248-L3254" target="_blank">source</a>]

```lua
gl.Scissor(integer, integer, integer, integer) -> nil
```

**Parameters**

- `x` `integer`
- `y` `integer`
- `w` `integer`
- `h` `integer`

### gl.Viewport {#gl.Viewport}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3285-L3291" target="_blank">source</a>]

```lua
gl.Viewport(integer, integer, integer, integer) -> nil
```

**Parameters**

- `x` `integer`
- `y` `integer`
- `w` `integer`
- `h` `integer`

### gl.ColorMask {#gl.ColorMask}
*function*

Enable or disable writing of frame buffer color components.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3308-L3312" target="_blank">source</a>]

```lua
gl.ColorMask(boolean) -> nil
```

**Parameters**

- `rgba` `boolean`

### gl.ColorMask (overload 1) {#gl.ColorMask-1}
*function*

Enable or disable writing of frame buffer color components.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3313-L3320" target="_blank">source</a>]

```lua
gl.ColorMask(boolean, boolean, boolean, boolean) -> nil
```

**Parameters**

- `red` `boolean`
- `green` `boolean`
- `blue` `boolean`
- `alpha` `boolean`

### gl.DepthMask {#gl.DepthMask}
*function*

Enable or disable writing into the depth buffer.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3344-L3348" target="_blank">source</a>]

```lua
gl.DepthMask(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.DepthTest {#gl.DepthTest}
*function*

Enable or disable depth test.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3361-L3365" target="_blank">source</a>]

```lua
gl.DepthTest(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.DepthTest (overload 1) {#gl.DepthTest-1}
*function*

Enable depth test and specify the depth comparison function.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3366-L3375" target="_blank">source</a>]

```lua
gl.DepthTest(GL) -> nil
```

**Parameters**

- `depthFunction` [`GL`](GL-enum.md#GL)

### gl.DepthClamp {#gl.DepthClamp}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3403-L3406" target="_blank">source</a>]

```lua
gl.DepthClamp(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.Culling {#gl.Culling}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3420-L3423" target="_blank">source</a>]

```lua
gl.Culling(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.Culling (overload 1) {#gl.Culling-1}
*function*

Enable culling and set culling mode.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3424-L3432" target="_blank">source</a>]

```lua
gl.Culling(GL) -> nil
```

**Parameters**

- `mode` [`GL`](GL-enum.md#GL)

### gl.LogicOp {#gl.LogicOp}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3461-L3464" target="_blank">source</a>]

```lua
gl.LogicOp(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.LogicOp (overload 1) {#gl.LogicOp-1}
*function*

Specify a logical pixel operation for rendering.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3465-L3477" target="_blank">source</a>]

```lua
gl.LogicOp(GL) -> nil
```

**Parameters**

- `opCode` [`GL`](GL-enum.md#GL)

### gl.Fog {#gl.Fog}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3505-L3508" target="_blank">source</a>]

```lua
gl.Fog(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.Blending {#gl.Blending}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3523-L3526" target="_blank">source</a>]

```lua
gl.Blending(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.Blending (overload 1) {#gl.Blending-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3527-L3530" target="_blank">source</a>]

```lua
gl.Blending(("add"|"alpha_add"|"alpha"|"reset"|"color"|"modulate"...)) -> nil
```

**Parameters**

- `mode` `("add"|"alpha_add"|"alpha"|"reset"|"color"|"modulate"...)`

### gl.Blending (overload 2) {#gl.Blending-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3531-L3535" target="_blank">source</a>]

```lua
gl.Blending(GL, GL) -> nil
```

**Parameters**

- `src` [`GL`](GL-enum.md#GL)
- `dst` [`GL`](GL-enum.md#GL)

### gl.BlendEquation {#gl.BlendEquation}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3598-L3601" target="_blank">source</a>]

```lua
gl.BlendEquation(GL) -> nil
```

**Parameters**

- `mode` [`GL`](GL-enum.md#GL)

### gl.BlendFunc {#gl.BlendFunc}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3611-L3615" target="_blank">source</a>]

```lua
gl.BlendFunc(GL, GL) -> nil
```

**Parameters**

- `src` [`GL`](GL-enum.md#GL)
- `dst` [`GL`](GL-enum.md#GL)

### gl.BlendEquationSeparate {#gl.BlendEquationSeparate}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3626-L3630" target="_blank">source</a>]

```lua
gl.BlendEquationSeparate(GL, GL) -> nil
```

**Parameters**

- `modeRGB` [`GL`](GL-enum.md#GL)
- `modeAlpha` [`GL`](GL-enum.md#GL)

### gl.BlendFuncSeparate {#gl.BlendFuncSeparate}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3641-L3647" target="_blank">source</a>]

```lua
gl.BlendFuncSeparate(GL, GL, GL, GL) -> nil
```

**Parameters**

- `srcRGB` [`GL`](GL-enum.md#GL)
- `dstRGB` [`GL`](GL-enum.md#GL)
- `srcAlpha` [`GL`](GL-enum.md#GL)
- `dstAlpha` [`GL`](GL-enum.md#GL)

### gl.AlphaTest {#gl.AlphaTest}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3660-L3663" target="_blank">source</a>]

```lua
gl.AlphaTest(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.AlphaTest (overload 1) {#gl.AlphaTest-1}
*function*

Specify the alpha test function.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3664-L3677" target="_blank">source</a>]

```lua
gl.AlphaTest(GL, number) -> nil
```

**Parameters**

- `func` [`GL`](GL-enum.md#GL)
- `ref` `number`

### gl.AlphaToCoverage {#gl.AlphaToCoverage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3701-L3704" target="_blank">source</a>]

```lua
gl.AlphaToCoverage(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.PolygonMode {#gl.PolygonMode}
*function*

Select polygon rasterization mode.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3722-L3738" target="_blank">source</a>]

```lua
gl.PolygonMode(GL, GL) -> nil
```

**Parameters**

- `face` [`GL`](GL-enum.md#GL)
- `mode` [`GL`](GL-enum.md#GL)

### gl.PolygonOffset {#gl.PolygonOffset}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3749-L3752" target="_blank">source</a>]

```lua
gl.PolygonOffset(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.PolygonOffset (overload 1) {#gl.PolygonOffset-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3753-L3764" target="_blank">source</a>]

```lua
gl.PolygonOffset(number, number) -> nil
```

**Parameters**

- `factor` `number`
- `units` `number`

### gl.StencilTest {#gl.StencilTest}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3796-L3799" target="_blank">source</a>]

```lua
gl.StencilTest(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.StencilMask {#gl.StencilMask}
*function*

Control the front and back writing of individual bits in the stencil planes.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3813-L3817" target="_blank">source</a>]

```lua
gl.StencilMask(integer) -> nil
```

**Parameters**

- `mask` `integer` — Specifies a bit mask to enable and disable writing of individual bits in the stencil planes. Initially, the mask is all `1`'s.

### gl.StencilFunc {#gl.StencilFunc}
*function*

Set front and back function and reference value for stencil testing.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3827-L3833" target="_blank">source</a>]

```lua
gl.StencilFunc(GL, integer, integer) -> nil
```

**Parameters**

- `func` [`GL`](GL-enum.md#GL) — Specifies the test function. Eight symbolic constants are valid: [GL.NEVER](GL-enum.md#GL.NEVER), [GL.LESS](GL-enum.md#GL.LESS), [GL.EQUAL](GL-enum.md#GL.EQUAL), [GL.LEQUAL](GL-enum.md#GL.LEQUAL), [GL.GREATER](GL-enum.md#GL.GREATER), [GL.NOTEQUAL](GL-enum.md#GL.NOTEQUAL), [GL.GEQUAL](GL-enum.md#GL.GEQUAL), and [GL.ALWAYS](GL-enum.md#GL.ALWAYS). The initial value is [GL.ALWAYS](GL-enum.md#GL.ALWAYS).
- `ref` `integer` — Specifies the reference value for the stencil test. `ref` is clamped to the range `[0, 2^n - 1]`, where `n` is the number of bitplanes in the stencil buffer. The initial value is `0`.
- `mask` `integer` — Specifies a mask that is ANDed with both the reference value and the stored stencil value when the test is done. The initial value is all `1`'s.

### gl.StencilOp {#gl.StencilOp}
*function*

Set front and back stencil test actions.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3845-L3851" target="_blank">source</a>]

```lua
gl.StencilOp(GL, GL, GL) -> nil
```

**Parameters**

- `fail` [`GL`](GL-enum.md#GL) — Specifies the action to take when the stencil test fails. Eight symbolic constants are valid: [GL.KEEP](GL-enum.md#GL.KEEP), [GL.ZERO](GL-enum.md#GL.ZERO), [GL.REPLACE](GL-enum.md#GL.REPLACE), [GL.INCR](GL-enum.md#GL.INCR), [GL.INCR_WRAP](GL-enum.md#GL.INCR_WRAP), [GL.DECR](GL-enum.md#GL.DECR), [GL.DECR_WRAP](GL-enum.md#GL.DECR_WRAP), and [GL.INVERT](GL-enum.md#GL.INVERT). The initial value is [GL.KEEP](GL-enum.md#GL.KEEP).
- `zfail` [`GL`](GL-enum.md#GL) — Specifies the stencil action when the stencil test passes, but the depth test fails. The initial value is [GL.KEEP](GL-enum.md#GL.KEEP).
- `zpass` [`GL`](GL-enum.md#GL) — Specifies the stencil action when both the stencil test and the depth test pass, or when the stencil test passes and either there is no depth buffer or depth testing is not enabled. The initial value is [GL.KEEP](GL-enum.md#GL.KEEP).

### gl.StencilMaskSeparate {#gl.StencilMaskSeparate}
*function*

Control the front and back writing of individual bits in the stencil planes.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3863-L3868" target="_blank">source</a>]

```lua
gl.StencilMaskSeparate(GL, integer) -> nil
```

**Parameters**

- `face` [`GL`](GL-enum.md#GL) — Specifies whether the front and/or back stencil writemask is updated. Three symbolic constants are accepted: [GL.FRONT](GL-enum.md#GL.FRONT), [GL.BACK](GL-enum.md#GL.BACK), and [GL.FRONT_AND_BACK](GL-enum.md#GL.FRONT_AND_BACK). The initial value is [GL.FRONT_AND_BACK](GL-enum.md#GL.FRONT_AND_BACK).
- `mask` `integer` — Specifies a bit mask to enable and disable writing of individual bits in the stencil planes. Initially, the mask is all `1`'s.

### gl.StencilFuncSeparate {#gl.StencilFuncSeparate}
*function*

Set front and/or back function and reference value for stencil testing.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3879-L3886" target="_blank">source</a>]

```lua
gl.StencilFuncSeparate(GL, GL, integer, integer) -> nil
```

**Parameters**

- `face` [`GL`](GL-enum.md#GL) — Specifies whether front and/or back stencil state is updated. Three symbolic constants are accepted: [GL.FRONT](GL-enum.md#GL.FRONT), [GL.BACK](GL-enum.md#GL.BACK), and [GL.FRONT_AND_BACK](GL-enum.md#GL.FRONT_AND_BACK). The initial value is [GL.FRONT_AND_BACK](GL-enum.md#GL.FRONT_AND_BACK).
- `func` [`GL`](GL-enum.md#GL) — Specifies the test function. Eight symbolic constants are valid: [GL.NEVER](GL-enum.md#GL.NEVER), [GL.LESS](GL-enum.md#GL.LESS), [GL.EQUAL](GL-enum.md#GL.EQUAL), [GL.LEQUAL](GL-enum.md#GL.LEQUAL), [GL.GREATER](GL-enum.md#GL.GREATER), [GL.NOTEQUAL](GL-enum.md#GL.NOTEQUAL), [GL.GEQUAL](GL-enum.md#GL.GEQUAL), and [GL.ALWAYS](GL-enum.md#GL.ALWAYS). The initial value is [GL.ALWAYS](GL-enum.md#GL.ALWAYS).
- `ref` `integer` — Specifies the reference value for the stencil test. `ref` is clamped to the range `[0, 2^n - 1]`, where `n` is the number of bitplanes in the stencil buffer. The initial value is `0`.
- `mask` `integer` — Specifies a mask that is ANDed with both the reference value and the stored stencil value when the test is done. The initial value is all `1`'s.

### gl.StencilOpSeparate {#gl.StencilOpSeparate}
*function*

Set front and/or back stencil test actions.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3899-L3906" target="_blank">source</a>]

```lua
gl.StencilOpSeparate(GL, GL, GL, GL) -> nil
```

**Parameters**

- `face` [`GL`](GL-enum.md#GL) — Specifies whether front and/or back stencil state is updated. Three symbolic constants are accepted: [GL.FRONT](GL-enum.md#GL.FRONT), [GL.BACK](GL-enum.md#GL.BACK), and [GL.FRONT_AND_BACK](GL-enum.md#GL.FRONT_AND_BACK). The initial value is [GL.FRONT_AND_BACK](GL-enum.md#GL.FRONT_AND_BACK).
- `fail` [`GL`](GL-enum.md#GL) — Specifies the action to take when the stencil test fails. Eight symbolic constants are valid: [GL.KEEP](GL-enum.md#GL.KEEP), [GL.ZERO](GL-enum.md#GL.ZERO), [GL.REPLACE](GL-enum.md#GL.REPLACE), [GL.INCR](GL-enum.md#GL.INCR), [GL.INCR_WRAP](GL-enum.md#GL.INCR_WRAP), [GL.DECR](GL-enum.md#GL.DECR), [GL.DECR_WRAP](GL-enum.md#GL.DECR_WRAP), and [GL.INVERT](GL-enum.md#GL.INVERT). The initial value is [GL.KEEP](GL-enum.md#GL.KEEP).
- `zfail` [`GL`](GL-enum.md#GL) — Specifies the stencil action when the stencil test passes, but the depth test fails. The initial value is [GL.KEEP](GL-enum.md#GL.KEEP).
- `zpass` [`GL`](GL-enum.md#GL) — Specifies the stencil action when both the stencil test and the depth test pass, or when the stencil test passes and either there is no depth buffer or depth testing is not enabled. The initial value is [GL.KEEP](GL-enum.md#GL.KEEP).

### gl.LineStipple {#gl.LineStipple}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3921-L3924" target="_blank">source</a>]

```lua
gl.LineStipple(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### gl.LineStipple (overload 1) {#gl.LineStipple-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3925-L3928" target="_blank">source</a>]

```lua
gl.LineStipple(string) -> nil
```

**Parameters**

- `ignoredString` `string` — The value of this string is ignored, but it still does something.

### gl.LineStipple (overload 2) {#gl.LineStipple-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3929-L3934" target="_blank">source</a>]

```lua
gl.LineStipple(integer, integer, integer?) -> nil
```

**Parameters**

- `factor` `integer`
- `pattern` `integer`
- `shift` `integer?`

### gl.LineWidth {#gl.LineWidth}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3984-L3987" target="_blank">source</a>]

```lua
gl.LineWidth(number) -> nil
```

**Parameters**

- `width` `number`

### gl.PointSize {#gl.PointSize}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L3998-L4001" target="_blank">source</a>]

```lua
gl.PointSize(number) -> nil
```

**Parameters**

- `size` `number`

### gl.PointSprite {#gl.PointSprite}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4012-L4017" target="_blank">source</a>]

```lua
gl.PointSprite(boolean, boolean?, boolean?) -> nil
```

**Parameters**

- `enable` `boolean`
- `enableCoordReplace` `boolean?`
- `coordOrigin` `boolean?` — `true` for upper left, `false` for lower left, otherwise no change.

### gl.PointParameter {#gl.PointParameter}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4046-L4054" target="_blank">source</a>]

```lua
gl.PointParameter(number, number, number, number?, number?, number?) -> nil
```

**Parameters**

- `atten0` `number`
- `atten1` `number`
- `atten2` `number`
- `sizeMin` `number?`
- `sizeMax` `number?`
- `sizeFade` `number?`

### gl.Texture {#gl.Texture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4082-L4087" target="_blank">source</a>]

```lua
gl.Texture(integer, boolean?) -> boolean
```

**Parameters**

- `texNum` `integer`
- `enable` `boolean?`

**Returns**

- `boolean`

### gl.Texture (overload 1) {#gl.Texture-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4088-L4092" target="_blank">source</a>]

```lua
gl.Texture(boolean) -> boolean
```

**Parameters**

- `enable` `boolean`

**Returns**

- `boolean`

### gl.Texture (overload 2) {#gl.Texture-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4093-L4098" target="_blank">source</a>]

```lua
gl.Texture(integer, string) -> boolean
```

**Parameters**

- `texNum` `integer`
- `image` `string`

**Returns**

- `boolean`

### gl.Texture (overload 3) {#gl.Texture-3}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4099-L4103" target="_blank">source</a>]

```lua
gl.Texture(string) -> boolean
```

**Parameters**

- `image` `string`

**Returns**

- `boolean`

### gl.CreateTexture {#gl.CreateTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4233-L4239" target="_blank">source</a>]

```lua
gl.CreateTexture(integer, integer, Texture) -> string?
```

**Parameters**

- `xsize` `integer`
- `ysize` `integer`
- `texture` [`Texture`](Texture.md#Texture)

**Returns**

- `texName` `string?`

### gl.CreateTexture (overload 1) {#gl.CreateTexture-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4240-L4247" target="_blank">source</a>]

```lua
gl.CreateTexture(integer, integer, integer, Texture) -> string?
```

**Parameters**

- `xsize` `integer`
- `ysize` `integer`
- `zsize` `integer`
- `texture` [`Texture`](Texture.md#Texture)

**Returns**

- `texName` `string?`

### gl.ChangeTextureParams {#gl.ChangeTextureParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4315-L4319" target="_blank">source</a>]

```lua
gl.ChangeTextureParams(string, Texture) -> nil
```

**Parameters**

- `texName` `string`
- `params` [`Texture`](Texture.md#Texture)

### gl.DeleteTexture {#gl.DeleteTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4346-L4350" target="_blank">source</a>]

```lua
gl.DeleteTexture(string) -> boolean
```

**Parameters**

- `texName` `string`

**Returns**

- `boolean`

### gl.DeleteTextureFBO {#gl.DeleteTextureFBO}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4367-L4371" target="_blank">source</a>]

```lua
gl.DeleteTextureFBO(string) -> boolean
```

**Parameters**

- `texName` `string`

**Returns**

- `boolean`

### gl.TextureInfo {#gl.TextureInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4393-L4397" target="_blank">source</a>]

```lua
gl.TextureInfo(string) -> TextureInfo
```

**Parameters**

- `texName` `string`

**Returns**

- `textureInfo` [`TextureInfo`](TextureInfo.md#TextureInfo)

### gl.CopyToTexture {#gl.CopyToTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4419-L4430" target="_blank">source</a>]

```lua
gl.CopyToTexture(string, integer, integer, integer, integer, integer, integer, GL?, GL?) -> nil
```

**Parameters**

- `texName` `string`
- `xoff` `integer`
- `yoff` `integer`
- `x` `integer`
- `y` `integer`
- `w` `integer`
- `h` `integer`
- `target` `GL?`
- `level` `GL?`

### gl.CopyImageSubData {#gl.CopyImageSubData}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4466-L4481" target="_blank">source</a>]

```lua
gl.CopyImageSubData(string, integer, integer, integer, integer, string, integer, integer, integer, integer, integer, integer, integer) -> nil
```

**Parameters**

- `srcName` `string`
- `srcLevel` `integer`
- `srcX` `integer`
- `srcY` `integer`
- `srcZ` `integer`
- `dstName` `string`
- `dstLevel` `integer`
- `dstX` `integer`
- `dstY` `integer`
- `dstZ` `integer`
- `width` `integer`
- `height` `integer`
- `depth` `integer`

### gl.RenderToTexture {#gl.RenderToTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4592-L4597" target="_blank">source</a>]

```lua
gl.RenderToTexture(string, unknown, [any, ]*) -> nil
```

**Parameters**

- `texName` `string`
- `fun` `unknown`
- `...` `any` — Arguments to the function.

### gl.GenerateMipmap {#gl.GenerateMipmap}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4646-L4649" target="_blank">source</a>]

```lua
gl.GenerateMipmap(string) -> nil
```

**Parameters**

- `texName` `string`

### gl.ActiveTexture {#gl.ActiveTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4671-L4676" target="_blank">source</a>]

```lua
gl.ActiveTexture(integer, function, [any, ]*) -> nil
```

**Parameters**

- `texNum` `integer`
- `func` `function`
- `...` `any` — Arguments to the function.

### gl.TexEnv {#gl.TexEnv}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4705-L4710" target="_blank">source</a>]

```lua
gl.TexEnv(GL, GL, number) -> nil
```

**Parameters**

- `target` [`GL`](GL-enum.md#GL)
- `pname` [`GL`](GL-enum.md#GL)
- `value` `number`

### gl.TexEnv (overload 1) {#gl.TexEnv-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4711-L4719" target="_blank">source</a>]

```lua
gl.TexEnv(GL, GL, number?, number?, number?, number?) -> nil
```

**Parameters**

- `target` [`GL`](GL-enum.md#GL)
- `pname` [`GL`](GL-enum.md#GL)
- `r` `number?` — (Default: `0.0`)
- `g` `number?` — (Default: `0.0`)
- `b` `number?` — (Default: `0.0`)
- `a` `number?` — (Default: `0.0`)

### gl.MultiTexEnv {#gl.MultiTexEnv}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4749-L4755" target="_blank">source</a>]

```lua
gl.MultiTexEnv(integer, GL, GL, number?) -> nil
```

**Parameters**

- `texNum` `integer`
- `target` [`GL`](GL-enum.md#GL)
- `pname` [`GL`](GL-enum.md#GL)
- `value` `number?`

### gl.MultiTexEnv (overload 1) {#gl.MultiTexEnv-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4756-L4765" target="_blank">source</a>]

```lua
gl.MultiTexEnv(integer, GL, GL, number?, number?, number?, number?) -> nil
```

**Parameters**

- `texNum` `integer`
- `target` [`GL`](GL-enum.md#GL)
- `pname` [`GL`](GL-enum.md#GL)
- `r` `number?` — (Default: `0.0`)
- `g` `number?` — (Default: `0.0`)
- `b` `number?` — (Default: `0.0`)
- `a` `number?` — (Default: `0.0`)

### gl.TexGen {#gl.TexGen}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4816-L4820" target="_blank">source</a>]

```lua
gl.TexGen(GL, boolean) -> nil
```

**Parameters**

- `target` [`GL`](GL-enum.md#GL)
- `state` `boolean`

### gl.TexGen (overload 1) {#gl.TexGen-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4821-L4826" target="_blank">source</a>]

```lua
gl.TexGen(GL, GL, number?) -> nil
```

**Parameters**

- `target` [`GL`](GL-enum.md#GL)
- `pname` [`GL`](GL-enum.md#GL)
- `value` `number?`

### gl.TexGen (overload 2) {#gl.TexGen-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4827-L4835" target="_blank">source</a>]

```lua
gl.TexGen(GL, GL, number?, number?, number?, number?) -> nil
```

**Parameters**

- `target` [`GL`](GL-enum.md#GL)
- `pname` [`GL`](GL-enum.md#GL)
- `r` `number?` — (Default: `0.0`)
- `g` `number?` — (Default: `0.0`)
- `b` `number?` — (Default: `0.0`)
- `a` `number?` — (Default: `0.0`)

### gl.MultiTexGen {#gl.MultiTexGen}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4874-L4879" target="_blank">source</a>]

```lua
gl.MultiTexGen(integer, GL, boolean) -> nil
```

**Parameters**

- `texNum` `integer`
- `target` [`GL`](GL-enum.md#GL)
- `state` `boolean`

### gl.MultiTexGen (overload 1) {#gl.MultiTexGen-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4880-L4886" target="_blank">source</a>]

```lua
gl.MultiTexGen(integer, GL, GL, number?) -> nil
```

**Parameters**

- `texNum` `integer`
- `target` [`GL`](GL-enum.md#GL)
- `pname` [`GL`](GL-enum.md#GL)
- `value` `number?`

### gl.MultiTexGen (overload 2) {#gl.MultiTexGen-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4887-L4896" target="_blank">source</a>]

```lua
gl.MultiTexGen(integer, GL, GL, number?, number?, number?, number?) -> nil
```

**Parameters**

- `texNum` `integer`
- `target` [`GL`](GL-enum.md#GL)
- `pname` [`GL`](GL-enum.md#GL)
- `r` `number?` — (Default: `0.0`)
- `g` `number?` — (Default: `0.0`)
- `b` `number?` — (Default: `0.0`)
- `a` `number?` — (Default: `0.0`)

### gl.BindImageTexture {#gl.BindImageTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L4945-L4971" target="_blank">source</a>]

For format parameters refer to
https://registry.khronos.org/OpenGL-Refpages/gl4/html/glBindImageTexture.xhtml
and
https://recoilengine.org/docs/lua-api/#GL.RGBA32F and further

Example uses
local my_texture_id = gl.CreateTexture(...)

-- bind layer 1 of my_texture_id if it supports layered bindings to image unit 0
gl.BindImageTexture(0, my_texture_id, 0, 1, GL.READ_WRITE, GL.RGBA16F)

-- bind all layers of my_texture_id if it supports layered bindings to image unit 0
gl.BindImageTexture(0, my_texture_id, 0, nil, GL.READ_WRITE, GL.RGBA16F)

-- unbind any texture attached to image unit 0
gl.BindImageTexture(0, nil, nil, nil, nil, GL.RGBA16F)

```lua
gl.BindImageTexture(integer, string?, integer?, integer?, GL?, integer) -> nil
```

**Parameters**

- `unit` `integer`
- `texID` `string?` — (nil breaks any existing binding to the image unit)
- `level` `integer?` — (Default: 0)
- `layer` `integer?` — (nil binds the entire texture(array/cube), an integer binds a specific layer, ignored by gl if the texture does not support layered bindings)
- `access` `GL?` — (Default: GL.READ_WRITE) Accepts [GL.READ_ONLY](GL-enum.md#GL.READ_ONLY), [GL.WRITE_ONLY](GL-enum.md#GL.WRITE_ONLY) or [GL.READ_WRITE](GL-enum.md#GL.READ_WRITE).
- `format` `integer` — (Example: GL.RGBA16F)

### gl.CreateTextureAtlas {#gl.CreateTextureAtlas}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5083-L5089" target="_blank">source</a>]

```lua
gl.CreateTextureAtlas(integer, integer, integer?) -> string
```

**Parameters**

- `xsize` `integer`
- `ysize` `integer`
- `allocType` `integer?`

**Returns**

- `texName` `string`

### gl.FinalizeTextureAtlas {#gl.FinalizeTextureAtlas}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5114-L5118" target="_blank">source</a>]

```lua
gl.FinalizeTextureAtlas(string) -> boolean
```

**Parameters**

- `texName` `string`

**Returns**

- `boolean`

### gl.DeleteTextureAtlas {#gl.DeleteTextureAtlas}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5134-L5138" target="_blank">source</a>]

```lua
gl.DeleteTextureAtlas(string) -> boolean
```

**Parameters**

- `texName` `string`

**Returns**

- `boolean`

### gl.AddAtlasTexture {#gl.AddAtlasTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5150-L5154" target="_blank">source</a>]

```lua
gl.AddAtlasTexture(string, string) -> nil
```

**Parameters**

- `texName` `string`
- `subAtlasTexName` `string`

### gl.GetAtlasTexture {#gl.GetAtlasTexture}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5201-L5209" target="_blank">source</a>]

```lua
gl.GetAtlasTexture(string, string) -> number, number, number, number
```

**Parameters**

- `texName` `string`
- `subAtlasTexName` `string`

**Returns**

- `x1` `number`
- `x2` `number`
- `y1` `number`
- `y2` `number`

### gl.GetEngineAtlasTextures {#gl.GetEngineAtlasTextures}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5235-L5239" target="_blank">source</a>]

```lua
gl.GetEngineAtlasTextures(("$explosions"|"$groundfx")) -> table<string,float4>
```

**Parameters**

- `atlasName` `("$explosions"|"$groundfx")`

**Returns**

- `atlasTextures` `table<string,float4>` — Table of x1,x2,y1,y2 coordinates by texture name.

### gl.Clear {#gl.Clear}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5289-L5292" target="_blank">source</a>]

```lua
gl.Clear(GL) -> nil
```

**Parameters**

- `bits` [`GL`](GL-enum.md#GL) — any buffer bit mask (e.g. [GL.STENCIL_BUFFER_BIT](GL-enum.md#GL.STENCIL_BUFFER_BIT)). Clears with current/default values.

### gl.Clear (overload 1) {#gl.Clear-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5293-L5297" target="_blank">source</a>]

```lua
gl.Clear(GL, number) -> nil
```

**Parameters**

- `bits` [`GL`](GL-enum.md#GL) — [GL.DEPTH_BUFFER_BIT](GL-enum.md#GL.DEPTH_BUFFER_BIT) or [GL.STENCIL_BUFFER_BIT](GL-enum.md#GL.STENCIL_BUFFER_BIT).
- `val` `number`

### gl.Clear (overload 2) {#gl.Clear-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5298-L5305" target="_blank">source</a>]

```lua
gl.Clear(GL, number, number, number, number) -> nil
```

**Parameters**

- `bits` [`GL`](GL-enum.md#GL) — [GL.COLOR_BUFFER_BIT](GL-enum.md#GL.COLOR_BUFFER_BIT) or [GL.ACCUM_BUFFER_BIT](GL-enum.md#GL.ACCUM_BUFFER_BIT).
- `r` `number`
- `g` `number`
- `b` `number`
- `a` `number`

### gl.SwapBuffers {#gl.SwapBuffers}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5344-L5346" target="_blank">source</a>]

```lua
gl.SwapBuffers() -> nil
```

### gl.Translate {#gl.Translate}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5361-L5366" target="_blank">source</a>]

```lua
gl.Translate(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`

### gl.Scale {#gl.Scale}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5379-L5384" target="_blank">source</a>]

```lua
gl.Scale(number, number, number) -> nil
```

**Parameters**

- `x` `number`
- `y` `number`
- `z` `number`

### gl.Rotate {#gl.Rotate}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5397-L5403" target="_blank">source</a>]

```lua
gl.Rotate(number, number, number, number) -> nil
```

**Parameters**

- `r` `number`
- `x` `number`
- `y` `number`
- `z` `number`

### gl.Ortho {#gl.Ortho}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5417-L5425" target="_blank">source</a>]

```lua
gl.Ortho(number, number, number, number, number, number) -> nil
```

**Parameters**

- `left` `number`
- `right` `number`
- `bottom` `number`
- `top` `number`
- `near` `number`
- `far` `number`

### gl.Frustum {#gl.Frustum}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5441-L5449" target="_blank">source</a>]

```lua
gl.Frustum(number, number, number, number, number, number) -> nil
```

**Parameters**

- `left` `number`
- `right` `number`
- `bottom` `number`
- `top` `number`
- `near` `number`
- `far` `number`

### gl.Billboard {#gl.Billboard}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5465-L5467" target="_blank">source</a>]

```lua
gl.Billboard() -> nil
```

### gl.Light {#gl.Light}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5479-L5483" target="_blank">source</a>]

```lua
gl.Light(integer, boolean) -> nil
```

**Parameters**

- `light` `integer`
- `enable` `boolean`

### gl.Light (overload 1) {#gl.Light-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5484-L5489" target="_blank">source</a>]

```lua
gl.Light(integer, GL, GL) -> nil
```

**Parameters**

- `light` `integer`
- `pname` [`GL`](GL-enum.md#GL)
- `param` [`GL`](GL-enum.md#GL)

### gl.Light (overload 2) {#gl.Light-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5490-L5498" target="_blank">source</a>]

```lua
gl.Light(integer, GL, number, number, number, number?) -> nil
```

**Parameters**

- `light` `integer`
- `pname` [`GL`](GL-enum.md#GL)
- `r` `number`
- `g` `number`
- `b` `number`
- `a` `number?`

### gl.ClipPlane {#gl.ClipPlane}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5549-L5553" target="_blank">source</a>]

```lua
gl.ClipPlane(integer, boolean) -> nil
```

**Parameters**

- `plane` `integer`
- `enable` `boolean`

### gl.ClipPlane (overload 1) {#gl.ClipPlane-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5554-L5561" target="_blank">source</a>]

```lua
gl.ClipPlane(integer, number, number, number, number) -> nil
```

**Parameters**

- `plane` `integer`
- `equation0` `number`
- `equation1` `number`
- `equation2` `number`
- `equation3` `number`

### gl.ClipDistance {#gl.ClipDistance}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5591-L5595" target="_blank">source</a>]

```lua
gl.ClipDistance(integer, boolean) -> nil
```

**Parameters**

- `clipId` `integer`
- `enable` `boolean`

### gl.MatrixMode {#gl.MatrixMode}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5624-L5627" target="_blank">source</a>]

```lua
gl.MatrixMode(GL) -> nil
```

**Parameters**

- `mode` [`GL`](GL-enum.md#GL)

### gl.LoadIdentity {#gl.LoadIdentity}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5640-L5642" target="_blank">source</a>]

```lua
gl.LoadIdentity() -> nil
```

### gl.LoadMatrix {#gl.LoadMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5678-L5681" target="_blank">source</a>]

```lua
gl.LoadMatrix(string) -> nil
```

**Parameters**

- `matrix` `string`

### gl.LoadMatrix (overload 1) {#gl.LoadMatrix-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5682-L5685" target="_blank">source</a>]

```lua
gl.LoadMatrix(Matrix4x4) -> nil
```

**Parameters**

- `matrix` [`Matrix4x4`](Matrix4x4.md#Matrix4x4)

### gl.LoadMatrix (overload 2) {#gl.LoadMatrix-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5686-L5704" target="_blank">source</a>]

```lua
gl.LoadMatrix() -> number, number, number, number, number, number, number, number, number, number, number, number, number, number, number, number
```

**Returns**

- `m11` `number`
- `m12` `number`
- `m13` `number`
- `m14` `number`
- `m21` `number`
- `m22` `number`
- `m23` `number`
- `m24` `number`
- `m31` `number`
- `m32` `number`
- `m33` `number`
- `m34` `number`
- `m41` `number`
- `m42` `number`
- `m43` `number`
- `m44` `number`

### gl.MultMatrix {#gl.MultMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5737-L5740" target="_blank">source</a>]

```lua
gl.MultMatrix(string) -> nil
```

**Parameters**

- `matrixName` `string`

### gl.MultMatrix (overload 1) {#gl.MultMatrix-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5741-L5744" target="_blank">source</a>]

```lua
gl.MultMatrix(Matrix4x4) -> nil
```

**Parameters**

- `matrix` [`Matrix4x4`](Matrix4x4.md#Matrix4x4)

### gl.MultMatrix (overload 2) {#gl.MultMatrix-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5745-L5763" target="_blank">source</a>]

```lua
gl.MultMatrix(number, number, number, number, number, number, number, number, number, number, number, number, number, number, number, number) -> nil
```

**Parameters**

- `m11` `number`
- `m12` `number`
- `m13` `number`
- `m14` `number`
- `m21` `number`
- `m22` `number`
- `m23` `number`
- `m24` `number`
- `m31` `number`
- `m32` `number`
- `m33` `number`
- `m34` `number`
- `m41` `number`
- `m42` `number`
- `m43` `number`
- `m44` `number`

### gl.PushMatrix {#gl.PushMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5796-L5798" target="_blank">source</a>]

```lua
gl.PushMatrix() -> nil
```

### gl.PopMatrix {#gl.PopMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5817-L5819" target="_blank">source</a>]

```lua
gl.PopMatrix() -> nil
```

### gl.PushPopMatrix {#gl.PushPopMatrix}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5837-L5842" target="_blank">source</a>]

```lua
gl.PushPopMatrix(GL, fun(), [any, ]*) -> nil
```

**Parameters**

- `matMode1` [`GL`](GL-enum.md#GL)
- `func` `fun()`
- `...` `any` — Arguments to the function.

### gl.PushPopMatrix (overload 1) {#gl.PushPopMatrix-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5843-L5847" target="_blank">source</a>]

```lua
gl.PushPopMatrix(fun(), [any, ]*) -> nil
```

**Parameters**

- `func` `fun()`
- `...` `any` — Arguments to the function.

### gl.GetMatrixData {#gl.GetMatrixData}
*function*

Get value at index of matrix.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5895-L5902" target="_blank">source</a>]

```lua
gl.GetMatrixData(GL, integer) -> number
```

**Parameters**

- `type` [`GL`](GL-enum.md#GL) — Matrix type ([GL.PROJECTION](GL-enum.md#GL.PROJECTION), [GL.MODELVIEW](GL-enum.md#GL.MODELVIEW), [GL.TEXTURE](GL-enum.md#GL.TEXTURE)).
- `index` `integer` — Matrix index in range `[1, 16]`.

**Returns**

- `value` `number` — The value at the given index.

### gl.GetMatrixData (overload 1) {#gl.GetMatrixData-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5903-L5907" target="_blank">source</a>]

```lua
gl.GetMatrixData(GL) -> Matrix4x4
```

**Parameters**

- `type` [`GL`](GL-enum.md#GL) — Matrix type ([GL.PROJECTION](GL-enum.md#GL.PROJECTION), [GL.MODELVIEW](GL-enum.md#GL.MODELVIEW), [GL.TEXTURE](GL-enum.md#GL.TEXTURE)).

**Returns**

- [`Matrix4x4`](Matrix4x4.md#Matrix4x4)

### gl.GetMatrixData (overload 2) {#gl.GetMatrixData-2}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5908-L5912" target="_blank">source</a>]

```lua
gl.GetMatrixData(integer) -> number
```

**Parameters**

- `index` `integer` — Matrix index in range `[1, 16]`.

**Returns**

- `value` `number` — The value at the given index.

### gl.GetMatrixData (overload 3) {#gl.GetMatrixData-3}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5913-L5917" target="_blank">source</a>]

```lua
gl.GetMatrixData(MatrixName) -> Matrix4x4
```

**Parameters**

- `name` [`MatrixName`](Aliases.md#MatrixName)

**Returns**

- [`Matrix4x4`](Matrix4x4.md#Matrix4x4)

### gl.PushAttrib {#gl.PushAttrib}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5980-L5983" target="_blank">source</a>]

```lua
gl.PushAttrib(GL?) -> nil
```

**Parameters**

- `mask` `GL?` — (Default: [GL.ALL_ATTRIB_BITS](GL-enum.md#GL.ALL_ATTRIB_BITS))

### gl.PopAttrib {#gl.PopAttrib}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L5997-L5999" target="_blank">source</a>]

```lua
gl.PopAttrib() -> nil
```

### gl.UnsafeState {#gl.UnsafeState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6008-L6013" target="_blank">source</a>]

```lua
gl.UnsafeState(GL, fun(), [any, ]*) -> nil
```

**Parameters**

- `state` [`GL`](GL-enum.md#GL)
- `func` `fun()`
- `...` `any` — Arguments to the function.

### gl.UnsafeState (overload 1) {#gl.UnsafeState-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6014-L6020" target="_blank">source</a>]

```lua
gl.UnsafeState(GL, boolean, fun(), [any, ]*) -> nil
```

**Parameters**

- `state` [`GL`](GL-enum.md#GL)
- `reverse` `boolean`
- `func` `fun()`
- `...` `any` — Arguments to the function.

### gl.GetFixedState {#gl.GetFixedState}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6047-L6053" target="_blank">source</a>]

```lua
gl.GetFixedState(string, boolean?) -> boolean, any ...
```

**Parameters**

- `param` `string`
- `toStr` `boolean?` — (Default: `false`)

**Returns**

- `enabled` `boolean`
- `values` `any ...`

### gl.CreateList {#gl.CreateList}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6335-L6340" target="_blank">source</a>]

```lua
gl.CreateList(fun(), [any, ]*) -> integer
```

**Parameters**

- `func` `fun()`
- `...` `any` — Arguments to the function.

**Returns**

- `listID` `integer` — `0` if the list could not be generated or `func` errored.

### gl.CallList {#gl.CallList}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6388-L6391" target="_blank">source</a>]

```lua
gl.CallList(integer) -> nil
```

**Parameters**

- `listIndex` `integer`

### gl.DeleteList {#gl.DeleteList}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6412-L6415" target="_blank">source</a>]

```lua
gl.DeleteList(integer) -> nil
```

**Parameters**

- `listIndex` `integer`

### gl.Flush {#gl.Flush}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6435-L6437" target="_blank">source</a>]

```lua
gl.Flush() -> nil
```

### gl.Finish {#gl.Finish}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6446-L6448" target="_blank">source</a>]

```lua
gl.Finish() -> nil
```

### gl.ReadPixels {#gl.ReadPixels}
*function*

Get single pixel.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6504-L6513" target="_blank">source</a>]

```lua
gl.ReadPixels(integer, integer, 1, 1, GL?) -> number ...
```

**Parameters**

- `x` `integer`
- `y` `integer`
- `w` `1`
- `h` `1`
- `format` `GL?` — (Default: `GL.RGBA`)

**Returns**

- `Color` `number ...` — value (color size based on format).

### gl.ReadPixels (overload 1) {#gl.ReadPixels-1}
*function*

Get column of pixels.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6514-L6523" target="_blank">source</a>]

```lua
gl.ReadPixels(integer, integer, 1, integer, GL?) -> number[][]
```

**Parameters**

- `x` `integer`
- `y` `integer`
- `w` `1`
- `h` `integer`
- `format` `GL?` — (Default: `GL.RGBA`)

**Returns**

- `colors` `number[][]` — Column of color values (color size based on format).

### gl.ReadPixels (overload 2) {#gl.ReadPixels-2}
*function*

Get row of pixels.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6524-L6533" target="_blank">source</a>]

```lua
gl.ReadPixels(integer, integer, integer, 1, GL?) -> number[][]
```

**Parameters**

- `x` `integer`
- `y` `integer`
- `w` `integer`
- `h` `1`
- `format` `GL?` — (Default: `GL.RGBA`)

**Returns**

- `colors` `number[][]` — Row of color values (color size based on format).

### gl.ReadPixels (overload 3) {#gl.ReadPixels-3}
*function*

Get columns of pixels.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6534-L6543" target="_blank">source</a>]

```lua
gl.ReadPixels(integer, integer, integer, integer, GL?) -> number[][][]
```

**Parameters**

- `x` `integer`
- `y` `integer`
- `w` `integer`
- `h` `integer`
- `format` `GL?` — (Default: `GL.RGBA`)

**Returns**

- `colors` `number[][][]` — Array of columns of color values (color size based on format).

### gl.SaveImage {#gl.SaveImage}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6624-L6633" target="_blank">source</a>]

```lua
gl.SaveImage(integer, integer, integer, integer, string, SaveImageOptions?) -> boolean?
```

**Parameters**

- `x` `integer`
- `y` `integer`
- `width` `integer`
- `height` `integer`
- `filename` `string`
- `options` `SaveImageOptions?`

**Returns**

- `success` `boolean?`

### gl.CreateQuery {#gl.CreateQuery}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6707-L6710" target="_blank">source</a>]

```lua
gl.CreateQuery() -> any
```

**Returns**

- `query` `any`

### gl.DeleteQuery {#gl.DeleteQuery}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6731-L6734" target="_blank">source</a>]

```lua
gl.DeleteQuery(any) -> nil
```

**Parameters**

- `query` `any`

### gl.RunQuery {#gl.RunQuery}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6758-L6761" target="_blank">source</a>]

```lua
gl.RunQuery(any) -> nil
```

**Parameters**

- `query` `any`

### gl.GetQuery {#gl.GetQuery}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6798-L6802" target="_blank">source</a>]

```lua
gl.GetQuery(any) -> integer
```

**Parameters**

- `query` `any`

**Returns**

- `count` `integer`

### gl.GetGlobalTexNames {#gl.GetGlobalTexNames}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6825-L6828" target="_blank">source</a>]

```lua
gl.GetGlobalTexNames() -> string[]
```

**Returns**

- `texNames` `string[]` — List of texture names.

### gl.GetGlobalTexCoords {#gl.GetGlobalTexCoords}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6844-L6850" target="_blank">source</a>]

```lua
gl.GetGlobalTexCoords() -> number, number, number, number
```

**Returns**

- `xstart` `number`
- `ystart` `number`
- `xend` `number`
- `yend` `number`

### gl.GetShadowMapParams {#gl.GetShadowMapParams}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6867-L6873" target="_blank">source</a>]

```lua
gl.GetShadowMapParams() -> number, number, number, number
```

**Returns**

- `x` `number`
- `y` `number`
- `z` `number`
- `w` `number`

### gl.GetAtmosphere {#gl.GetAtmosphere}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6883-L6888" target="_blank">source</a>]

```lua
gl.GetAtmosphere() -> number, number, number
```

**Returns**

- `lightDirX` `number`
- `lightDirY` `number`
- `lightDirZ` `number`

### gl.GetAtmosphere (overload 1) {#gl.GetAtmosphere-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6889-L6893" target="_blank">source</a>]

```lua
gl.GetAtmosphere(("fogStart"|"fogEnd"|"pos"|"fogColor"|"skyColor"|"sunColor"...)) -> any ...
```

**Parameters**

- `param` `("fogStart"|"fogEnd"|"pos"|"fogColor"|"skyColor"|"sunColor"...)`

**Returns**

- `any ...`

### gl.GetSun {#gl.GetSun}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6946-L6951" target="_blank">source</a>]

```lua
gl.GetSun() -> number, number, number
```

**Returns**

- `lightDirX` `number`
- `lightDirY` `number`
- `lightDirZ` `number`

### gl.GetSun (overload 1) {#gl.GetSun-1}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L6952-L6959" target="_blank">source</a>]

```lua
gl.GetSun(("pos"|"dir"|"specularExponent"|"shadowDensity"|"diffuse"|"ambient"...), ("ground"|"unit")) -> number?, number?, number?
```

**Parameters**

- `param` `("pos"|"dir"|"specularExponent"|"shadowDensity"|"diffuse"|"ambient"...)`
- `mode` `("ground"|"unit")` — (Default: `"ground"`)

**Returns**

- `data1` `number?`
- `data2` `number?`
- `data3` `number?`

### gl.GetWaterRendering {#gl.GetWaterRendering}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L7025-L7029" target="_blank">source</a>]

```lua
gl.GetWaterRendering(string) -> any ...
```

**Parameters**

- `key` `string`

**Returns**

- `value` `any ...`

### gl.GetMapRendering {#gl.GetMapRendering}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L7207-L7211" target="_blank">source</a>]

```lua
gl.GetMapRendering(string) -> any ...
```

**Parameters**

- `key` `string`

**Returns**

- `value` `any ...`

### gl.ObjectLabel {#gl.ObjectLabel}
*function*

Labels an object for use with debugging tools.
May be unavailable and `nil` if the platform doesn't support the feature.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L7251-L7259" target="_blank">source</a>]

```lua
gl.ObjectLabel(GL, integer, string) -> nil
```

**Parameters**

- `objectTypeIdentifier` [`GL`](GL-enum.md#GL) — Specifies the type of object being labeled.
- `objectID` `integer` — Specifies the name or ID of the object to label.
- `label` `string` — A string containing the label to be assigned to the object.

### gl.PushDebugGroup {#gl.PushDebugGroup}
*function*

Pushes a debug marker for debugging tools such as `nVidia nSight 2024.04`,
see https://registry.khronos.org/OpenGL-Refpages/gl4/html/glPushDebugGroup.xhtml .

May be unavailable and `nil` if the platform doesn't support the feature.

Groups are basically named scopes similar to tracy's, and are pushed/popped independently
from GL attribute/matrix push/pop (though of course makes sense to put them together).

Tools are known to struggle to see the annotation for FBOs if they are raw bound.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L7288-L7304" target="_blank">source</a>]

```lua
gl.PushDebugGroup(integer, string, boolean?) -> nil
```

**Parameters**

- `id` `integer` — A numeric identifier for the group, can be any unique number.
- `message` `string` — A human-readable string describing the debug group. Will be truncated if longer than driver-specific limit
- `sourceIsThirdParty` `boolean?` — Set the source tag, true for GL_DEBUG_SOURCE_THIRD_PARTY, false for GL_DEBUG_SOURCE_APPLICATION. default false

**Returns**

- `nil`

### gl.PopDebugGroup {#gl.PopDebugGroup}
*function*

Pops the most recent GL debug group from the stack (does NOT take the numerical ID from push).
May be unavailable and `nil` if the platform doesn't support the feature.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaOpenGL.cpp#L7326-L7333" target="_blank">source</a>]

```lua
gl.PopDebugGroup() -> nil
```

**Returns**

- `nil`

### gl.CreateRBO {#gl.CreateRBO}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaRBOs.cpp#L158-L164" target="_blank">source</a>]

```lua
gl.CreateRBO(integer, integer, CreateRBOData) -> RBO
```

**Parameters**

- `xsize` `integer`
- `ysize` `integer`
- `data` [`CreateRBOData`](CreateRBOData.md#CreateRBOData)

**Returns**

- [`RBO`](RBO.md#RBO)

### gl.DeleteRBO {#gl.DeleteRBO}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaRBOs.cpp#L234-L237" target="_blank">source</a>]

```lua
gl.DeleteRBO(RBO) -> nil
```

**Parameters**

- `rbo` [`RBO`](RBO.md#RBO)

### gl.GetShaderLog {#gl.GetShaderLog}
*function*

Returns the shader compilation error log. This is empty if the shader linking failed, in that case, check your in/out blocks and ensure they match.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L199-L203" target="_blank">source</a>]

```lua
gl.GetShaderLog() -> string
```

**Returns**

- `infoLog` `string`

### gl.CreateShader {#gl.CreateShader}
*function*

Create a shader.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L624-L630" target="_blank">source</a>]

```lua
gl.CreateShader(ShaderParams) -> integer
```

**Parameters**

- `shaderParams` [`ShaderParams`](ShaderParams.md#ShaderParams)

**Returns**

- `shaderID` `integer`

### gl.DeleteShader {#gl.DeleteShader}
*function*

Deletes a shader identified by shaderID

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L794-L799" target="_blank">source</a>]

```lua
gl.DeleteShader(integer) -> boolean?
```

**Parameters**

- `shaderID` `integer`

**Returns**

- `deleted` `boolean?` — `nil` if `shaderID` is `nil`.

### gl.UseShader {#gl.UseShader}
*function*

Binds a shader program identified by shaderID. Pass 0 to disable the shader. Returns whether the shader was successfully bound.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L812-L817" target="_blank">source</a>]

```lua
gl.UseShader(integer) -> boolean
```

**Parameters**

- `shaderID` `integer`

**Returns**

- `linked` `boolean`

### gl.ActiveShader {#gl.ActiveShader}
*function*

Binds a shader program identified by shaderID, and calls the Lua func with
the specified arguments.

Can be used in NON-drawing events (to update uniforms etc.)!

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L845-L855" target="_blank">source</a>]

```lua
gl.ActiveShader(integer, function, [any, ]*) -> nil
```

**Parameters**

- `shaderID` `integer`
- `func` `function`
- `...` `any` — Arguments

### gl.GetActiveUniforms {#gl.GetActiveUniforms}
*function*

Query the active (actually used) uniforms of a shader and identify their
names, types (float, int, uint) and sizes (float, vec4, ...).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L938-L945" target="_blank">source</a>]

```lua
gl.GetActiveUniforms(integer) -> ActiveUniform[]
```

**Parameters**

- `shaderID` `integer`

**Returns**

- `activeUniforms` `ActiveUniform[]`

### gl.GetUniformLocation {#gl.GetUniformLocation}
*function*

Returns the locationID of a shaders uniform. Needed for changing uniform
values with function [gl.Uniform](gl.md#gl.Uniform).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L973-L981" target="_blank">source</a>]

```lua
gl.GetUniformLocation(integer, string) -> GL
```

**Parameters**

- `shaderID` `integer`
- `name` `string`

**Returns**

- `locationID` [`GL`](GL-enum.md#GL)

### gl.GetSubroutineIndex {#gl.GetSubroutineIndex}
*function*

Returns the subroutine index for a shader program.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L996-L1006" target="_blank">source</a>]

```lua
gl.GetSubroutineIndex(integer, integer, string) -> integer?
```

**Parameters**

- `shaderID` `integer`
- `shaderType` `integer`
- `name` `string`

**Returns**

- `index` `integer?`

### gl.SetUnitBufferUniforms {#gl.SetUnitBufferUniforms}
*function*

Writes user-defined model uniforms for a unit.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1055-L1063" target="_blank">source</a>]

```lua
gl.SetUnitBufferUniforms(UnitID, number[], integer?) -> integer
```

**Parameters**

- `unitID` [`UnitID`](Aliases.md#UnitID)
- `values` `number[]`
- `offset` `integer?`

**Returns**

- `count` `integer`

### gl.SetFeatureBufferUniforms {#gl.SetFeatureBufferUniforms}
*function*

Writes user-defined model uniforms for a feature.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1065-L1073" target="_blank">source</a>]

```lua
gl.SetFeatureBufferUniforms(FeatureID, number[], integer?) -> integer
```

**Parameters**

- `featureID` [`FeatureID`](Aliases.md#FeatureID)
- `values` `number[]`
- `offset` `integer?`

**Returns**

- `count` `integer`

### gl.Uniform {#gl.Uniform}
*function*

Sets the uniform float value at the locationID for the currently active
shader. Shader must be activated before setting uniforms.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1081-L1092" target="_blank">source</a>]

```lua
gl.Uniform((GL|string), number, number?, number?, number?) -> nil
```

**Parameters**

- `locationID` `(GL|string)` — uniformName
- `f1` `number`
- `f2` `number?`
- `f3` `number?`
- `f4` `number?`

### gl.UniformFloat {#gl.UniformFloat}
*function*

Sets the uniform float value at the locationID for the currently active
shader. Shader must be activated before setting uniforms.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1081-L1092" target="_blank">source</a>]

Alias of Uniform

```lua
gl.UniformFloat((GL|string), number, number?, number?, number?) -> nil
```

**Parameters**

- `locationID` `(GL|string)` — uniformName
- `f1` `number`
- `f2` `number?`
- `f3` `number?`
- `f4` `number?`

### gl.UniformInt {#gl.UniformInt}
*function*

Sets the uniform int value at the locationID for the currently active shader.
Shader must be activated before setting uniforms.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1123-L1133" target="_blank">source</a>]

```lua
gl.UniformInt((integer|string), integer, integer?, integer?, integer?) -> nil
```

**Parameters**

- `locationID` `(integer|string)` — uniformName
- `int1` `integer`
- `int2` `integer?`
- `int3` `integer?`
- `int4` `integer?`

### gl.UniformArray {#gl.UniformArray}
*function*

Sets the an array of uniform values at the locationID for the currently
active shader.

Shader must be activated before setting uniforms.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1193-L1203" target="_blank">source</a>]

```lua
gl.UniformArray((integer|string), UniformArrayType, number[]) -> nil
```

**Parameters**

- `locationID` `(integer|string)` — uniformName
- `type` [`UniformArrayType`](Aliases.md#UniformArrayType)
- `uniforms` `number[]` — Array up to 1024 elements

### gl.UniformMatrix {#gl.UniformMatrix}
*function*

Sets the a uniform mat4 locationID for the currently active shader.

Shader must be activated before setting uniforms.

Can set one one common matrix like shadow, or by passing 16 additional
numbers for the matrix.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1242-L1253" target="_blank">source</a>]

```lua
gl.UniformMatrix((integer|string), MatrixName) -> nil
```

**Parameters**

- `locationID` `(integer|string)` — uniformName
- `matrix` [`MatrixName`](Aliases.md#MatrixName) — Name of common matrix.

### gl.UniformMatrix (overload 1) {#gl.UniformMatrix-1}
*function*

Sets the a uniform mat4 locationID for the currently active shader.

Shader must be activated before setting uniforms.

Can set one one common matrix like shadow, or by passing 16 additional
numbers for the matrix.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1255-L1266" target="_blank">source</a>]

```lua
gl.UniformMatrix((integer|string), number[]) -> nil
```

**Parameters**

- `locationID` `(integer|string)` — uniformName
- `matrix` `number[]` — A 2x2, 3x3 or 4x4 matrix.

### gl.UniformSubroutine {#gl.UniformSubroutine}
*function*

Selects a subroutine for the active shader program.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1328-L1334" target="_blank">source</a>]

```lua
gl.UniformSubroutine(integer, integer) -> nil
```

**Parameters**

- `shaderType` `integer`
- `index` `integer`

### gl.GetEngineUniformBufferDef {#gl.GetEngineUniformBufferDef}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1350-L1358" target="_blank">source</a>]

Return the GLSL compliant definition of UniformMatricesBuffer(idx=0) or UniformParamsBuffer(idx=1) structure.

```lua
gl.GetEngineUniformBufferDef(integer) -> string
```

**Parameters**

- `index` `integer`

**Returns**

- `glslDefinition` `string`

### gl.GetEngineModelUniformDataDef {#gl.GetEngineModelUniformDataDef}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1372-L1380" target="_blank">source</a>]

Return the GLSL compliant definition of ModelUniformData structure (per Unit/Feature buffer available on GPU)

```lua
gl.GetEngineModelUniformDataDef(integer) -> string
```

**Parameters**

- `index` `integer`

**Returns**

- `glslDefinition` `string`

### gl.GetEngineModelUniformDataSize {#gl.GetEngineModelUniformDataSize}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1390-L1400" target="_blank">source</a>]

Return the current size values of ModelUniformData structure (per Unit/Feature buffer available on GPU)

```lua
gl.GetEngineModelUniformDataSize(integer) -> integer, integer
```

**Parameters**

- `index` `integer`

**Returns**

- `sizeInElements` `integer`
- `sizeInBytesOnCPU` `integer`

### gl.SetGeometryShaderParameter {#gl.SetGeometryShaderParameter}
*function*

Sets the Geometry shader parameters for shaderID. Needed by geometry shader programs (check the opengl GL_ARB_geometry_shader4 extension for glProgramParameteri)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1413-L1420" target="_blank">source</a>]

```lua
gl.SetGeometryShaderParameter(integer, GL, integer) -> nil
```

**Parameters**

- `shaderID` `integer`
- `key` [`GL`](GL-enum.md#GL)
- `value` `integer`

**Returns**

- `nil`

### gl.SetTesselationShaderParameter {#gl.SetTesselationShaderParameter}
*function*

Sets the tesselation shader parameters for `shaderID`.

Needed by tesselation shader programs. (Check the opengl
`GL_ARB_tessellation_shader` extension for `glProgramParameteri`).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaShaders.cpp#L1441-L1451" target="_blank">source</a>]

```lua
gl.SetTesselationShaderParameter(integer, integer) -> nil
```

**Parameters**

- `param` `integer`
- `value` `integer`

**Returns**

- `nil`

### gl.GetVAO {#gl.GetVAO}
*function*

Example:
```
local myVAO = gl.GetVAO()
if myVAO == nil then Spring.Echo("Failed to get VAO") end
```

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVAO.cpp#L75-L84" target="_blank">source</a>]

```lua
gl.GetVAO() -> VAO?
```

**Returns**

- `vao` `VAO?` — The VAO ref on success, else `nil`

### gl.GetVBO {#gl.GetVBO}
*function*

Example:

```lua
local myVBO = gl.GetVBO()
if myVBO == nil then Spring.Echo("Failed to get VBO") end
```

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVBO.cpp#L125-L152" target="_blank">source</a>]

**See:** GL.OpenGL_Buffer_Types

```lua
gl.GetVBO(GL?, boolean?) -> VBO?
```

**Parameters**

- `bufferType` `GL?` — (Default: [GL.ARRAY_BUFFER](GL-enum.md#GL.ARRAY_BUFFER)) The buffer type to use.

Accepts the following:
- [GL.ARRAY_BUFFER](GL-enum.md#GL.ARRAY_BUFFER) for vertex data.
- [GL.ELEMENT_ARRAY_BUFFER](GL-enum.md#GL.ELEMENT_ARRAY_BUFFER) for vertex indices.
- [GL.UNIFORM_BUFFER](GL-enum.md#GL.UNIFORM_BUFFER)
- [GL.SHADER_STORAGE_BUFFER](GL-enum.md#GL.SHADER_STORAGE_BUFFER)
- `freqUpdated` `boolean?` — (Default: `true`)

`true` to updated frequently, `false` to update only once.

**Returns**

- `VBO` `VBO?`
