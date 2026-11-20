---
title: "RmlUi.SolLuaDataModel"
tags:
  - Lua-API
---

## RmlUi.SolLuaDataModel {#RmlUi.SolLuaDataModel}
*class*

Handle for a data model.

It is a wrapper around the model table, marked as type T.
You can access fields by using normal indexing, but for the moment, the only keys that work are strings. Any index done this way will automatically trigger a rerender.
If you need to index any tables or subtables by anything not a string, you will need to use the underlying table, gotten with `__GetTable`. This will not trigger a rerender.
To trigger a rerender manually, use `_SetDirty`, passing in the name of the top-level entry in your model table that you edited.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/DataModel.cpp#L60-L67" target="_blank">source</a>]

**Members**

### RmlUi.SolLuaDataModel:__SetDirty {#RmlUi.SolLuaDataModel:__SetDirty}
*function*

Set a table property dirty to trigger a rerender

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/DataModel.cpp#L72-L76" target="_blank">source</a>]

```lua
RmlUi.SolLuaDataModel:__SetDirty(string) -> nil
```

**Parameters**

- `property` `string`
