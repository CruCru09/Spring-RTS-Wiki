---
title: "RmlUi.ElementFormControlTextArea"
tags:
  - Lua-API
---

## RmlUi.ElementFormControlTextArea {#RmlUi.ElementFormControlTextArea}
*class*

Inherits [`RmlUi.Element`](RmlUi.Element.md#RmlUi.Element) [`RmlUi.ElementFormControl`](RmlUi.ElementFormControl.md#RmlUi.ElementFormControl)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L296-L298" target="_blank">source</a>]

**Members**

### RmlUi.ElementFormControlTextArea:Select {#RmlUi.ElementFormControlTextArea:Select}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L301-L304" target="_blank">source</a>]

Selects all text.

```lua
RmlUi.ElementFormControlTextArea:Select() -> nil
```

### RmlUi.ElementFormControlTextArea:SetSelection {#RmlUi.ElementFormControlTextArea:SetSelection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L306-L311" target="_blank">source</a>]

Selects the text in the given character range.

```lua
RmlUi.ElementFormControlTextArea:SetSelection(integer, integer) -> nil
```

**Parameters**

- `selection_start` `integer` — The first character to be selected.
- `selection_end` `integer` — The first character *after* the selection.

### RmlUi.ElementFormControlTextArea:GetSelection {#RmlUi.ElementFormControlTextArea:GetSelection}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L313-L317" target="_blank">source</a>]

Retrieves the selection range and text.

```lua
RmlUi.ElementFormControlTextArea:GetSelection() -> any
```

**Returns**

- `selection_start` `any` — The first character selected; selection_end The first character *after* the selection; selected_text The selected text.

**Fields**

- <span id="RmlUi.ElementFormControlTextArea.cols"></span> `RmlUi.ElementFormControlTextArea.cols` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L321-L321" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlTextArea.maxlength"></span> `RmlUi.ElementFormControlTextArea.maxlength` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L323-L323" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlTextArea.rows"></span> `RmlUi.ElementFormControlTextArea.rows` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L325-L325" target="_blank">source</a>]
- <span id="RmlUi.ElementFormControlTextArea.wordwrap"></span> `RmlUi.ElementFormControlTextArea.wordwrap` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/ElementForm.cpp#L327-L327" target="_blank">source</a>]
