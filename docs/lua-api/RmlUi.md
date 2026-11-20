---
title: "RmlUi"
tags:
  - Lua-API
---

## RmlUi {#RmlUi}
*table*

Global functions for Recoil's RmlUi implementation.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/RmlSolLua.cpp#L56-L59" target="_blank">source</a>]

**Members**

### RmlUi.CreateContext {#RmlUi.CreateContext}
*function*

Create a new context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L142-L149" target="_blank">source</a>]

```lua
RmlUi.CreateContext(string) -> RmlUi.Context?
```

**Parameters**

- `name` `string`

**Returns**

- `nil` `RmlUi.Context?` — if failed.

### RmlUi.RemoveContext {#RmlUi.RemoveContext}
*function*

Remove a context.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L159-L165" target="_blank">source</a>]

```lua
RmlUi.RemoveContext((string|RmlUi.Context)) -> nil
```

**Parameters**

- `context` `(string|RmlUi.Context)`

### RmlUi.LoadFontFace {#RmlUi.LoadFontFace}
*function*

Load a font face.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L170-L180" target="_blank">source</a>]

```lua
RmlUi.LoadFontFace(string, boolean?, RmlUi.font_weight?, number?) -> boolean
```

**Parameters**

- `file_path` `string`
- `fallback` `boolean?`
- `weight` `RmlUi.font_weight?`
- `face_index` `number?` — The index of the font face within a font collection.

**Returns**

- `success` `boolean`

### RmlUi.GetContext {#RmlUi.GetContext}
*function*

Get a context by name.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L188-L195" target="_blank">source</a>]

```lua
RmlUi.GetContext(string) -> RmlUi.Context?
```

**Parameters**

- `name` `string`

**Returns**

- `nil` `RmlUi.Context?` — if failed.

### RmlUi.RegiserEventType {#RmlUi.RegiserEventType}
*function*

Register a new event type.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L237-L247" target="_blank">source</a>]

```lua
RmlUi.RegiserEventType(string, boolean?, boolean?, RmlUi.default_action_phase?) -> RmlUi.EventID
```

**Parameters**

- `event_type` `string`
- `interruptible` `boolean?`
- `bubbles` `boolean?`
- `default_phase` `RmlUi.default_action_phase?`

**Returns**

