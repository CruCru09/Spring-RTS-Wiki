---
title: "Menu"
tags:
  - Lua-API
---

## Menu {#Menu}
*class*

Inherits [`Callins`](Callins.md#Callins)

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaMenu.cpp#L33-L36" target="_blank">source</a>]

**Members**

### Menu:ActivateMenu {#Menu:ActivateMenu}
*function*

Called whenever LuaMenu is on with no game loaded.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaMenu.cpp#L328-L331" target="_blank">source</a>]

```lua
Menu:ActivateMenu() -> nil
```

### Menu:ActivateGame {#Menu:ActivateGame}
*function*

Called whenever LuaMenu is on with a game loaded.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaMenu.cpp#L349-L352" target="_blank">source</a>]

```lua
Menu:ActivateGame() -> nil
```

### Menu:AllowDraw {#Menu:AllowDraw}
*function*

Enables Draw{Genesis,Screen,ScreenPost} callins if true is returned,
otherwise they are called once every 30 seconds. Only active when a game
isn't running.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaMenu.cpp#L369-L376" target="_blank">source</a>]

```lua
Menu:AllowDraw() -> boolean
```

**Returns**

- `allowDraw` `boolean`
