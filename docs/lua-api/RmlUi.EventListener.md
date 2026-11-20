---
title: "RmlUi.EventListener"
tags:
  - Lua-API
---

## RmlUi.EventListener {#RmlUi.EventListener}
*class*

Event listener interface

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L223-L226" target="_blank">source</a>]

**Members**

### RmlUi.EventListener.OnAttach {#RmlUi.EventListener.OnAttach}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L229-L232" target="_blank">source</a>]

```lua
RmlUi.EventListener.OnAttach(RmlUi.Element) -> nil
```

**Parameters**

- `element` [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element)

### RmlUi.EventListener.OnDetach {#RmlUi.EventListener.OnDetach}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L234-L237" target="_blank">source</a>]

```lua
RmlUi.EventListener.OnDetach(RmlUi.Element) -> nil
```

**Parameters**

- `element` [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element)

### RmlUi.EventListener.ProcessEvent {#RmlUi.EventListener.ProcessEvent}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L239-L242" target="_blank">source</a>]

```lua
RmlUi.EventListener.ProcessEvent(RmlUi.Event) -> nil
```

**Parameters**

- `event` [`RmlUi.Event`](RmlUi.Event.md#RmlUi.Event)
