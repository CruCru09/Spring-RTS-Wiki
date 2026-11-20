---
title: "RmlUi.Element"
tags:
  - Lua-API
---

## RmlUi.Element {#RmlUi.Element}
*class*

Represents an element in the RmlUi document tree. This class cannot be constructed directly; use a Document object to instantiate elements. This is the foundational piece of the DOM.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L256-L259" target="_blank">source</a>]

**Members**

### RmlUi.Element:AddEventListener {#RmlUi.Element:AddEventListener}
*function*

Adds an event listener to the element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L265-L271" target="_blank">source</a>]

```lua
RmlUi.Element:AddEventListener(string, (function|string), boolean) -> nil
```

**Parameters**

- `event` `string`
- `listener` `(function|string)`
- `in_capture_phase` `boolean`

### RmlUi.Element:AppendChild {#RmlUi.Element:AppendChild}
*function*

Appends element as a child to this element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L278-L283" target="_blank">source</a>]

```lua
RmlUi.Element:AppendChild(RmlUi.ElementPtr) -> RmlUi.ElementPtr
```

**Parameters**

- `element` [`RmlUi.ElementPtr`](RmlUi.ElementPtr.md#RmlUi.ElementPtr)

**Returns**

- [`RmlUi.ElementPtr`](RmlUi.ElementPtr.md#RmlUi.ElementPtr)

### RmlUi.Element:Blur {#RmlUi.Element:Blur}
*function*

Removes input focus from this element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L287-L290" target="_blank">source</a>]

```lua
RmlUi.Element:Blur() -> nil
```

### RmlUi.Element:Click {#RmlUi.Element:Click}
*function*

Fakes a click on this element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L292-L295" target="_blank">source</a>]

```lua
RmlUi.Element:Click() -> nil
```

### RmlUi.Element:DispatchEvent {#RmlUi.Element:DispatchEvent}
*function*

Dispatches an event to this element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L297-L304" target="_blank">source</a>]

```lua
RmlUi.Element:DispatchEvent(string, table, string) -> boolean
```

**Parameters**

- `event` `string`
- `parameters` `table`
- `interruptible` `string`

**Returns**

- `boolean`

### RmlUi.Element:Focus {#RmlUi.Element:Focus}
*function*

Gives input focus to this element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L306-L309" target="_blank">source</a>]

```lua
RmlUi.Element:Focus() -> nil
```

### RmlUi.Element:GetAttribute {#RmlUi.Element:GetAttribute}
*function*

Returns the value of the attribute named name. If no such attribute exists, the empty string will be returned.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L314-L319" target="_blank">source</a>]

```lua
RmlUi.Element:GetAttribute(string) -> string?
```

**Parameters**

- `name` `string`

**Returns**

- `string?`

### RmlUi.Element:GetElementById {#RmlUi.Element:GetElementById}
*function*

Returns the descendant element with an id of id.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L321-L326" target="_blank">source</a>]

```lua
RmlUi.Element:GetElementById(string) -> RmlUi.Element?
```

**Parameters**

- `id` `string`

**Returns**

- `RmlUi.Element?`

### RmlUi.Element:GetElementsByTagName {#RmlUi.Element:GetElementsByTagName}
*function*

Returns a list of all descendant elements with the tag of tag_name.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L328-L333" target="_blank">source</a>]

```lua
RmlUi.Element:GetElementsByTagName(string) -> RmlUi.ElementPtr[]
```

**Parameters**

- `tag_name` `string`

**Returns**

- `RmlUi.ElementPtr[]`

### RmlUi.Element:QuerySelector {#RmlUi.Element:QuerySelector}
*function*

JQuery-like element selector

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L335-L340" target="_blank">source</a>]

```lua
RmlUi.Element:QuerySelector(string) -> RmlUi.ElementPtr?
```

**Parameters**

- `query` `string`

**Returns**

- `RmlUi.ElementPtr?`

### RmlUi.Element:QuerySelectorAll {#RmlUi.Element:QuerySelectorAll}
*function*

JQuery-like element selector

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L342-L347" target="_blank">source</a>]

```lua
RmlUi.Element:QuerySelectorAll(string) -> RmlUi.ElementPtr[]
```

**Parameters**

- `selectors` `string`

**Returns**

- `RmlUi.ElementPtr[]`

### RmlUi.Element:Matches {#RmlUi.Element:Matches}
*function*

Checks if the current element matches the given RCSS selector(s).

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L349-L354" target="_blank">source</a>]

```lua
RmlUi.Element:Matches(string) -> boolean
```

**Parameters**

- `selectors` `string`

**Returns**

- `boolean`

### RmlUi.Element:HasAttribute {#RmlUi.Element:HasAttribute}
*function*

Returns True if the element has a value for the attribute named name, False if not.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L356-L361" target="_blank">source</a>]

```lua
RmlUi.Element:HasAttribute(string) -> boolean
```

**Parameters**

- `name` `string`

**Returns**

- `boolean`

### RmlUi.Element:HasChildNodes {#RmlUi.Element:HasChildNodes}
*function*

Returns True if the element has at least one child node, false if not.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L363-L367" target="_blank">source</a>]

```lua
RmlUi.Element:HasChildNodes() -> boolean
```

**Returns**

- `boolean`

### RmlUi.Element:InsertBefore {#RmlUi.Element:InsertBefore}
*function*

Inserts the element element as a child of this element, directly before adjacent_element in the list of children.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L369-L375" target="_blank">source</a>]

```lua
RmlUi.Element:InsertBefore(RmlUi.ElementPtr, RmlUi.Element) -> RmlUi.Element?
```

**Parameters**

- `element` [`RmlUi.ElementPtr`](RmlUi.ElementPtr.md#RmlUi.ElementPtr)
- `adjacent_element` [`RmlUi.Element`](#RmlUi.Element)

**Returns**

- `RmlUi.Element?`

### RmlUi.Element:IsClassSet {#RmlUi.Element:IsClassSet}
*function*

Returns true if the class name is set on the element, false if not.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L379-L384" target="_blank">source</a>]

```lua
RmlUi.Element:IsClassSet(string) -> boolean
```

**Parameters**

- `name` `string`

**Returns**

- `boolean`

### RmlUi.Element:RemoveAttribute {#RmlUi.Element:RemoveAttribute}
*function*

Removes the attribute named name from the element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L386-L390" target="_blank">source</a>]

```lua
RmlUi.Element:RemoveAttribute(string) -> nil
```

**Parameters**

- `name` `string`

### RmlUi.Element:RemoveChild {#RmlUi.Element:RemoveChild}
*function*

Removes the child element element from this element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L392-L397" target="_blank">source</a>]

```lua
RmlUi.Element:RemoveChild(RmlUi.Element) -> boolean
```

**Parameters**

- `element` [`RmlUi.Element`](#RmlUi.Element)

**Returns**

- `boolean`

### RmlUi.Element:ReplaceChild {#RmlUi.Element:ReplaceChild}
*function*

Replaces the child element replaced_element with inserted_element in this element's list of children. If replaced_element is not a child of this element, inserted_element will be appended onto the list instead.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L399-L405" target="_blank">source</a>]

```lua
RmlUi.Element:ReplaceChild(RmlUi.ElementPtr, RmlUi.Element) -> boolean
```

**Parameters**

- `inserted_element` [`RmlUi.ElementPtr`](RmlUi.ElementPtr.md#RmlUi.ElementPtr)
- `replaced_element` [`RmlUi.Element`](#RmlUi.Element)

**Returns**

- `boolean`

### RmlUi.Element:ScrollIntoView {#RmlUi.Element:ScrollIntoView}
*function*

Scrolls this element into view if its ancestors have hidden overflow.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L409-L413" target="_blank">source</a>]

```lua
RmlUi.Element:ScrollIntoView(boolean) -> nil
```

**Parameters**

- `align_with_top` `boolean`

### RmlUi.Element:SetAttribute {#RmlUi.Element:SetAttribute}
*function*

Sets the value of the attribute named name to value.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L420-L425" target="_blank">source</a>]

```lua
RmlUi.Element:SetAttribute(string, string) -> nil
```

**Parameters**

- `name` `string`
- `value` `string`

### RmlUi.Element:SetClass {#RmlUi.Element:SetClass}
*function*

Sets (if value is true) or clears (if value is false) the class name on the element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L427-L432" target="_blank">source</a>]

```lua
RmlUi.Element:SetClass(string, boolean) -> nil
```

**Parameters**

- `name` `string`
- `value` `boolean`

### RmlUi.Element:GetElementsByClassName {#RmlUi.Element:GetElementsByClassName}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L435-L439" target="_blank">source</a>]

```lua
RmlUi.Element:GetElementsByClassName(string) -> RmlUi.Element[]
```

**Parameters**

- `class_name` `string`

**Returns**

- `RmlUi.Element[]`

### RmlUi.Element:Clone {#RmlUi.Element:Clone}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L441-L444" target="_blank">source</a>]

```lua
RmlUi.Element:Clone() -> RmlUi.ElementPtr
```

**Returns**

- [`RmlUi.ElementPtr`](RmlUi.ElementPtr.md#RmlUi.ElementPtr)

### RmlUi.Element:Closest {#RmlUi.Element:Closest}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L446-L449" target="_blank">source</a>]

```lua
RmlUi.Element:Closest() -> RmlUi.Element?
```

**Returns**

- `RmlUi.Element?`

### RmlUi.Element:SetPseudoClass {#RmlUi.Element:SetPseudoClass}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L451-L454" target="_blank">source</a>]

```lua
RmlUi.Element:SetPseudoClass(string) -> nil
```

**Parameters**

- `class_name` `string`

### RmlUi.Element:IsPseudoClassSet {#RmlUi.Element:IsPseudoClassSet}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L456-L460" target="_blank">source</a>]

```lua
RmlUi.Element:IsPseudoClassSet(string) -> boolean
```

**Parameters**

- `class_name` `string`

**Returns**

- `boolean`

### RmlUi.Element:ArePseudoCLassesSet {#RmlUi.Element:ArePseudoCLassesSet}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L462-L466" target="_blank">source</a>]

```lua
RmlUi.Element:ArePseudoCLassesSet(string[]) -> boolean
```

**Parameters**

- `class_names` `string[]`

**Returns**

- `boolean`

### RmlUi.Element:GetActivePseudoCLasses {#RmlUi.Element:GetActivePseudoCLasses}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L468-L471" target="_blank">source</a>]

```lua
RmlUi.Element:GetActivePseudoCLasses() -> string[]
```

**Returns**

- `string[]`

### RmlUi.Element:IsPointWithinElement {#RmlUi.Element:IsPointWithinElement}
*function*

Is a screen-space point within this element?

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L473-L478" target="_blank">source</a>]

```lua
RmlUi.Element:IsPointWithinElement(RmlUi.Vector2f) -> boolean
```

**Parameters**

- `point` [`RmlUi.Vector2f`](RmlUi.Vector2f.md#RmlUi.Vector2f)

**Returns**

- `boolean`

### RmlUi.Element:ProcessDefaultAction {#RmlUi.Element:ProcessDefaultAction}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L480-L483" target="_blank">source</a>]

```lua
RmlUi.Element:ProcessDefaultAction(RmlUi.Event) -> nil
```

**Parameters**

- `event` [`RmlUi.Event`](RmlUi.Event.md#RmlUi.Event)

### RmlUi.Element:IsVisible {#RmlUi.Element:IsVisible}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L485-L489" target="_blank">source</a>]

True if the element is visible, false otherwise.

```lua
RmlUi.Element:IsVisible() -> boolean
```

**Returns**

- `boolean`

### RmlUi.Element:GetValue {#RmlUi.Element:GetValue}
*function*

Get the value of this element.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L494-L498" target="_blank">source</a>]

```lua
RmlUi.Element:GetValue() -> (number|string|"")
```

**Returns**

- `value` `(number|string|"")` — Returns number if it has the tag "input", a string if it has the tag "textarea", else an empty string.

### RmlUi.Element:GetChild {#RmlUi.Element:GetChild}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L507-L511" target="_blank">source</a>]

```lua
RmlUi.Element:GetChild(integer) -> RmlUi.Element?
```

**Parameters**

- `index` `integer`

**Returns**

- `RmlUi.Element?`

**Fields**

- <span id="RmlUi.Element.class_name"></span> `RmlUi.Element.class_name` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L515-L515" target="_blank">source</a>]
Name of the class.
- <span id="RmlUi.Element.id"></span> `RmlUi.Element.id` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L517-L517" target="_blank">source</a>]
ID of this element, in the context of `<span id="foo">`.
- <span id="RmlUi.Element.inner_rml"></span> `RmlUi.Element.inner_rml` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L519-L519" target="_blank">source</a>]
Gets or sets the inner RML (markup) content of the element.
- <span id="RmlUi.Element.scroll_left"></span> `RmlUi.Element.scroll_left` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L521-L521" target="_blank">source</a>]
Gets or sets the number of pixels that the content of the element is scrolled from the left.
- <span id="RmlUi.Element.scroll_top"></span> `RmlUi.Element.scroll_top` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L523-L523" target="_blank">source</a>]
Gets or sets the number of pixels that the content of the element is scrolled from the top.
- <span id="RmlUi.Element.attributes"></span> `RmlUi.Element.attributes` [`RmlUi.ElementAttributesProxy`](Aliases.md#RmlUi.ElementAttributesProxy) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L527-L527" target="_blank">source</a>]
Read-only. Proxy for accessing element attributes.
- <span id="RmlUi.Element.child_nodes"></span> `RmlUi.Element.child_nodes` [`RmlUi.ElementChildNodesProxy`](Aliases.md#RmlUi.ElementChildNodesProxy) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L529-L529" target="_blank">source</a>]
Read-only. Proxy for accessing child nodes of the element.
- <span id="RmlUi.Element.client_left"></span> `RmlUi.Element.client_left` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L531-L531" target="_blank">source</a>]
Read-only. The width of the left border of the element in pixels.
- <span id="RmlUi.Element.client_height"></span> `RmlUi.Element.client_height` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L533-L533" target="_blank">source</a>]
Read-only. The inner height of the element in pixels, including padding but not the horizontal scrollbar height, border, or margin.
- <span id="RmlUi.Element.client_top"></span> `RmlUi.Element.client_top` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L535-L535" target="_blank">source</a>]
Read-only. The width of the top border of the element in pixels.
- <span id="RmlUi.Element.client_width"></span> `RmlUi.Element.client_width` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L537-L537" target="_blank">source</a>]
Read-only. The inner width of the element in pixels, including padding but not the vertical scrollbar width, border, or margin.
- <span id="RmlUi.Element.first_child"></span> `RmlUi.Element.first_child` `RmlUi.Element?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L539-L539" target="_blank">source</a>]
Read-only. The first child element, or nil if there are no children.
- <span id="RmlUi.Element.last_child"></span> `RmlUi.Element.last_child` `RmlUi.Element?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L541-L541" target="_blank">source</a>]
Read-only. The last child element, or nil if there are no children.
- <span id="RmlUi.Element.next_sibling"></span> `RmlUi.Element.next_sibling` `RmlUi.Element?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L543-L543" target="_blank">source</a>]
Read-only. The next sibling element, or nil if there is none.
- <span id="RmlUi.Element.offset_height"></span> `RmlUi.Element.offset_height` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L545-L545" target="_blank">source</a>]
Read-only. The height of the element including vertical padding and borders, in pixels.
- <span id="RmlUi.Element.offset_left"></span> `RmlUi.Element.offset_left` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L547-L547" target="_blank">source</a>]
Read-only. The distance from the inner left edge of the offset parent, in pixels.
- <span id="RmlUi.Element.offset_parent"></span> `RmlUi.Element.offset_parent` [`RmlUi.Element`](#RmlUi.Element) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L549-L549" target="_blank">source</a>]
Read-only. The closest positioned ancestor element.
- <span id="RmlUi.Element.offset_top"></span> `RmlUi.Element.offset_top` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L551-L551" target="_blank">source</a>]
Read-only. The distance from the inner top edge of the offset parent, in pixels.
- <span id="RmlUi.Element.offset_width"></span> `RmlUi.Element.offset_width` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L553-L553" target="_blank">source</a>]
Read-only. The width of the element including horizontal padding and borders, in pixels.
- <span id="RmlUi.Element.owner_document"></span> `RmlUi.Element.owner_document` [`RmlUi.Document`](RmlUi.Document.md#RmlUi.Document) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L555-L555" target="_blank">source</a>]
Read-only. The document that owns this element.
- <span id="RmlUi.Element.parent_node"></span> `RmlUi.Element.parent_node` `RmlUi.Element?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L557-L557" target="_blank">source</a>]
Read-only. The parent node of this element, or nil if there is none.
- <span id="RmlUi.Element.previous_sibling"></span> `RmlUi.Element.previous_sibling` `RmlUi.Element?` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L559-L559" target="_blank">source</a>]
Read-only. The previous sibling element, or nil if there is none.
- <span id="RmlUi.Element.scroll_height"></span> `RmlUi.Element.scroll_height` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L561-L561" target="_blank">source</a>]
Read-only. The total height of the element's content, including content not visible on the screen due to overflow.
- <span id="RmlUi.Element.scroll_width"></span> `RmlUi.Element.scroll_width` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L563-L563" target="_blank">source</a>]
Read-only. The total width of the element's content, including content not visible on the screen due to overflow.
- <span id="RmlUi.Element.style"></span> `RmlUi.Element.style` [`RmlUi.ElementStyleProxy`](Aliases.md#RmlUi.ElementStyleProxy) — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L565-L565" target="_blank">source</a>]
Read-only. Proxy for accessing and modifying the element's style properties.
- <span id="RmlUi.Element.tag_name"></span> `RmlUi.Element.tag_name` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L567-L567" target="_blank">source</a>]
Read-only. The tag name of the element.
- <span id="RmlUi.Element.address"></span> `RmlUi.Element.address` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L570-L570" target="_blank">source</a>]
Read-only. The address of the element in the document tree.
- <span id="RmlUi.Element.absolute_left"></span> `RmlUi.Element.absolute_left` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L572-L572" target="_blank">source</a>]
Read-only. The absolute left position of the element relative to the document.
- <span id="RmlUi.Element.absolute_top"></span> `RmlUi.Element.absolute_top` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L574-L574" target="_blank">source</a>]
Read-only. The absolute top position of the element relative to the document.
- <span id="RmlUi.Element.baseline"></span> `RmlUi.Element.baseline` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L576-L576" target="_blank">source</a>]
Read-only. The baseline position of the element.
- <span id="RmlUi.Element.line_height"></span> `RmlUi.Element.line_height` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L578-L578" target="_blank">source</a>]
Read-only. The computed line height of the element.
- <span id="RmlUi.Element.visible"></span> `RmlUi.Element.visible` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L580-L580" target="_blank">source</a>]
Read-only. True if the element is visible, false otherwise.
- <span id="RmlUi.Element.z_index"></span> `RmlUi.Element.z_index` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Rml/SolLua/bind/Element.cpp#L582-L582" target="_blank">source</a>]
Read-only. The computed z-index of the element.