- [`RmlUi.EventID`](Aliases.md#RmlUi.EventID)

### RmlUi.AddTranslationString {#RmlUi.AddTranslationString}
*function*

Add a translation string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L249-L257" target="_blank">source</a>]

```lua
RmlUi.AddTranslationString(string, string) -> boolean
```

**Parameters**

- `key` `string`
- `translation` `string`

**Returns**

- `success` `boolean`

### RmlUi.ClearTranslations {#RmlUi.ClearTranslations}
*function*

Clear registered translations.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L261-L265" target="_blank">source</a>]

```lua
RmlUi.ClearTranslations() -> nil
```

### RmlUi.SetMouseCursorAlias {#RmlUi.SetMouseCursorAlias}
*function*

Converts the css names for cursors to the Recoil Engine names for cursors like `RmlUi.SetMouseCursorAlias("pointer", 'Move')`.
Web devs tend to want to use specific words for pointer types.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L269-L277" target="_blank">source</a>]

```lua
RmlUi.SetMouseCursorAlias(string, string) -> nil
```

**Parameters**

- `rml_name` `string` — name used in rml script
- `recoil_name` `string` — name used in recoil

### RmlUi.SetDebugContext {#RmlUi.SetDebugContext}
*function*

Set which context the debug inspector is meant to inspect.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L279-L285" target="_blank">source</a>]

```lua
RmlUi.SetDebugContext((string|RmlUi.Context)) -> nil
```

**Parameters**

- `context` `(string|RmlUi.Context)`

### RmlUi.ClearDocumentPathRequests {#RmlUi.ClearDocumentPathRequests}
*function*

Clear the list of paths requested for a document for the purpose of GetDocumentPathRequests.
Does not clear anything else related to those requests themselves.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L296-L303" target="_blank">source</a>]

```lua
RmlUi.ClearDocumentPathRequests(string) -> nil
```

**Parameters**

- `document_path` `string` — path of document

### RmlUi.GetDocumentPathRequests {#RmlUi.GetDocumentPathRequests}
*function*

Retrieve the list of paths requested by the loaded RML document since the most recent RmlUi.ClearDocumentPathRequests call.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L309-L316" target="_blank">source</a>]

```lua
RmlUi.GetDocumentPathRequests(string) -> string[]
```

**Parameters**

- `document_path` `string` — path of document

**Returns**

- `array` `string[]` — of paths requested by the document

**Fields**

- <span id="RmlUi.Context"></span> `RmlUi.Context` [`RmlUi.Context`](RmlUi.Context.md#RmlUi.Context) — Holds documents and a data model.

The Context class has no constructor; it must be instantiated through the CreateContext() function. It has the following functions and properties:

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Context.cpp#L376-L380" target="_blank">source</a>]
- <span id="RmlUi.SolLuaDataModel"></span> `RmlUi.SolLuaDataModel` `RmlUi.SolLuaDataModel<T>` — Handle for a data model.

It is a wrapper around the model table, marked as type T.
You can access fields by using normal indexing, but for the moment, the only keys that work are strings. Any index done this way will automatically trigger a rerender.
If you need to index any tables or subtables by anything not a string, you will need to use the underlying table, gotten with `__GetTable`. This will not trigger a rerender.
To trigger a rerender manually, use `_SetDirty`, passing in the name of the top-level entry in your model table that you edited.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/DataModel.cpp#L60-L67" target="_blank">source</a>]
- <span id="RmlUi.RmlModalFlag"></span> `RmlUi.RmlModalFlag` [`RmlUi.RmlModalFlag`](RmlUi.RmlModalFlag.md#RmlUi.RmlModalFlag) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L102-L104" target="_blank">source</a>]
- <span id="RmlUi.RmlFocusFlag"></span> `RmlUi.RmlFocusFlag` [`RmlUi.RmlFocusFlag`](RmlUi.RmlFocusFlag.md#RmlUi.RmlFocusFlag) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L116-L118" target="_blank">source</a>]
- <span id="RmlUi.Document"></span> `RmlUi.Document` [`RmlUi.Document`](RmlUi.Document.md#RmlUi.Document) — Document derives from Element.

Document has no constructor; it must be instantiated through a Context object instead, either by loading an external RML file or creating an empty document. It has the following functions and properties:

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L132-L137" target="_blank">source</a>]
- <span id="RmlUi.EventListener"></span> `RmlUi.EventListener` [`RmlUi.EventListener`](RmlUi.EventListener.md#RmlUi.EventListener) — Event listener interface

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L223-L226" target="_blank">source</a>]
- <span id="RmlUi.Element"></span> `RmlUi.Element` [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element) — Represents an element in the RmlUi document tree. This class cannot be constructed directly; use a Document object to instantiate elements. This is the foundational piece of the DOM.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L256-L259" target="_blank">source</a>]
- <span id="RmlUi.ElementText"></span> `RmlUi.ElementText` [`RmlUi.ElementText`](RmlUi.ElementText.md#RmlUi.ElementText) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementDerived.cpp#L44-L46" target="_blank">source</a>]
- <span id="RmlUi.ElementTabSet"></span> `RmlUi.ElementTabSet` [`RmlUi.ElementTabSet`](RmlUi.ElementTabSet.md#RmlUi.ElementTabSet) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementDerived.cpp#L57-L59" target="_blank">source</a>]
- <span id="RmlUi.ElementProgress"></span> `RmlUi.ElementProgress` [`RmlUi.ElementProgress`](RmlUi.ElementProgress.md#RmlUi.ElementProgress) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementDerived.cpp#L99-L101" target="_blank">source</a>]
- <span id="RmlUi.ElementForm"></span> `RmlUi.ElementForm` [`RmlUi.ElementForm`](RmlUi.ElementForm.md#RmlUi.ElementForm) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L161-L163" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControl"></span> `RmlUi.ElementFormControl` [`RmlUi.ElementFormControl`](RmlUi.ElementFormControl.md#RmlUi.ElementFormControl) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L178-L180" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlInput"></span> `RmlUi.ElementFormControlInput` [`RmlUi.ElementFormControlInput`](RmlUi.ElementFormControlInput.md#RmlUi.ElementFormControlInput) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L200-L202" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlSelect"></span> `RmlUi.ElementFormControlSelect` [`RmlUi.ElementFormControlSelect`](RmlUi.ElementFormControlSelect.md#RmlUi.ElementFormControlSelect) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L258-L260" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlTextArea"></span> `RmlUi.ElementFormControlTextArea` [`RmlUi.ElementFormControlTextArea`](RmlUi.ElementFormControlTextArea.md#RmlUi.ElementFormControlTextArea) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L296-L298" target="_blank">source</a>]
- <span id="RmlUi.RmlEventPhase"></span> `RmlUi.RmlEventPhase` [`RmlUi.RmlEventPhase`](RmlUi.RmlEventPhase.md#RmlUi.RmlEventPhase) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Event.cpp#L66-L68" target="_blank">source</a>]
- <span id="RmlUi.EventParametersProxy"></span> `RmlUi.EventParametersProxy` [`RmlUi.EventParametersProxy`](RmlUi.EventParametersProxy.md#RmlUi.EventParametersProxy) — Keyboard and mouse input data associated with an event.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Event.cpp#L94-L107" target="_blank">source</a>]
- <span id="RmlUi.Event"></span> `RmlUi.Event` [`RmlUi.Event`](RmlUi.Event.md#RmlUi.Event) — An event that happens to an element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Event.cpp#L109-L112" target="_blank">source</a>]
- <span id="RmlUi.ElementPtr"></span> `RmlUi.ElementPtr` [`RmlUi.ElementPtr`](RmlUi.ElementPtr.md#RmlUi.ElementPtr) — Represents an owned element.

This type is mainly used to modify the DOM tree by passing the object into other elements. For example `RmlUi.Element:AppendChild()`.
A current limitation in the Lua plugin is that Element member properties and functions cannot be used directly on this type.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L110-L116" target="_blank">source</a>]
- <span id="RmlUi.contexts"></span> `RmlUi.contexts` `RmlUi.Context[]` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L289-L289" target="_blank">source</a>]
- <span id="RmlUi.version"></span> `RmlUi.version` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L292-L292" target="_blank">source</a>]
RmlUi version
- <span id="RmlUi.key_identifier"></span> `RmlUi.key_identifier` [`RmlUi.key_identifier`](RmlUi.key_identifier.md#RmlUi.key_identifier) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L321-L333" target="_blank">source</a>]
- <span id="RmlUi.key_modifier"></span> `RmlUi.key_modifier` [`RmlUi.key_modifier`](RmlUi.key_modifier.md#RmlUi.key_modifier) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L683-L685" target="_blank">source</a>]
- <span id="RmlUi.font_weight"></span> `RmlUi.font_weight` [`RmlUi.font_weight`](RmlUi.font_weight.md#RmlUi.font_weight) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L705-L707" target="_blank">source</a>]
- <span id="RmlUi.default_action_phase"></span> `RmlUi.default_action_phase` [`RmlUi.default_action_phase`](RmlUi.default_action_phase.md#RmlUi.default_action_phase) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Global.cpp#L719-L721" target="_blank">source</a>]
- <span id="RmlUi.Vector2i"></span> `RmlUi.Vector2i` [`RmlUi.Vector2i`](RmlUi.Vector2i.md#RmlUi.Vector2i) — Two-dimensional integral vector.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Vector.cpp#L40-L48" target="_blank">source</a>]
- <span id="RmlUi.Vector2f"></span> `RmlUi.Vector2f` [`RmlUi.Vector2f`](RmlUi.Vector2f.md#RmlUi.Vector2f) — Two-dimensional float vector

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Vector.cpp#L83-L92" target="_blank">source</a>]
