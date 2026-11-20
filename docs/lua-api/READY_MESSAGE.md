---
title: "READY_MESSAGE"
tags:
  - Lua-API
---

## READY_MESSAGE {#READY_MESSAGE}
*enum*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaHandle.cpp#L4052-L4058" target="_blank">source</a>]

- <span id="READY_MESSAGE.WAITING"></span> `READY_MESSAGE.WAITING` "Waiting for players"
- <span id="READY_MESSAGE.HOST_WAITING"></span> `READY_MESSAGE.HOST_WAITING` "Waiting for players, press key to force start" — when waiting and currently the host, key is the first key bound to the action forcestart
- <span id="READY_MESSAGE.CHOOSE_POS"></span> `READY_MESSAGE.CHOOSE_POS` "Choose start pos" — when current player is not ready and is not a spectator
- <span id="READY_MESSAGE.STARTING"></span> `READY_MESSAGE.STARTING` "Starting in n" — where n is the number of seconds
