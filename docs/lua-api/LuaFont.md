---
title: "LuaFont"
tags:
  - Lua-API
---

## LuaFont {#LuaFont}
*class*

Lua opengl font object.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L21-L27" target="_blank">source</a>]

**See:** [gl.LoadFont](gl.md#gl.LoadFont)

**Members**

### LuaFont:Print {#LuaFont:Print}
*function*

Draws text in screen space at the given position.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L278-L286" target="_blank">source</a>]

```lua
LuaFont:Print(string, number, number, number?, string?) -> nil
```

**Parameters**

- `text` `string`
- `x` `number`
- `y` `number`
- `size` `number?` — Defaults to the font's point size.
- `options` `string?` — Flag characters for alignment, outline, shadow, scaling, etc. (e.g. `"co"` for center and outline).

### LuaFont:PrintWorld {#LuaFont:PrintWorld}
*function*

Draws text in world space at the given position.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L335-L344" target="_blank">source</a>]

```lua
LuaFont:PrintWorld(string, number, number, number, number?, string?) -> nil
```

**Parameters**

- `text` `string`
- `x` `number`
- `y` `number`
- `z` `number`
- `size` `number?` — Defaults to the font's point size.
- `options` `string?` — Flag characters for alignment, outline, shadow, scaling, etc. (e.g. `"co"` for center and outline).

### LuaFont:Begin {#LuaFont:Begin}
*function*

Begin a block of font commands.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L399-L413" target="_blank">source</a>]

Fonts can be printed without using Start/End, but when doing several operations it's more optimal
if done inside a block.

Also allows disabling automatic setting of the blend mode. Otherwise the font will always print
with `BlendFunc(GL.SRC_ALPHA, GL.ONE_MINUS_SRC_ALPHA)`.

**See:** [gl.BlendFuncSeparate](gl.md#gl.BlendFuncSeparate)

```lua
LuaFont:Begin(boolean?) -> nil
```

**Parameters**

- `userDefinedBlending` `boolean?` — When `true` doesn't set the gl.BlendFunc automatically. Defaults to `false`.

### LuaFont:End {#LuaFont:End}
*function*

Ends a font command block started with [LuaFont:Begin](LuaFont.md#LuaFont:Begin).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L424-L427" target="_blank">source</a>]

```lua
LuaFont:End() -> nil
```

### LuaFont:SubmitBuffered {#LuaFont:SubmitBuffered}
*function*

Draws text printed with the `buffered` option.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L437-L446" target="_blank">source</a>]

**See:** [gl.BlendFuncSeparate](gl.md#gl.BlendFuncSeparate)

```lua
LuaFont:SubmitBuffered(boolean?, boolean?) -> nil
```

**Parameters**

- `noBillboarding` `boolean?` — When `false` sets 3d billboard mode. Defaults to `true`.
- `userDefinedBlending` `boolean?` — When `true` doesn't set the gl.BlendFunc automatically. Defaults to `false`.

### LuaFont:WrapText {#LuaFont:WrapText}
*function*

Wraps text to fit within a maximum width (and optional max height), in-place.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L466-L475" target="_blank">source</a>]

```lua
LuaFont:WrapText(string, number, number?, number?) -> string, integer
```

**Parameters**

- `text` `string`
- `maxWidth` `number`
- `maxHeight` `number?` — Defaults to an engine-defined maximum height.
- `size` `number?` — Defaults to the font's point size.

**Returns**

- `wrappedText` `string`
- `lineCount` `integer`

### LuaFont:GetTextWidth {#LuaFont:GetTextWidth}
*function*

Returns the horizontal extent of a string for this font at its current size.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L497-L502" target="_blank">source</a>]

```lua
LuaFont:GetTextWidth(string) -> number
```

**Parameters**

- `text` `string`

**Returns**

- `width` `number`

### LuaFont:GetTextHeight {#LuaFont:GetTextHeight}
*function*

Returns layout metrics for a string: total height, descender depth, and line count.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L513-L520" target="_blank">source</a>]

```lua
LuaFont:GetTextHeight(string) -> number, number, integer
```

**Parameters**

- `text` `string`

**Returns**

- `height` `number`
- `descender` `number`
- `lines` `integer`

### LuaFont:SetTextColor {#LuaFont:SetTextColor}
*function*

Sets the RGBA color used when drawing text (fill).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L572-L576" target="_blank">source</a>]

```lua
LuaFont:SetTextColor(table) -> nil
```

**Parameters**

- `color` `table` — Four-component RGBA array (`{r, g, b, a}`), or pass `r`, `g`, `b`, and optional `a` as separate numbers (requires at least three numeric components after the font).

### LuaFont:SetOutlineColor {#LuaFont:SetOutlineColor}
*function*

Sets the RGBA color used for text outline when outline rendering is enabled.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L579-L583" target="_blank">source</a>]

```lua
LuaFont:SetOutlineColor(table) -> nil
```

**Parameters**

- `color` `table` — Four-component RGBA array (`{r, g, b, a}`), or pass `r`, `g`, `b`, and optional `a` as separate numbers (requires at least three numeric components after the font).

### LuaFont:SetAutoOutlineColor {#LuaFont:SetAutoOutlineColor}
*function*

When enabled, outline color is derived automatically instead of using `SetOutlineColor`.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaFonts.cpp#L587-L591" target="_blank">source</a>]

```lua
LuaFont:SetAutoOutlineColor(boolean) -> nil
```

**Parameters**

- `enabled` `boolean`
