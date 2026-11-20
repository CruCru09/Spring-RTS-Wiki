---
title: "tracy"
tags:
  - Lua-API
---

## tracy {#tracy}
*table*

**Members**

### tracy.LuaTracyPlotConfig {#tracy.LuaTracyPlotConfig}
*function*

Configure custom appearance for a Tracy plot for use in debugging or profiling

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaTracyExtra.cpp#L32-L40" target="_blank">source</a>]

```lua
tracy.LuaTracyPlotConfig(string, ("Number"|"Percentage"|"Memory")?, boolean?, boolean?, integer?) -> nil
```

**Parameters**

- `plotName` `string` — name of the plot to customize
- `plotFormatType` `("Number"|"Percentage"|"Memory")?` — (Default: `"Number"`)
- `stepwise` `boolean?` — (Default: `true`) stepwise chart
- `fill` `boolean?` — (Default: `false`) whether to fill color
- `color` `integer?` — (Default: `0xFFFFFF`) uint32 number as BGR color

### tracy.LuaTracyPlot {#tracy.LuaTracyPlot}
*function*

Update a Tracy plot with a value

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaTracyExtra.cpp#L62-L67" target="_blank">source</a>]

```lua
tracy.LuaTracyPlot(string, number) -> nil
```

**Parameters**

- `plotName` `string` — Which LuaPlot should be updated
- `plotValue` `number` — the number to show on the Tracy plot

### tracy.ZoneBegin {#tracy.ZoneBegin}
*function*

```lua
tracy.ZoneBegin(string) -> nil
```

**Parameters**

- `name` `string`

### tracy.ZoneBeginN {#tracy.ZoneBeginN}
*function*

```lua
tracy.ZoneBeginN(string) -> nil
```

**Parameters**

- `name` `string`

### tracy.ZoneBeginS {#tracy.ZoneBeginS}
*function*

```lua
tracy.ZoneBeginS(string) -> nil
```

**Parameters**

- `name` `string`

### tracy.ZoneBeginNS {#tracy.ZoneBeginNS}
*function*

```lua
tracy.ZoneBeginNS(string) -> nil
```

**Parameters**

- `name` `string`

### tracy.ZoneEnd {#tracy.ZoneEnd}
*function*

```lua
tracy.ZoneEnd() -> nil
```

### tracy.ZoneText {#tracy.ZoneText}
*function*

```lua
tracy.ZoneText(string) -> nil
```

**Parameters**

- `text` `string`

### tracy.ZoneName {#tracy.ZoneName}
*function*

```lua
tracy.ZoneName(string) -> nil
```

**Parameters**

- `name` `string`

### tracy.Message {#tracy.Message}
*function*

```lua
tracy.Message(string) -> nil
```

**Parameters**

- `text` `string`
