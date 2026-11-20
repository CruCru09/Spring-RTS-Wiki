---
title: "RmlUi.Context"
tags:
  - Lua-API
---

## RmlUi.Context {#RmlUi.Context}
*class*

Holds documents and a data model.

The Context class has no constructor; it must be instantiated through the CreateContext() function. It has the following functions and properties:

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L376-L380" target="_blank">source</a>]

**Members**

### RmlUi.Context:AddEventListener {#RmlUi.Context:AddEventListener}
*function*

Adds the inline Lua script, script, as an event listener to the context. element_context is an optional Element; if it is not None, then the script will be executed as if it was bound to that element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L385-L392" target="_blank">source</a>]

```lua
RmlUi.Context:AddEventListener(string, RmlUi.Element, boolean, boolean) -> nil
```

**Parameters**

- `event` `string`
- `script` [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element)
- `element_context` `boolean`
- `in_capture_phase` `boolean`

### RmlUi.Context:CreateDocument {#RmlUi.Context:CreateDocument}
*function*

Creates a new document with the tag name of tag.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L394-L399" target="_blank">source</a>]

```lua
RmlUi.Context:CreateDocument(string) -> RmlUi.Document
```

**Parameters**

- `tag` `string`

**Returns**

- [`RmlUi.Document`](RmlUi.Document.md#RmlUi.Document)

### RmlUi.Context:LoadDocument {#RmlUi.Context:LoadDocument}
*function*

Attempts to load a document from the RML file found at document_path. If successful, the document will be returned with a reference count of one.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L405-L410" target="_blank">source</a>]

```lua
RmlUi.Context:LoadDocument(string) -> RmlUi.Document
```

**Parameters**

- `document_path` `string`

**Returns**

- [`RmlUi.Document`](RmlUi.Document.md#RmlUi.Document)

### RmlUi.Context:GetDocument {#RmlUi.Context:GetDocument}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L421-L424" target="_blank">source</a>]

```lua
RmlUi.Context:GetDocument(string) -> nil
```

**Parameters**

- `name` `string`

### RmlUi.Context:Render {#RmlUi.Context:Render}
*function*

Renders the context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L426-L430" target="_blank">source</a>]

```lua
RmlUi.Context:Render() -> boolean
```

**Returns**

- `boolean`

### RmlUi.Context:UnloadAllDocuments {#RmlUi.Context:UnloadAllDocuments}
*function*

Closes all documents currently loaded with the context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L437-L440" target="_blank">source</a>]

```lua
RmlUi.Context:UnloadAllDocuments() -> nil
```

### RmlUi.Context:UnloadDocument {#RmlUi.Context:UnloadDocument}
*function*

Unloads a specific document within the context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L442-L446" target="_blank">source</a>]

```lua
RmlUi.Context:UnloadDocument(RmlUi.Document) -> nil
```

**Parameters**

- `document` [`RmlUi.Document`](RmlUi.Document.md#RmlUi.Document)

### RmlUi.Context:Update {#RmlUi.Context:Update}
*function*

Updates the context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L448-L452" target="_blank">source</a>]

```lua
RmlUi.Context:Update() -> boolean
```

**Returns**

- `boolean`

### RmlUi.Context:OpenDataModel {#RmlUi.Context:OpenDataModel}
*function*

Create a new data model from a base table `model` and register to the context. The model table is copied.
Note that `widget` does not actually have to be a widget; it can be any table. This table can be accessed in widgets like `<button class="mode-button" onclick="widget:SetCamMode()">Set Dolly Mode</button>`. Also note that your data model is inaccessible in `onx` properties.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L454-L463" target="_blank">source</a>]

```lua
RmlUi.Context:OpenDataModel(string, T, table) -> SolLuaDataModel<T>
```

**Parameters**

- `name` `string`
- `model` `T`
- `widget` `table`

**Returns**

- `SolLuaDataModel<T>`

### RmlUi.Context:RemoveDataModel {#RmlUi.Context:RemoveDataModel}
*function*

Removes a data model from the context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L465-L469" target="_blank">source</a>]

```lua
RmlUi.Context:RemoveDataModel(string) -> nil
```

**Parameters**

- `name` `string`

### RmlUi.Context:ProcessMouseMove {#RmlUi.Context:ProcessMouseMove}
*function*

Processes a mouse move event.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L471-L476" target="_blank">source</a>]

```lua
RmlUi.Context:ProcessMouseMove(RmlUi.Vector2f) -> boolean
```

**Parameters**

- `position` [`RmlUi.Vector2f`](RmlUi.Vector2f.md#RmlUi.Vector2f)

**Returns**

- `boolean`

### RmlUi.Context:ProcessMouseButtonDown {#RmlUi.Context:ProcessMouseButtonDown}
*function*

Processes a mouse button down event.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L478-L484" target="_blank">source</a>]

```lua
RmlUi.Context:ProcessMouseButtonDown(RmlUi.MouseButton, integer) -> boolean
```

**Parameters**

- `button` [`RmlUi.MouseButton`](Aliases.md#RmlUi.MouseButton)
- `key_modifier_state` `integer`

**Returns**

- `boolean`

### RmlUi.Context:ProcessMouseButtonUp {#RmlUi.Context:ProcessMouseButtonUp}
*function*

Processes a mouse button up event.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L486-L492" target="_blank">source</a>]

```lua
RmlUi.Context:ProcessMouseButtonUp(RmlUi.MouseButton, integer) -> boolean
```

**Parameters**

- `button` [`RmlUi.MouseButton`](Aliases.md#RmlUi.MouseButton)
- `key_modifier_state` `integer`

**Returns**

- `boolean`

### RmlUi.Context:ProcessMouseWheel {#RmlUi.Context:ProcessMouseWheel}
*function*

Processes a mouse wheel event.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L494-L500" target="_blank">source</a>]

```lua
RmlUi.Context:ProcessMouseWheel((RmlUi.Vector2f|number), integer) -> boolean
```

**Parameters**

- `delta` `(RmlUi.Vector2f|number)`
- `key_modifier_state` `integer`

**Returns**

- `boolean`

### RmlUi.Context:ProcessMouseLeave {#RmlUi.Context:ProcessMouseLeave}
*function*

Processes a mouse leave event.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L504-L508" target="_blank">source</a>]

```lua
RmlUi.Context:ProcessMouseLeave() -> boolean
```

**Returns**

- `boolean`

### RmlUi.Context:IsMouseInteracting {#RmlUi.Context:IsMouseInteracting}
*function*

Returns true if the mouse is currently interacting with the context, false if not.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L510-L514" target="_blank">source</a>]

```lua
RmlUi.Context:IsMouseInteracting() -> boolean
```

**Returns**

- `boolean`

### RmlUi.Context:ProcessKeyDown {#RmlUi.Context:ProcessKeyDown}
*function*

Processes a key down event.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L516-L522" target="_blank">source</a>]

```lua
RmlUi.Context:ProcessKeyDown(RmlUi.key_identifier, integer) -> boolean
```

**Parameters**

- `key` [`RmlUi.key_identifier`](RmlUi.key_identifier.md#RmlUi.key_identifier)
- `key_modifier_state` `integer`

**Returns**

- `boolean`

### RmlUi.Context:ProcessKeyUp {#RmlUi.Context:ProcessKeyUp}
*function*

Processes a key up event.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L524-L530" target="_blank">source</a>]

```lua
RmlUi.Context:ProcessKeyUp(RmlUi.key_identifier, integer) -> boolean
```

**Parameters**

- `key` [`RmlUi.key_identifier`](RmlUi.key_identifier.md#RmlUi.key_identifier)
- `key_modifier_state` `integer`

**Returns**

- `boolean`

### RmlUi.Context:ProcessTextInput {#RmlUi.Context:ProcessTextInput}
*function*

Processes a text input event.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L532-L537" target="_blank">source</a>]

```lua
RmlUi.Context:ProcessTextInput(string) -> boolean
```

**Parameters**

- `text` `string`

**Returns**

- `boolean`

### RmlUi.Context:EnableMouseCursor {#RmlUi.Context:EnableMouseCursor}
*function*

Enables or disables the mouse cursor for the context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L540-L544" target="_blank">source</a>]

```lua
RmlUi.Context:EnableMouseCursor(boolean) -> nil
```

**Parameters**

- `enable` `boolean`

### RmlUi.Context:ActivateTheme {#RmlUi.Context:ActivateTheme}
*function*

Activates a theme for the context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L546-L551" target="_blank">source</a>]

```lua
RmlUi.Context:ActivateTheme(string, boolean) -> nil
```

**Parameters**

- `theme_name` `string`
- `activate` `boolean`

### RmlUi.Context:IsThemeActive {#RmlUi.Context:IsThemeActive}
*function*

Returns true if the theme is active, false if not.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L553-L558" target="_blank">source</a>]

```lua
RmlUi.Context:IsThemeActive(string) -> boolean
```

**Parameters**

- `theme_name` `string`

**Returns**

- `boolean`

### RmlUi.Context:GetElementAtPoint {#RmlUi.Context:GetElementAtPoint}
*function*

Returns the element at the point specified by point.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L560-L566" target="_blank">source</a>]

```lua
RmlUi.Context:GetElementAtPoint(RmlUi.Vector2f, RmlUi.Element?) -> RmlUi.Element
```

**Parameters**

- `point` [`RmlUi.Vector2f`](RmlUi.Vector2f.md#RmlUi.Vector2f)
- `ignore` `RmlUi.Element?`

**Returns**

- [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element)

### RmlUi.Context:PullDocumentToFront {#RmlUi.Context:PullDocumentToFront}
*function*

Pulls the document to the front of the context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L568-L572" target="_blank">source</a>]

```lua
RmlUi.Context:PullDocumentToFront(RmlUi.Document) -> nil
```

**Parameters**

- `document` [`RmlUi.Document`](RmlUi.Document.md#RmlUi.Document)

### RmlUi.Context:PushDocumentToBack {#RmlUi.Context:PushDocumentToBack}
*function*

Pushes the document to the back of the context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L574-L578" target="_blank">source</a>]

```lua
RmlUi.Context:PushDocumentToBack(RmlUi.Document) -> nil
```

**Parameters**

- `document` [`RmlUi.Document`](RmlUi.Document.md#RmlUi.Document)

**Fields**

- <span id="RmlUi.Context.dimensions"></span> `RmlUi.Context.dimensions` [`RmlUi.Vector2i`](RmlUi.Vector2i.md#RmlUi.Vector2i) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L582-L582" target="_blank">source</a>]
- <span id="RmlUi.Context.dp_ratio"></span> `RmlUi.Context.dp_ratio` `number` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L584-L584" target="_blank">source</a>]
- <span id="RmlUi.Context.documents"></span> `RmlUi.Context.documents` `RmlUi.Document[]` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L587-L587" target="_blank">source</a>]
- <span id="RmlUi.Context.focus_element"></span> `RmlUi.Context.focus_element` [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L589-L589" target="_blank">source</a>]
- <span id="RmlUi.Context.hover_element"></span> `RmlUi.Context.hover_element` [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L591-L591" target="_blank">source</a>]
- <span id="RmlUi.Context.name"></span> `RmlUi.Context.name` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L593-L593" target="_blank">source</a>]
- <span id="RmlUi.Context.root_element"></span> `RmlUi.Context.root_element` [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L595-L595" target="_blank">source</a>]
