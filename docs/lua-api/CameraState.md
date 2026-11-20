---
title: "CameraState"
tags:
  - Lua-API
---

## CameraState {#CameraState}
*class*

Parameters for camera state.

Highly dependent on the type of the current camera controller.

**Fields**

- <span id="CameraState.name"></span> `CameraState.name` [`CameraName`](Aliases.md#CameraName) — The camera name.
- <span id="CameraState.mode"></span> `CameraState.mode` [`CameraMode`](Aliases.md#CameraMode) — The camera mode.
- <span id="CameraState.fov"></span> `CameraState.fov` `number?`
- <span id="CameraState.px"></span> `CameraState.px` `number?` — Position X of the ground point in screen center.
- <span id="CameraState.py"></span> `CameraState.py` `number?` — Position Y of the ground point in screen center.
- <span id="CameraState.pz"></span> `CameraState.pz` `number?` — Position Z of the ground point in screen center.
- <span id="CameraState.dx"></span> `CameraState.dx` `number?` — Camera direction vector X.
- <span id="CameraState.dy"></span> `CameraState.dy` `number?` — Camera direction vector Y.
- <span id="CameraState.dz"></span> `CameraState.dz` `number?` — Camera direction vector Z.
- <span id="CameraState.rx"></span> `CameraState.rx` `number?` — Camera rotation angle on X axis. (spring)
- <span id="CameraState.ry"></span> `CameraState.ry` `number?` — Camera rotation angle on Y axis. (spring)
- <span id="CameraState.rz"></span> `CameraState.rz` `number?` — Camera rotation angle on Z axis. (spring)
- <span id="CameraState.angle"></span> `CameraState.angle` `number?` — Camera rotation angle on X axis (aka tilt/pitch). (ta)
- <span id="CameraState.flipped"></span> `CameraState.flipped` `number?` — `-1` for when south is down, `1` for when north is down. (ta)
- <span id="CameraState.dist"></span> `CameraState.dist` `number?` — Camera distance from the ground. (spring)
- <span id="CameraState.height"></span> `CameraState.height` `number?` — Camera distance from the ground. (ta)
- <span id="CameraState.oldHeight"></span> `CameraState.oldHeight` `number?` — Camera distance from the ground, cannot be changed. (rot)
