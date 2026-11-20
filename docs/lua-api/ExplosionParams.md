---
title: "ExplosionParams"
tags:
  - Lua-API
---

## ExplosionParams {#ExplosionParams}
*class*

Parameters for explosion.

Please note the explosion defaults to 1 damage regardless of what it's defined in the weaponDef.
The weapondefID is only used for visuals and for passing into callins like UnitDamaged.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L7592-L7612" target="_blank">source</a>]

**Fields**

- <span id="ExplosionParams.weaponDef"></span> `ExplosionParams.weaponDef` `WeaponDefID?`
- <span id="ExplosionParams.owner"></span> `ExplosionParams.owner` `UnitID?`
- <span id="ExplosionParams.hitUnit"></span> `ExplosionParams.hitUnit` `UnitID?`
- <span id="ExplosionParams.hitFeature"></span> `ExplosionParams.hitFeature` `FeatureID?`
- <span id="ExplosionParams.craterAreaOfEffect"></span> `ExplosionParams.craterAreaOfEffect` `number?`
- <span id="ExplosionParams.damageAreaOfEffect"></span> `ExplosionParams.damageAreaOfEffect` `number?`
- <span id="ExplosionParams.edgeEffectiveness"></span> `ExplosionParams.edgeEffectiveness` `number?`
- <span id="ExplosionParams.explosionSpeed"></span> `ExplosionParams.explosionSpeed` `number?`
- <span id="ExplosionParams.gfxMod"></span> `ExplosionParams.gfxMod` `number?`
- <span id="ExplosionParams.impactOnly"></span> `ExplosionParams.impactOnly` `boolean?`
- <span id="ExplosionParams.ignoreOwner"></span> `ExplosionParams.ignoreOwner` `boolean?`
- <span id="ExplosionParams.damageGround"></span> `ExplosionParams.damageGround` `boolean?`
