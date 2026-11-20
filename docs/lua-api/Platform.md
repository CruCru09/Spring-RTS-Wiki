---
title: "Platform"
tags:
  - Lua-API
---

## Platform {#Platform}
*table*

Platform specific information

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L16-L19" target="_blank">source</a>]

**Fields**

- <span id="Platform.gpu"></span> `Platform.gpu` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L23-L23" target="_blank">source</a>]
Full GPU device name
- <span id="Platform.gpuVendor"></span> `Platform.gpuVendor` `("Nvidia"|"Intel"|"ATI"|"Mesa"|"Unknown")` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L25-L25" target="_blank">source</a>]
- <span id="Platform.gpuMemorySize"></span> `Platform.gpuMemorySize` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L27-L27" target="_blank">source</a>]
Size of total GPU memory in MBs; only available for "Nvidia", (rest are 0)
- <span id="Platform.glVersionShort"></span> `Platform.glVersionShort` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L29-L29" target="_blank">source</a>]
`major.minor.buildNumber`
- <span id="Platform.glVersionNum"></span> `Platform.glVersionNum` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L31-L31" target="_blank">source</a>]
- <span id="Platform.glslVersionShort"></span> `Platform.glslVersionShort` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L33-L33" target="_blank">source</a>]
`major.minor`
- <span id="Platform.glslVersionNum"></span> `Platform.glslVersionNum` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L35-L35" target="_blank">source</a>]
- <span id="Platform.glVersion"></span> `Platform.glVersion` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L38-L38" target="_blank">source</a>]
Full version
- <span id="Platform.glVendor"></span> `Platform.glVendor` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L40-L40" target="_blank">source</a>]
- <span id="Platform.glRenderer"></span> `Platform.glRenderer` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L42-L42" target="_blank">source</a>]
- <span id="Platform.glslVersion"></span> `Platform.glslVersion` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L44-L44" target="_blank">source</a>]
Full version
- <span id="Platform.gladVersion"></span> `Platform.gladVersion` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L46-L46" target="_blank">source</a>]
- <span id="Platform.glewVersion"></span> `Platform.glewVersion` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L48-L48" target="_blank">source</a>]
- <span id="Platform.sdlVersionCompiledMajor"></span> `Platform.sdlVersionCompiledMajor` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L51-L51" target="_blank">source</a>]
- <span id="Platform.sdlVersionCompiledMinor"></span> `Platform.sdlVersionCompiledMinor` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L53-L53" target="_blank">source</a>]
- <span id="Platform.sdlVersionCompiledPatch"></span> `Platform.sdlVersionCompiledPatch` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L55-L55" target="_blank">source</a>]
- <span id="Platform.sdlVersionLinkedMajor"></span> `Platform.sdlVersionLinkedMajor` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L57-L57" target="_blank">source</a>]
- <span id="Platform.sdlVersionLinkedMinor"></span> `Platform.sdlVersionLinkedMinor` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L59-L59" target="_blank">source</a>]
- <span id="Platform.sdlVersionLinkedPatch"></span> `Platform.sdlVersionLinkedPatch` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L61-L61" target="_blank">source</a>]
- <span id="Platform.availableVideoModes"></span> `Platform.availableVideoModes` `PlatformVideoMode[]` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L64-L64" target="_blank">source</a>]
- <span id="Platform.numDisplays"></span> `Platform.numDisplays` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L93-L93" target="_blank">source</a>]
- <span id="Platform.glSupportNonPowerOfTwoTex"></span> `Platform.glSupportNonPowerOfTwoTex` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L96-L96" target="_blank">source</a>]
- <span id="Platform.glSupportTextureQueryLOD"></span> `Platform.glSupportTextureQueryLOD` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L98-L98" target="_blank">source</a>]
- <span id="Platform.glSupportMSAAFrameBuffer"></span> `Platform.glSupportMSAAFrameBuffer` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L100-L100" target="_blank">source</a>]
- <span id="Platform.glHaveAMD"></span> `Platform.glHaveAMD` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L103-L103" target="_blank">source</a>]
- <span id="Platform.glHaveNVidia"></span> `Platform.glHaveNVidia` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L105-L105" target="_blank">source</a>]
- <span id="Platform.glHaveIntel"></span> `Platform.glHaveIntel` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L107-L107" target="_blank">source</a>]
- <span id="Platform.glHaveGLSL"></span> `Platform.glHaveGLSL` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L110-L110" target="_blank">source</a>]
- <span id="Platform.glHaveGL4"></span> `Platform.glHaveGL4` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L112-L112" target="_blank">source</a>]
- <span id="Platform.glSupportDepthBufferBitDepth"></span> `Platform.glSupportDepthBufferBitDepth` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L115-L115" target="_blank">source</a>]
- <span id="Platform.glSupportRestartPrimitive"></span> `Platform.glSupportRestartPrimitive` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L118-L118" target="_blank">source</a>]
- <span id="Platform.glSupportClipSpaceControl"></span> `Platform.glSupportClipSpaceControl` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L120-L120" target="_blank">source</a>]
- <span id="Platform.glSupportFragDepthLayout"></span> `Platform.glSupportFragDepthLayout` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L122-L122" target="_blank">source</a>]
- <span id="Platform.glSupportSeamlessCubeMaps"></span> `Platform.glSupportSeamlessCubeMaps` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L124-L124" target="_blank">source</a>]
- <span id="Platform.osName"></span> `Platform.osName` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L127-L127" target="_blank">source</a>]
full name of the OS
- <span id="Platform.osVersion"></span> `Platform.osVersion` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L129-L129" target="_blank">source</a>]
- <span id="Platform.osFamily"></span> `Platform.osFamily` `("Windows"|"Linux"|"MacOSX"|"FreeBSD"|"Unknown")` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L131-L131" target="_blank">source</a>]
- <span id="Platform.architecture"></span> `Platform.architecture` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L133-L133" target="_blank">source</a>]
CPU architecture (e.g., "x86_64", "arm64")
- <span id="Platform.hwConfig"></span> `Platform.hwConfig` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L135-L135" target="_blank">source</a>]
- <span id="Platform.cpuLogicalCores"></span> `Platform.cpuLogicalCores` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L137-L137" target="_blank">source</a>]
- <span id="Platform.cpuPhysicalCores"></span> `Platform.cpuPhysicalCores` `integer` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L139-L139" target="_blank">source</a>]
- <span id="Platform.cpuBrand"></span> `Platform.cpuBrand` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L141-L141" target="_blank">source</a>]
- <span id="Platform.totalRAM"></span> `Platform.totalRAM` `number` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L143-L143" target="_blank">source</a>]
Total physical system RAM in MBs.
- <span id="Platform.sysInfoHash"></span> `Platform.sysInfoHash` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L146-L146" target="_blank">source</a>]
- <span id="Platform.macAddrHash"></span> `Platform.macAddrHash` `string` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L148-L148" target="_blank">source</a>]
- <span id="Platform.isHeadless"></span> `Platform.isHeadless` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L151-L151" target="_blank">source</a>]
Is this a headless build which only simulates and doesnt offer interactive IO?
- <span id="Platform.hasSyncChecksums"></span> `Platform.hasSyncChecksums` `boolean` — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaConstPlatform.cpp#L154-L154" target="_blank">source</a>]
Whether the engine was built with sync-check support (i.e. Spring.GetPrevFrameSyncChecksum() returns a meaningful value).
