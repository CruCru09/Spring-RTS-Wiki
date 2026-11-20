---
title: "Engine"
tags:
  - Lua-API
---

## Engine {#Engine}
*table*

Engine specific information.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstEngine.cpp#L37-L52" target="_blank">source</a>]

**Fields**

- <span id="Engine.version"></span> `Engine.version` `string` — "Major.Minor.PatchSet" for releases, "Major.Minor.PatchSet-CommitNum-gHash branch" otherwise
- <span id="Engine.versionFull"></span> `Engine.versionFull` `string` — "Major.Minor.PatchSet" for releases, "Major.Minor.PatchSet-CommitNum-gHash branch" otherwise. Will also include (buildFlags), if there're any.
- <span id="Engine.versionMajor"></span> `Engine.versionMajor` `string` — Major part of the named release version
- <span id="Engine.versionMinor"></span> `Engine.versionMinor` `string` — Minor part of the named release version
- <span id="Engine.versionPatchSet"></span> `Engine.versionPatchSet` `string` — Build number of the named release version
- <span id="Engine.commitsNumber"></span> `Engine.commitsNumber` `string` — Number of commits after the latest named release, non-zero indicates a "dev" build
- <span id="Engine.buildFlags"></span> `Engine.buildFlags` `string` — Gets additional engine buildflags, e.g. "Debug" or "Sync-Debug"
- <span id="Engine.featureSupport"></span> `Engine.featureSupport` [`FeatureSupport`](FeatureSupport.md#FeatureSupport) — Table containing various engine features as keys; use for cross-version compat
- <span id="Engine.wordSize"></span> `Engine.wordSize` `integer` — Indicates the build type always 64 these days
- <span id="Engine.gameSpeed"></span> `Engine.gameSpeed` `integer` — Number of simulation gameframes per second
- <span id="Engine.textColorCodes"></span> `Engine.textColorCodes` [`TextColorCode`](TextColorCode.md#TextColorCode) — Table containing keys that represent the color code operations during font rendering
