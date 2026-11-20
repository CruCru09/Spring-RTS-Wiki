---
title: "losAccess"
tags:
  - Lua-API
---

## losAccess {#losAccess}
*class*

Parameters for los access

If one condition is fulfilled all beneath it are too (e.g. if an unit is in
LOS it can read params with `inradar=true` even if the param has
`inlos=false`) All GameRulesParam are public, TeamRulesParams can just be
`private`,`allied` and/or `public` You can read RulesParams from any Lua
environments! With those losAccess policies you can limit their access.

All GameRulesParam are public, TeamRulesParams can just be `private`,`allied` and/or `public`
You can read RulesParams from any Lua environments! With those losAccess policies you can limit their access.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L1530-L1551" target="_blank">source</a>]

**Fields**

- <span id="losAccess.private"></span> `losAccess.private` `boolean?` — only readable by the ally (default)
- <span id="losAccess.allied"></span> `losAccess.allied` `boolean?` — readable by ally + ingame allied
- <span id="losAccess.inlos"></span> `losAccess.inlos` `boolean?` — readable if the unit is in LOS
- <span id="losAccess.inradar"></span> `losAccess.inradar` `boolean?` — readable if the unit is in AirLOS
- <span id="losAccess.public"></span> `losAccess.public` `boolean?` — readable by all
