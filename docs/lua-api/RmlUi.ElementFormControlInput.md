---
title: "RmlUi.ElementFormControlInput"
tags:
  - Lua-API
---

## RmlUi.ElementFormControlInput {#RmlUi.ElementFormControlInput}
*class*

Inherits [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element) [`RmlUi.ElementFormControl`](RmlUi.ElementFormControl.md#RmlUi.ElementFormControl)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L200-L202" target="_blank">source</a>]

**Members**

### RmlUi.ElementFormControlInput:Select {#RmlUi.ElementFormControlInput:Select}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L205-L208" target="_blank">source</a>]

Selects all text.

```lua
RmlUi.ElementFormControlInput:Select() -> nil
```

### RmlUi.ElementFormControlInput:SetSelection {#RmlUi.ElementFormControlInput:SetSelection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L210-L215" target="_blank">source</a>]

Selects the text in the given character range.

```lua
RmlUi.ElementFormControlInput:SetSelection(integer, integer) -> nil
```

**Parameters**

- `selection_start` `integer` — The first character to be selected.
- `selection_end` `integer` — The first character *after* the selection.

### RmlUi.ElementFormControlInput:GetSelection {#RmlUi.ElementFormControlInput:GetSelection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L217-L221" target="_blank">source</a>]

Retrieves the selection range and text.

```lua
RmlUi.ElementFormControlInput:GetSelection() -> any
```

**Returns**

- `selection_start` `any` — The first character selected; selection_end The first character *after* the selection; selected_text The selected text.

**Fields**

- <span id="RmlUi.ElementFormControlInput.checked"></span> `RmlUi.ElementFormControlInput.checked` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L225-L225" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlInput.maxlength"></span> `RmlUi.ElementFormControlInput.maxlength` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L227-L227" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlInput.size"></span> `RmlUi.ElementFormControlInput.size` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L229-L229" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlInput.max"></span> `RmlUi.ElementFormControlInput.max` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L231-L231" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlInput.min"></span> `RmlUi.ElementFormControlInput.min` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L233-L233" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlInput.step"></span> `RmlUi.ElementFormControlInput.step` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L235-L235" target="_blank">source</a>]
