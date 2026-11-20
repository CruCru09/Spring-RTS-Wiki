---
title: "FeatureSupport"
tags:
  - Lua-API
---

## FeatureSupport {#FeatureSupport}
*class*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstEngine.cpp#L16-L35" target="_blank">source</a>]

**Fields**

- <span id="FeatureSupport.NegativeGetUnitCurrentCommand"></span> `FeatureSupport.NegativeGetUnitCurrentCommand` `boolean` — Whether Spring.GetUnitCurrentCommand allows negative indices to look from the end
- <span id="FeatureSupport.hasExitOnlyYardmaps"></span> `FeatureSupport.hasExitOnlyYardmaps` `boolean` — Whether yardmaps accept 'e' (exit only) and 'u' (unbuildable, walkable)
- <span id="FeatureSupport.rmlUiApiVersion"></span> `FeatureSupport.rmlUiApiVersion` `integer` — Version of Recoil's rmlUI API
- <span id="FeatureSupport.noAutoShowMetal"></span> `FeatureSupport.noAutoShowMetal` `boolean` — Whether the engine switches to the metal view when selecting a "build metal extractor" command (yes if false)
- <span id="FeatureSupport.maxPiecesPerModel"></span> `FeatureSupport.maxPiecesPerModel` `integer` — How many pieces supported for 3d models?
- <span id="FeatureSupport.gunshipCruiseAltitudeMultiplier"></span> `FeatureSupport.gunshipCruiseAltitudeMultiplier` `number` — For gunships, the cruiseAltitude from the unit def is multiplied by this much
- <span id="FeatureSupport.noRefundForConstructionDecay"></span> `FeatureSupport.noRefundForConstructionDecay` `boolean` — Whether there is no refund for construction decay (100% metal back if false)
- <span id="FeatureSupport.noRefundForFactoryCancel"></span> `FeatureSupport.noRefundForFactoryCancel` `boolean` — Whether there is no refund for factory cancel (100% metal back if false)
- <span id="FeatureSupport.noOffsetForFeatureID"></span> `FeatureSupport.noOffsetForFeatureID` `boolean` — Whether featureID from various interfaces (targetID for Reclaim commands, ownerID from SpringGetGroundDecalOwner, etc) needs to be offset by [Game.maxUnits](Game.md#Game.maxUnits)
- <span id="FeatureSupport.noHandicapForReclaim"></span> `FeatureSupport.noHandicapForReclaim` `boolean` — Whether handicap is applied to income from reclaim
- <span id="FeatureSupport.groupAddDoesntSelect"></span> `FeatureSupport.groupAddDoesntSelect` `boolean` — Whether 'group add' also selects the group (does both if false)
- <span id="FeatureSupport.deadTeamsKeepUnitLimit"></span> `FeatureSupport.deadTeamsKeepUnitLimit` `boolean` — Whether engine redistributes dead team unitlimit to allies (false) or keeps it as-is (true)
- <span id="FeatureSupport.reliableLuaMapShaders"></span> `FeatureSupport.reliableLuaMapShaders` `boolean` — Whether forward-only Lua map shaders activate without a deferred draw and Spring.SetMapShader program swaps refresh cached uniform locations
- <span id="FeatureSupport.nanoParticleUpdateCallin"></span> `FeatureSupport.nanoParticleUpdateCallin` `boolean` — Whether LuaUI receives batched `NanoParticleUpdate` lifecycle events
- <span id="FeatureSupport.nanoParticlesGL4"></span> `FeatureSupport.nanoParticlesGL4` `boolean` — Whether the engine has the standalone shader-based nano particle effect (the `NanoParticles*` springsettings)
- <span id="FeatureSupport.modelVertexColor"></span> `FeatureSupport.modelVertexColor` `boolean` — Whether glTF `COLOR_0` is loaded into the models VBO (`color`, attribute 15; opaque white when absent)
