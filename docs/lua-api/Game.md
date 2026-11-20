---
title: "Game"
tags:
  - Lua-API
---

## Game {#Game}
*table*

Game specific information

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstGame.cpp#L36-L121" target="_blank">source</a>]

**Fields**

- <span id="Game.maxUnits"></span> `Game.maxUnits` `integer`
- <span id="Game.maxTeams"></span> `Game.maxTeams` `integer`
- <span id="Game.maxPlayers"></span> `Game.maxPlayers` `integer`
- <span id="Game.squareSize"></span> `Game.squareSize` `integer` — Divide Game.mapSizeX or Game.mapSizeZ by this to get engine's "mapDims" coordinates. The resolution of height, yard and type maps.
- <span id="Game.metalMapSquareSize"></span> `Game.metalMapSquareSize` `integer` — The resolution of metalmap (for use in API such as Spring.GetMetalAmount etc.)
- <span id="Game.gameSpeed"></span> `Game.gameSpeed` `integer` — Number of simulation gameframes per second
- <span id="Game.startPosType"></span> `Game.startPosType` `integer`
- <span id="Game.ghostedBuildings"></span> `Game.ghostedBuildings` `boolean`
- <span id="Game.mapChecksum"></span> `Game.mapChecksum` `string`
- <span id="Game.modChecksum"></span> `Game.modChecksum` `string`
- <span id="Game.mapDamage"></span> `Game.mapDamage` `boolean`
- <span id="Game.mapName"></span> `Game.mapName` `string`
- <span id="Game.mapDescription"></span> `Game.mapDescription` `string` — = string Game.mapHumanName
- <span id="Game.mapHardness"></span> `Game.mapHardness` `number`
- <span id="Game.mapX"></span> `Game.mapX` `integer`
- <span id="Game.mapY"></span> `Game.mapY` `integer`
- <span id="Game.mapSizeX"></span> `Game.mapSizeX` `integer` — in worldspace/opengl coords. Divide by Game.squareSize to get engine's "mapDims" coordinates
- <span id="Game.mapSizeZ"></span> `Game.mapSizeZ` `integer` — in worldspace/opengl coords. Divide by Game.squareSize to get engine's "mapDims" coordinates
- <span id="Game.gravity"></span> `Game.gravity` `number`
- <span id="Game.tidal"></span> `Game.tidal` `number`
- <span id="Game.windMin"></span> `Game.windMin` `number`
- <span id="Game.windMax"></span> `Game.windMax` `number`
- <span id="Game.extractorRadius"></span> `Game.extractorRadius` `number`
- <span id="Game.waterDamage"></span> `Game.waterDamage` `number`
- <span id="Game.envDamageTypes"></span> `Game.envDamageTypes` `table` — Containing {def}IDs of environmental-damage sources
- <span id="Game.gameName"></span> `Game.gameName` `string`
- <span id="Game.gameShortName"></span> `Game.gameShortName` `string`
- <span id="Game.gameVersion"></span> `Game.gameVersion` `string`
- <span id="Game.gameMutator"></span> `Game.gameMutator` `string`
- <span id="Game.gameDesc"></span> `Game.gameDesc` `string`
- <span id="Game.requireSonarUnderWater"></span> `Game.requireSonarUnderWater` `boolean`
- <span id="Game.transportAir"></span> `Game.transportAir` `integer`
- <span id="Game.transportShip"></span> `Game.transportShip` `integer`
- <span id="Game.transportHover"></span> `Game.transportHover` `integer`
- <span id="Game.transportGround"></span> `Game.transportGround` `integer`
- <span id="Game.fireAtKilled"></span> `Game.fireAtKilled` `integer`
- <span id="Game.fireAtCrashing"></span> `Game.fireAtCrashing` `integer`
- <span id="Game.constructionDecay"></span> `Game.constructionDecay` `boolean`
- <span id="Game.reclaimAllowEnemies"></span> `Game.reclaimAllowEnemies` `boolean`
- <span id="Game.reclaimAllowAllies"></span> `Game.reclaimAllowAllies` `boolean`
- <span id="Game.constructionDecayTime"></span> `Game.constructionDecayTime` `integer`
- <span id="Game.constructionDecaySpeed"></span> `Game.constructionDecaySpeed` `number`
- <span id="Game.multiReclaim"></span> `Game.multiReclaim` `integer`
- <span id="Game.reclaimMethod"></span> `Game.reclaimMethod` `integer`
- <span id="Game.reclaimUnitMethod"></span> `Game.reclaimUnitMethod` `integer`
- <span id="Game.reclaimUnitEnergyCostFactor"></span> `Game.reclaimUnitEnergyCostFactor` `number`
- <span id="Game.reclaimUnitEfficiency"></span> `Game.reclaimUnitEfficiency` `number`
- <span id="Game.reclaimFeatureEnergyCostFactor"></span> `Game.reclaimFeatureEnergyCostFactor` `number`
- <span id="Game.repairEnergyCostFactor"></span> `Game.repairEnergyCostFactor` `number`
- <span id="Game.resurrectEnergyCostFactor"></span> `Game.resurrectEnergyCostFactor` `number`
- <span id="Game.captureEnergyCostFactor"></span> `Game.captureEnergyCostFactor` `number`
- <span id="Game.springCategories"></span> `Game.springCategories` `table<string,integer>` — ```lua
    example: {
      ["vtol"]         = 0,  ["special"]      = 1,  ["noweapon"]     = 2,
      ["notair"]       = 3,  ["notsub"]       = 4,  ["all"]          = 5,
      ["weapon"]       = 6,  ["notship"]      = 7,  ["notland"]      = 8,
      ["mobile"]       = 9,  ["kbot"]         = 10, ["antigator"]    = 11,
      ["tank"]         = 12, ["plant"]        = 13, ["ship"]         = 14,
      ["antiemg"]      = 15, ["antilaser"]    = 16, ["antiflame"]    = 17,
      ["underwater"]   = 18, ["hover"]        = 19, ["phib"]         = 20,
      ["constr"]       = 21, ["strategic"]    = 22, ["commander"]    = 23,
      ["paral"]        = 24, ["jam"]          = 25, ["mine"]         = 26,
      ["kamikaze"]     = 27, ["minelayer"]    = 28, ["notstructure"] = 29,
      ["air"]          = 30
    }
```
- <span id="Game.armorTypes"></span> `Game.armorTypes` `table<(string|integer),(integer|string)>` — (bidirectional)
```lua
    example: {
      [1]  = amphibious,   [2] = anniddm,     [3] = antibomber,
      [4]  = antifighter,  [5] = antiraider,  [6] = atl,
      [7]  = blackhydra,   [8] = bombers,     [9] = commanders,
      [10] = crawlingbombs, ...

      ["amphibious"]   = 1, ["anniddm"]    = 2, ["antibomber"] = 3
      ["antifighter"]  = 4, ["antiraider"] = 5, ["atl"]        = 6
      ["blackhydra"]   = 7, ["bombers"]    = 8, ["commanders"] = 9
      ["crawlingbombs"]= 10, ...
    }
```
- <span id="Game.textColorCodes"></span> `Game.textColorCodes` [`TextColorCode`](TextColorCode.md#TextColorCode) — Table containing keys that represent the color code operations during font rendering
- <span id="Game.nativeExcessSharing"></span> `Game.nativeExcessSharing` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstGame.cpp#L223-L223" target="_blank">source</a>]
whether the engine handles excess resources overflow
