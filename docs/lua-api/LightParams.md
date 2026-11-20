---
title: "LightParams"
tags:
  - Lua-API
---

## LightParams {#LightParams}
*class*

Parameters for lighting

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaUnsyncedCtrl.cpp#L1630-L1657" target="_blank">source</a>]

**Fields**

- <span id="LightParams.position"></span> `LightParams.position` `{ px: number, py: number, pz: number }`
- <span id="LightParams.direction"></span> `LightParams.direction` `{ dx: number, dy: number, dz: number }`
- <span id="LightParams.ambientColor"></span> `LightParams.ambientColor` `{ blue: number, green: number, red: number }`
- <span id="LightParams.diffuseColor"></span> `LightParams.diffuseColor` `{ blue: number, green: number, red: number }`
- <span id="LightParams.specularColor"></span> `LightParams.specularColor` `{ blue: number, green: number, red: number }`
- <span id="LightParams.intensityWeight"></span> `LightParams.intensityWeight` `{ ambientWeight: number, diffuseWeight: number, specularWeight: number }`
- <span id="LightParams.ambientDecayRate"></span> `LightParams.ambientDecayRate` `{ ambientBlueDecay: number, ambientGreenDecay: number, ambientRedDecay: number }` — Per-frame decay of `ambientColor` (spread over TTL frames)
- <span id="LightParams.diffuseDecayRate"></span> `LightParams.diffuseDecayRate` `{ diffuseBlueDecay: number, diffuseGreenDecay: number, diffuseRedDecay: number }` — Per-frame decay of `diffuseColor` (spread over TTL frames)
- <span id="LightParams.specularDecayRate"></span> `LightParams.specularDecayRate` `{ specularBlueDecay: number, specularGreenDecay: number, specularRedDecay: number }` — Per-frame decay of `specularColor` (spread over TTL frames)
- <span id="LightParams.decayFunctionType"></span> `LightParams.decayFunctionType` `{ ambientDecayType: number, diffuseDecayType: number, specularDecayType: number }` — If value is `0.0` then the `*DecayRate` values will be interpreted as linear, otherwise exponential.
- <span id="LightParams.radius"></span> `LightParams.radius` `number`
- <span id="LightParams.fov"></span> `LightParams.fov` `number`
- <span id="LightParams.ttl"></span> `LightParams.ttl` `number`
- <span id="LightParams.priority"></span> `LightParams.priority` `number`
- <span id="LightParams.ignoreLOS"></span> `LightParams.ignoreLOS` `boolean`
