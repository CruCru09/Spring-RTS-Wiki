---
title: "WeaponState"
tags:
  - Lua-API
---

## WeaponState {#WeaponState}
*class*

Parameter for weapon states

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaSyncedCtrl.cpp#L2461-L2485" target="_blank">source</a>]

**Fields**

- <span id="WeaponState.reloadState"></span> `WeaponState.reloadState` `integer?`
- <span id="WeaponState.reloadFrame"></span> `WeaponState.reloadFrame` `integer?` — Alias for `reloadState`.
- <span id="WeaponState.reloadTime"></span> `WeaponState.reloadTime` `number?`
- <span id="WeaponState.reaimTime"></span> `WeaponState.reaimTime` `integer?`
- <span id="WeaponState.accuracy"></span> `WeaponState.accuracy` `number?`
- <span id="WeaponState.sprayAngle"></span> `WeaponState.sprayAngle` `number?`
- <span id="WeaponState.range"></span> `WeaponState.range` `number?` — If you change the range of a weapon with dynamic damage make sure you use `SetUnitWeaponDamages` to change dynDamageRange as well.
- <span id="WeaponState.projectileSpeed"></span> `WeaponState.projectileSpeed` `number?`
- <span id="WeaponState.burst"></span> `WeaponState.burst` `integer?`
- <span id="WeaponState.burstRate"></span> `WeaponState.burstRate` `number?`
- <span id="WeaponState.projectiles"></span> `WeaponState.projectiles` `integer?`
- <span id="WeaponState.salvoLeft"></span> `WeaponState.salvoLeft` `integer?`
- <span id="WeaponState.nextSalvo"></span> `WeaponState.nextSalvo` `integer?`
- <span id="WeaponState.aimReady"></span> `WeaponState.aimReady` `number?` — Set to `true` if a non-zero value is passed, `false` is zero is passed.
- <span id="WeaponState.forceAim"></span> `WeaponState.forceAim` `integer?`
- <span id="WeaponState.avoidFlags"></span> `WeaponState.avoidFlags` `integer?`
- <span id="WeaponState.collisionFlags"></span> `WeaponState.collisionFlags` `integer?`
- <span id="WeaponState.ttl"></span> `WeaponState.ttl` `number?` — How many seconds the projectile should live
