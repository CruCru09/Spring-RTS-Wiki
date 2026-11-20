---
title: "LosMask"
tags:
  - Lua-API
---

## LosMask {#LosMask}
*enum*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2922-L2929" target="_blank">source</a>]

- <span id="LosMask.INLOS"></span> `LosMask.INLOS` 1 — the unit is currently in the los of the allyteam
- <span id="LosMask.INRADAR"></span> `LosMask.INRADAR` 2 — the unit is currently in radar from the allyteam
- <span id="LosMask.PREVLOS"></span> `LosMask.PREVLOS` 4 — the unit has previously been in los from the allyteam
- <span id="LosMask.CONTRADAR"></span> `LosMask.CONTRADAR` 8 — the unit has continuously been in radar since it was last inlos by the allyteam
