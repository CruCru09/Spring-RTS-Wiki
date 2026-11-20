---
title: "Encoding"
tags:
  - Lua-API
---

## Encoding {#Encoding}
*table*

Lua Encoding API

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaEncoding.cpp#L22-L25" target="_blank">source</a>]

**Members**

### Encoding.DecodeBase64 {#Encoding.DecodeBase64}
*function*

Decodes a base64 string

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaEncoding.cpp#L41-L50" target="_blank">source</a>]

Decodes a base64 encoded string. If it encounters
invalid data, it stops and returns whatever it parsed so far.

```lua
Encoding.DecodeBase64(string) -> string
```

**Parameters**

- `text` `string` — Text to decode

**Returns**

- `decoded` `string` — Decoded text

### Encoding.EncodeBase64 {#Encoding.EncodeBase64}
*function*

Encodes a base64 string

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaEncoding.cpp#L61-L68" target="_blank">source</a>]

```lua
Encoding.EncodeBase64(string, boolean?) -> string
```

**Parameters**

- `text` `string` — Text to encode
- `stripPadding` `boolean?` — Remove padding (`=` characters) at the end when 'true'. Defaults to `true`.

**Returns**

- `encoded` `string` — Encoded text

### Encoding.IsValidBase64 {#Encoding.IsValidBase64}
*function*

Validates a base64 string

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaEncoding.cpp#L85-L91" target="_blank">source</a>]

```lua
Encoding.IsValidBase64(string) -> boolean
```

**Parameters**

- `text` `string` — Text to validate

**Returns**

- `valid` `boolean` — Whether the text is valid base64

### Encoding.DecodeBase64Url {#Encoding.DecodeBase64Url}
*function*

Decodes a base64url string

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaEncoding.cpp#L109-L118" target="_blank">source</a>]

Decodes a base64url encoded string. If it encounters
invalid data, it stops and returns whatever it parsed so far.

```lua
Encoding.DecodeBase64Url(string) -> string
```

**Parameters**

- `text` `string` — Text to decode

**Returns**

- `decoded` `string` — Decoded text

### Encoding.EncodeBase64Url {#Encoding.EncodeBase64Url}
*function*

Encodes a base64url string

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaEncoding.cpp#L136-L142" target="_blank">source</a>]

```lua
Encoding.EncodeBase64Url(string) -> string
```

**Parameters**

- `text` `string` — Text to encode

**Returns**

- `encoded` `string` — Encoded text

### Encoding.IsValidBase64Url {#Encoding.IsValidBase64Url}
*function*

Validates a base64url string

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaEncoding.cpp#L164-L170" target="_blank">source</a>]

```lua
Encoding.IsValidBase64Url(string) -> boolean
```

**Parameters**

- `text` `string` — Text to validate

**Returns**

- `valid` `boolean` — Whether the text is valid base64url
