---
title: "RmlUi.Document"
tags:
  - Lua-API
---

## RmlUi.Document {#RmlUi.Document}
*class*

Inherits [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element)

Document derives from Element.

Document has no constructor; it must be instantiated through a Context object instead, either by loading an external RML file or creating an empty document. It has the following functions and properties:

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L132-L137" target="_blank">source</a>]

**Members**

### RmlUi.Document:PullToFront {#RmlUi.Document:PullToFront}
*function*

Pulls the document in front of other documents within its context with a similar z-index.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L141-L144" target="_blank">source</a>]

```lua
RmlUi.Document:PullToFront() -> nil
```

### RmlUi.Document:PushToBack {#RmlUi.Document:PushToBack}
*function*

Pushes the document behind other documents within its context with a similar z-index.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L146-L149" target="_blank">source</a>]

```lua
RmlUi.Document:PushToBack() -> nil
```

### RmlUi.Document:Show {#RmlUi.Document:Show}
*function*

Shows the document.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L151-L156" target="_blank">source</a>]

```lua
RmlUi.Document:Show(RmlUi.RmlModalFlag?, RmlUi.RmlFocusFlag?) -> nil
```

**Parameters**

- `modal` `RmlUi.RmlModalFlag?` — Defaults to Focus
- `focus` `RmlUi.RmlFocusFlag?`

### RmlUi.Document:Hide {#RmlUi.Document:Hide}
*function*

Hides the document.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L158-L161" target="_blank">source</a>]

```lua
RmlUi.Document:Hide() -> nil
```

### RmlUi.Document:Close {#RmlUi.Document:Close}
*function*

Hides and closes the document, destroying its contents.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L163-L166" target="_blank">source</a>]

```lua
RmlUi.Document:Close() -> nil
```

### RmlUi.Document:CreateElement {#RmlUi.Document:CreateElement}
*function*

Instances an element with a tag of tag_name.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L168-L173" target="_blank">source</a>]

```lua
RmlUi.Document:CreateElement(string) -> RmlUi.ElementPtr
```

**Parameters**

- `tag_name` `string`

**Returns**

- [`RmlUi.ElementPtr`](RmlUi.ElementPtr.md#RmlUi.ElementPtr)

### RmlUi.Document:CreateTextNode {#RmlUi.Document:CreateTextNode}
*function*

Instances a text element containing the string text.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L175-L180" target="_blank">source</a>]

```lua
RmlUi.Document:CreateTextNode(string) -> RmlUi.ElementPtr
```

**Parameters**

- `text` `string`

**Returns**

- [`RmlUi.ElementPtr`](RmlUi.ElementPtr.md#RmlUi.ElementPtr)

### RmlUi.Document:ReloadStyleSheet {#RmlUi.Document:ReloadStyleSheet}
*function*

Reload the active style sheet.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L183-L187" target="_blank">source</a>]

```lua
RmlUi.Document:ReloadStyleSheet(boolean?) -> nil
```

**Parameters**

- `load` `boolean?`

### RmlUi.Document:LoadInlineScript {#RmlUi.Document:LoadInlineScript}
*function*

Load scripts as if it were in the script tag.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L189-L195" target="_blank">source</a>]

```lua
RmlUi.Document:LoadInlineScript(string, string?, integer?) -> nil
```

**Parameters**

- `content` `string`
- `source` `string?`
- `source_line` `integer?`

### RmlUi.Document:LoadExternalScript {#RmlUi.Document:LoadExternalScript}
*function*

Load an external script.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L197-L201" target="_blank">source</a>]

```lua
RmlUi.Document:LoadExternalScript(string) -> nil
```

**Parameters**

- `source_path` `string`

### RmlUi.Document:UpdateDocument {#RmlUi.Document:UpdateDocument}
*function*

Update the Document.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L203-L206" target="_blank">source</a>]

```lua
RmlUi.Document:UpdateDocument() -> nil
```

### RmlUi.Document:AppendToStyleSheet {#RmlUi.Document:AppendToStyleSheet}
*function*

Append text to style sheet.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L208-L212" target="_blank">source</a>]

```lua
RmlUi.Document:AppendToStyleSheet(string) -> nil
```

**Parameters**

- `content` `string`

**Fields**

- <span id="RmlUi.Document.title"></span> `RmlUi.Document.title` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L216-L216" target="_blank">source</a>]
- <span id="RmlUi.Document.context"></span> `RmlUi.Document.context` [`RmlUi.Context`](RmlUi.Context.md#RmlUi.Context) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L220-L220" target="_blank">source</a>]
- <span id="RmlUi.Document.url"></span> `RmlUi.Document.url` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L223-L223" target="_blank">source</a>]
- <span id="RmlUi.Document.modal"></span> `RmlUi.Document.modal` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L225-L225" target="_blank">source</a>]
Is it modal?
- <span id="RmlUi.Document.widget"></span> `RmlUi.Document.widget` `table` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Document.cpp#L227-L227" target="_blank">source</a>]
A table of data that can be accessed in onevent attributes. It doesn't have to be a widget.
