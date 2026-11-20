---
title: "RmlUi.ElementPtr"
tags:
  - Lua-API
---

## RmlUi.ElementPtr {#RmlUi.ElementPtr}
*class*

Represents an owned element.

This type is mainly used to modify the DOM tree by passing the object into other elements. For example `RmlUi.Element:AppendChild()`.
A current limitation in the Lua plugin is that Element member properties and functions cannot be used directly on this type.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L110-L116" target="_blank">source</a>]
