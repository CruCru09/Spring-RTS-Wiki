---
title: "RmlUi.ElementTabSet"
tags:
  - Lua-API
---

## RmlUi.ElementTabSet {#RmlUi.ElementTabSet}
*class*

Inherits [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementDerived.cpp#L57-L59" target="_blank">source</a>]

**Members**

### RmlUi.ElementTabSet:SetPanel {#RmlUi.ElementTabSet:SetPanel}
*function*

Sets the contents of a panel to the RML content rml. If index is out-of-bounds, a new panel will be added at the end.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementDerived.cpp#L63-L68" target="_blank">source</a>]

```lua
RmlUi.ElementTabSet:SetPanel(integer, string) -> nil
```

**Parameters**

- `index` `integer`
- `rml` `string`

### RmlUi.ElementTabSet:SetTab {#RmlUi.ElementTabSet:SetTab}
*function*

Sets the contents of a tab to the RML content rml. If index is out-of-bounds, a new tab will be added at the end.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementDerived.cpp#L70-L75" target="_blank">source</a>]

```lua
RmlUi.ElementTabSet:SetTab(integer, string) -> nil
```

**Parameters**

- `index` `integer`
- `rml` `string`

### RmlUi.ElementTabSet:RemoveTab {#RmlUi.ElementTabSet:RemoveTab}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementDerived.cpp#L78-L81" target="_blank">source</a>]

```lua
RmlUi.ElementTabSet:RemoveTab(integer) -> nil
```

**Parameters**

- `index` `integer`

**Fields**

- <span id="RmlUi.ElementTabSet.active_tab"></span> `RmlUi.ElementTabSet.active_tab` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementDerived.cpp#L85-L85" target="_blank">source</a>]
- <span id="RmlUi.ElementTabSet.num_tabs"></span> `RmlUi.ElementTabSet.num_tabs` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementDerived.cpp#L89-L89" target="_blank">source</a>]
