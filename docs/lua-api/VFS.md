---
title: "VFS"
tags:
  - Lua-API
---

## VFS {#VFS}
*table*

Unified IO for archive and filesystem

The Virtual File System is a unified layer to access (read-only) the
different archives used at runtime. So you can access map, game & config
files via the same interface.

#### Overview

Although Spring can access the filesystem directly (via os module) it is
more common that you would want to access files included with your game or
Spring. Trouble is, most of these files are compressed into archives
(`.sdz`/`.sd7`) so random access would generally be a difficult procedure.
Fortunately, the Spring Lua system automatically provides access to mod and
base files via the VFS module.

As an additional caveat, synced Lua cannot use the `os` and `io` modules,
so using VFS is mandatory there to have any file access at all.

The VFS module doesn't simply open archives though. What it does is map
your game files, game dependencies and Spring content onto a virtual file
tree. All archives start from the 'roots' of the tree and share the same
virtual space, meaning that if two or more archives contain the same
resource file name the resources overlap and only one of the files will be
retrieved. Overlapping directories on the other hand are merged so the
resulting virtual directory contains the contents of both. Here is an
example of how this works:

**Archive 1** (`games/mygame.sd7`)

```
textures
└── texture1.png
models
└── model1.mdl
```

**Archive 2** (`base/springcontent.sdz`)

```
textures
├── texture1.png
├── texture2.png
└── texture3.png
```

**VFS**

```
textures
├── texture1.png
├── texture2.png
└── texture3.png
models
└── model1.mdl
```

This raises the question: If both archives have a `texture1.png` then which
`texture1.png` is retreived via the VFS? The answer depends on the order the
archives are loaded and the VFS mode (more on modes below). Generally
however, each archive loaded overrides any archives loaded before it. The
standard order of loading (from first to last) is:

1. The automatic dependencies `springcontent.sdz` and `maphelper.sdz`.
2. Dependencies listed in your `modinfo.lua` (or `modinfo.tdf`), in the order listed.
Note that they are loaded fully and recursively, i.e. all the deeper dependencies of the 1st base-level dependency are
loaded before the 2nd base-level dependency. This breaks the usual "loaded later overrides loaded earlier" priority if
a dependency comes from multiple places, since only the first time an archive is loaded counts.
3. Your mod archive.

Loose files (not within any archive) in the engine dir are also visible
as if under the VFS root if loading under the [VFS.RAW](VFS.md#VFS.RAW) mode, though you
can also use full FS path (i.e. `C:/.../Spring/foo/bar.txt` is visible
both as that and as just `foo/bar.txt`). Note that [VFS.RAW](VFS.md#VFS.RAW) is only
accessible to unsynced Lua, all synced states are limited to loaded archives.

#### Paths

Spring's VFS is **lowercase only**. Also it is **strongly** recommended to
use linux style path separators, e.g. `"foo/bar.txt"` and not `"foo\bar.txt"`.

#### Engine read files

The engine access a few files directly, most of them are lua files which
access other files themselves. Here the list of files that must exist in the
VFS (some of them don't have to be in the game/map archive cause there are
fallback solutions in `springcontent.sdz` & `maphelper.sdz`):

- `./`
- anims/
- `cursornormal.bmp/png`
- gamedata/
- `defs.lua`
- `explosions.lua`
- `explosion_alias.lua`
- `icontypes.lua`
- `messages.lua`
- `modrules.lua`
- `resources.lua`
- `resources_map.lua`
- `sidedata.lua`
- `sounds.lua`
- `luagaia/`
- `main.lua`
- `draw.lua`
- `luarules/`
- `main.lua`
- `draw.lua`
- `luaui/`
- `main.lua`
- `shaders/`
- `?`
- `luaai.lua`
- `mapinfo.lua`
- `mapoptions.lua`
- `modinfo.lua`
- `modoptions.lua`
- `validmaps.lua`

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L27-L146" target="_blank">source</a>]

**Members**

### VFS.GetMaps {#VFS.GetMaps}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L52-L55" target="_blank">source</a>]

```lua
VFS.GetMaps() -> string[]
```

**Returns**

- `mapNames` `string[]`

### VFS.GetGames {#VFS.GetGames}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L63-L66" target="_blank">source</a>]

```lua
VFS.GetGames() -> string[]
```

**Returns**

- `gameNames` `string[]`

### VFS.GetAllArchives {#VFS.GetAllArchives}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L82-L85" target="_blank">source</a>]

```lua
VFS.GetAllArchives() -> string[]
```

**Returns**

- `archiveNames` `string[]`

### VFS.HasArchive {#VFS.HasArchive}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L101-L104" target="_blank">source</a>]

```lua
VFS.HasArchive() -> boolean
```

**Returns**

- `hasArchive` `boolean`

### VFS.GetLoadedArchives {#VFS.GetLoadedArchives}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L115-L118" target="_blank">source</a>]

```lua
VFS.GetLoadedArchives() -> string[]
```

**Returns**

- `archiveNames` `string[]`

### VFS.GetArchivePath {#VFS.GetArchivePath}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L129-L133" target="_blank">source</a>]

```lua
VFS.GetArchivePath(string) -> string?
```

**Parameters**

- `archiveName` `string`

**Returns**

- `archivePath` `string?`

### VFS.GetArchiveInfo {#VFS.GetArchiveInfo}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L170-L174" target="_blank">source</a>]

```lua
VFS.GetArchiveInfo(string) -> ArchiveInfo?
```

**Parameters**

- `archiveName` `string`

**Returns**

- `archiveInfo` `ArchiveInfo?`

### VFS.GetArchiveDependencies {#VFS.GetArchiveDependencies}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L215-L219" target="_blank">source</a>]

```lua
VFS.GetArchiveDependencies(string) -> string[]
```

**Parameters**

- `archiveName` `string`

**Returns**

- `archiveNames` `string[]`

### VFS.GetArchiveReplaces {#VFS.GetArchiveReplaces}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L233-L237" target="_blank">source</a>]

```lua
VFS.GetArchiveReplaces(string) -> string[]
```

**Parameters**

- `archiveName` `string`

**Returns**

- `archiveNames` `string[]`

### VFS.GetArchiveChecksum {#VFS.GetArchiveChecksum}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L255-L260" target="_blank">source</a>]

```lua
VFS.GetArchiveChecksum(string) -> string, string
```

**Parameters**

- `archiveName` `string`

**Returns**

- `singleArchiveChecksum` `string`
- `completeArchiveChecksum` `string`

### VFS.GetNameFromRapidTag {#VFS.GetNameFromRapidTag}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L280-L284" target="_blank">source</a>]

```lua
VFS.GetNameFromRapidTag(string) -> string
```

**Parameters**

- `rapidTag` `string`

**Returns**

- `archiveName` `string`

### VFS.GetAvailableAIs {#VFS.GetAvailableAIs}
*function*

Get a list of all Spring AIs.

The optional gameName and mapName parameters can be used to include game/map
specific LuaAIs in the list.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaArchive.cpp#L308-L317" target="_blank">source</a>]

```lua
VFS.GetAvailableAIs(string?, string?) -> AIInfo[]
```

**Parameters**

- `gameArchiveName` `string?`
- `mapArichiveName` `string?`

**Returns**

- `ais` `AIInfo[]`

### VFS.Include {#VFS.Include}
*function*

Loads and runs lua code from a file in the VFS.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L277-L311" target="_blank">source</a>]

The path is relative to the main Spring directory, e.g.

```lua
VFS.Include('LuaUI/includes/filename.lua', nil, vfsmode)
```

```lua
VFS.Include(string, table?, string?) -> any
```

**Parameters**

- `filename` `string`
- `environment` `table?` — (Default: the current function environment)

The environment arg sets the global environment (see generic lua refs). In
almost all cases, this should be left `nil` to preserve the current env.

If the provided, any non-local variables and functions defined in
`filename.lua` are then accessable via env. Vise-versa, any variables
defined in env prior to passing to [VFS.Include](VFS.md#VFS.Include) are available to code in the
included file. Code running in `filename.lua` will see the contents of env in
place of the normal global environment.
- `mode` `string?`

**Returns**

- `module` `any` — The return value of the included file.

### VFS.LoadFile {#VFS.LoadFile}
*function*

Load raw text data from the VFS.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L395-L415" target="_blank">source</a>]

Returns file contents as a string. Unlike [VFS.Include](VFS.md#VFS.Include) the file will not be
executed. This lets you pre-process the code. Use `loadstring` afterwards.

```lua
VFS.LoadFile(string, string?) -> string?
```

**Parameters**

- `filename` `string`
- `mode` `string?`

**Returns**

- `data` `string?` — The contents of the file.

### VFS.FileExists {#VFS.FileExists}
*function*

Check if file exists in VFS.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L446-L471" target="_blank">source</a>]

Example usage:

```lua
if VFS.FileExists("mapconfig/custom_lava_config.lua", VFS.MAP) then
  # ...
end
```

```lua
VFS.FileExists(string, string?) -> boolean
```

**Parameters**

- `filename` `string`
- `mode` `string?`

**Returns**

- `exists` `boolean` — `true` if the file exists, otherwise `false`.

### VFS.DirList {#VFS.DirList}
*function*

List files in a directory.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L492-L519" target="_blank">source</a>]

Example usage:

```lua
local luaFiles = VFS.DirList('units/', '*.lua', nil, true)
```

```lua
VFS.DirList(string, string?, string?, boolean?) -> string[]
```

**Parameters**

- `directory` `string`
- `pattern` `string?` — (Default: `"*"`)
- `mode` `string?`
- `recursive` `boolean?` — (Default: `false`)

**Returns**

- `filenames` `string[]`

### VFS.SubDirs {#VFS.SubDirs}
*function*

List sub-directories in a directory.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L551-L581" target="_blank">source</a>]

Example usage:

```lua
local files = VFS.SubDirs('sounds/voice/' .. language, '*')
for _, file in ipairs(files) do
    # ...
end
```

```lua
VFS.SubDirs(string, string?, string?, boolean?) -> string[]
```

**Parameters**

- `directory` `string`
- `pattern` `string?` — (Default: `"*"`)
- `mode` `string?`
- `recursive` `boolean?` — (Default: `false`)

**Returns**

- `dirnames` `string[]`

### VFS.GetFileAbsolutePath {#VFS.GetFileAbsolutePath}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L609-L624" target="_blank">source</a>]

```lua
VFS.GetFileAbsolutePath(string, string?) -> string?
```

**Parameters**

- `filename` `string`
- `mode` `string?`

**Returns**

- `absolutePath` `string?`

### VFS.GetArchiveContainingFile {#VFS.GetArchiveContainingFile}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L648-L663" target="_blank">source</a>]

```lua
VFS.GetArchiveContainingFile(string, string?) -> string?
```

**Parameters**

- `filename` `string`
- `mode` `string?`

**Returns**

- `archiveName` `string?`

### VFS.UseArchive {#VFS.UseArchive}
*function*

Temporarily load an archive from the VFS and run the given function,
which can make usage of the files in the archive.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L688-L696" target="_blank">source</a>]

```lua
VFS.UseArchive(string, unknown) -> any ...
```

**Parameters**

- `archiveName` `string`
- `fun` `unknown`

**Returns**

- `Results` `any ...` — of the given function

### VFS.CompressFolder {#VFS.CompressFolder}
*function*

Compresses the specified folder.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L816-L826" target="_blank">source</a>]

```lua
VFS.CompressFolder(string, string?, string?, boolean?, string?) -> nil
```

**Parameters**

- `folderPath` `string`
- `archiveType` `string?` — (Default: `"zip"`)The compression type (can
currently be only `"zip"`).
- `compressedFilePath` `string?` — (Default: `folderPath .. ".sdz"`)
- `includeFolder` `boolean?` — (Default: `false`) Whether the archive should
have the specified folder as root.
- `mode` `string?`

### VFS.ZlibCompress {#VFS.ZlibCompress}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L862-L866" target="_blank">source</a>]

```lua
VFS.ZlibCompress(string) -> string?
```

**Parameters**

- `uncompressed` `string` — Data to compress.

**Returns**

- `compressed` `string?` — Compressed data, or `nil` on error.

### VFS.ZlibDecompress {#VFS.ZlibDecompress}
*function*

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L882-L886" target="_blank">source</a>]

```lua
VFS.ZlibDecompress(string) -> string?
```

**Parameters**

- `compressed` `string` — Data to decompress.

**Returns**

- `uncompressed` `string?` — Uncompressed data, or `nil` on error.

### VFS.CalculateHash {#VFS.CalculateHash}
*function*

Calculates hash of a given string.

- MD5 gets base64 encoded.
- SHA512 gets hex encoded.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L909-L919" target="_blank">source</a>]

```lua
VFS.CalculateHash(string, HashType) -> string?
```

**Parameters**

- `input` `string`
- `hashType` [`HashType`](Aliases.md#HashType) — Hash type.

**Returns**

- `hash` `string?`

### VFS.PackU8 {#VFS.PackU8}
*function*

Convert unsigned 8-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1001-L1006" target="_blank">source</a>]

```lua
VFS.PackU8([integer, ]*) -> string
```

**Parameters**

- `...` `integer` — Numbers to pack.

**Returns**

- `string`

### VFS.PackU8 (overload 1) {#VFS.PackU8-1}
*function*

Convert unsigned 8-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1007-L1012" target="_blank">source</a>]

```lua
VFS.PackU8(integer[]) -> string
```

**Parameters**

- `numbers` `integer[]` — Numbers to pack.

**Returns**

- `string`

### VFS.PackU16 {#VFS.PackU16}
*function*

Convert unsigned 16-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1015-L1020" target="_blank">source</a>]

```lua
VFS.PackU16([integer, ]*) -> string
```

**Parameters**

- `...` `integer` — Numbers to pack.

**Returns**

- `string`

### VFS.PackU16 (overload 1) {#VFS.PackU16-1}
*function*

Convert unsigned 16-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1021-L1026" target="_blank">source</a>]

```lua
VFS.PackU16(integer[]) -> string
```

**Parameters**

- `numbers` `integer[]` — Numbers to pack.

**Returns**

- `string`

### VFS.PackU32 {#VFS.PackU32}
*function*

Convert unsigned 32-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1029-L1034" target="_blank">source</a>]

```lua
VFS.PackU32([integer, ]*) -> string
```

**Parameters**

- `...` `integer` — Numbers to pack.

**Returns**

- `string`

### VFS.PackU32 (overload 1) {#VFS.PackU32-1}
*function*

Convert unsigned 32-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1035-L1040" target="_blank">source</a>]

```lua
VFS.PackU32(integer[]) -> string
```

**Parameters**

- `numbers` `integer[]` — Numbers to pack.

**Returns**

- `string`

### VFS.PackS8 {#VFS.PackS8}
*function*

Convert signed 8-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1043-L1048" target="_blank">source</a>]

```lua
VFS.PackS8([integer, ]*) -> string
```

**Parameters**

- `...` `integer` — Numbers to pack.

**Returns**

- `string`

### VFS.PackS8 (overload 1) {#VFS.PackS8-1}
*function*

Convert signed 8-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1049-L1054" target="_blank">source</a>]

```lua
VFS.PackS8(integer[]) -> string
```

**Parameters**

- `numbers` `integer[]` — Numbers to pack.

**Returns**

- `string`

### VFS.PackS16 {#VFS.PackS16}
*function*

Convert signed 16-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1057-L1062" target="_blank">source</a>]

```lua
VFS.PackS16([integer, ]*) -> string
```

**Parameters**

- `...` `integer` — Numbers to pack.

**Returns**

- `string`

### VFS.PackS16 (overload 1) {#VFS.PackS16-1}
*function*

Convert signed 16-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1063-L1068" target="_blank">source</a>]

```lua
VFS.PackS16(integer[]) -> string
```

**Parameters**

- `numbers` `integer[]` — Numbers to pack.

**Returns**

- `string`

### VFS.PackS32 {#VFS.PackS32}
*function*

Convert signed 32-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1071-L1076" target="_blank">source</a>]

```lua
VFS.PackS32([integer, ]*) -> string
```

**Parameters**

- `...` `integer` — Numbers to pack.

**Returns**

- `string`

### VFS.PackS32 (overload 1) {#VFS.PackS32-1}
*function*

Convert signed 32-bit integer(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1077-L1082" target="_blank">source</a>]

```lua
VFS.PackS32(integer[]) -> string
```

**Parameters**

- `numbers` `integer[]` — Numbers to pack.

**Returns**

- `string`

### VFS.PackF32 {#VFS.PackF32}
*function*

Convert signed 32-bit float(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1085-L1090" target="_blank">source</a>]

```lua
VFS.PackF32([number, ]*) -> string?
```

**Parameters**

- `...` `number` — Numbers to pack.

**Returns**

- `string?`

### VFS.PackF32 (overload 1) {#VFS.PackF32-1}
*function*

Convert signed 32-bit float(s) to binary string.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1091-L1096" target="_blank">source</a>]

```lua
VFS.PackF32(number[]) -> string?
```

**Parameters**

- `numbers` `number[]` — Numbers to pack.

**Returns**

- `string?`

### VFS.UnpackU8 {#VFS.UnpackU8}
*function*

Convert a binary string to an unsigned 8-bit integer.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1144-L1150" target="_blank">source</a>]

```lua
VFS.UnpackU8(string, integer?) -> integer
```

**Parameters**

- `str` `string` — Binary string.
- `pos` `integer?` — Byte offset.

**Returns**

- `integer`

### VFS.UnpackU16 {#VFS.UnpackU16}
*function*

Convert a binary string to an unsigned 16-bit integer.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1153-L1159" target="_blank">source</a>]

```lua
VFS.UnpackU16(string, integer?) -> integer
```

**Parameters**

- `str` `string` — Binary string.
- `pos` `integer?` — Byte offset.

**Returns**

- `integer`

### VFS.UnpackU32 {#VFS.UnpackU32}
*function*

Convert a binary string to an unsigned 32-bit integer.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1162-L1168" target="_blank">source</a>]

```lua
VFS.UnpackU32(string, integer?) -> integer
```

**Parameters**

- `str` `string` — Binary string.
- `pos` `integer?` — Byte offset.

**Returns**

- `integer`

### VFS.UnpackS8 {#VFS.UnpackS8}
*function*

Convert a binary string to a signed 8-bit integer.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1171-L1177" target="_blank">source</a>]

```lua
VFS.UnpackS8(string, integer?) -> integer
```

**Parameters**

- `str` `string` — Binary string.
- `pos` `integer?` — Byte offset.

**Returns**

- `integer`

### VFS.UnpackS16 {#VFS.UnpackS16}
*function*

Convert a binary string to a signed 16-bit integer.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1180-L1186" target="_blank">source</a>]

```lua
VFS.UnpackS16(string, integer?) -> integer
```

**Parameters**

- `str` `string` — Binary string.
- `pos` `integer?` — Byte offset.

**Returns**

- `integer`

### VFS.UnpackS32 {#VFS.UnpackS32}
*function*

Convert a binary string to a signed 32-bit integer.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1189-L1195" target="_blank">source</a>]

```lua
VFS.UnpackS32(string, integer?) -> integer
```

**Parameters**

- `str` `string` — Binary string.
- `pos` `integer?` — Byte offset.

**Returns**

- `integer`

### VFS.UnpackF32 {#VFS.UnpackF32}
*function*

Convert a binary string to a signed 32-bit float.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L1198-L1204" target="_blank">source</a>]

```lua
VFS.UnpackF32(string, integer?) -> integer
```

**Parameters**

- `str` `string` — Binary string.
- `pos` `integer?` — Byte offset.

**Returns**

- `integer`

### VFS.DownloadArchive {#VFS.DownloadArchive}
*function*

Queue an archive download through pr-downloader.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFSDownload.cpp#L315-L320" target="_blank">source</a>]

```lua
VFS.DownloadArchive(string, string) -> nil
```

**Parameters**

- `filename` `string` — Archive or rapid package name.
- `category` `string` — One of `map`, `game`, or `engine`.

### VFS.AbortDownload {#VFS.AbortDownload}
*function*

Abort a queued or active archive download.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFSDownload.cpp#L346-L351" target="_blank">source</a>]

```lua
VFS.AbortDownload(integer) -> boolean
```

**Parameters**

- `id` `integer` — Download queue identifier.

**Returns**

- `removed` `boolean` — Whether a matching queued or active download was removed.

### VFS.ScanAllDirs {#VFS.ScanAllDirs}
*function*

Rescan all data directories for newly added archives.

[<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFSDownload.cpp#L358-L361" target="_blank">source</a>]

```lua
VFS.ScanAllDirs() -> nil
```

**Fields**

- <span id="VFS.RAW"></span> `VFS.RAW` "r" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L151-L151" target="_blank">source</a>]
Only select uncompressed files.
- <span id="VFS.GAME"></span> `VFS.GAME` "M" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L153-L153" target="_blank">source</a>]
- <span id="VFS.MAP"></span> `VFS.MAP` "m" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L155-L155" target="_blank">source</a>]
- <span id="VFS.BASE"></span> `VFS.BASE` "b" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L157-L157" target="_blank">source</a>]
- <span id="VFS.MENU"></span> `VFS.MENU` "e" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L159-L159" target="_blank">source</a>]
- <span id="VFS.ZIP"></span> `VFS.ZIP` "Mmeb" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L161-L161" target="_blank">source</a>]
Only select compressed files (`.sdz`, `.sd7`).
- <span id="VFS.RAW_FIRST"></span> `VFS.RAW_FIRST` "rMmeb" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L163-L163" target="_blank">source</a>]
Try uncompressed files first, then compressed.
- <span id="VFS.ZIP_FIRST"></span> `VFS.ZIP_FIRST` "Mmebr" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L165-L165" target="_blank">source</a>]
Try compressed files first, then uncompressed.
- <span id="VFS.MOD"></span> `VFS.MOD` "M" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L168-L171" target="_blank">source</a>]
- <span id="VFS.RAW_ONLY"></span> `VFS.RAW_ONLY` "r" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L173-L176" target="_blank">source</a>]
- <span id="VFS.ZIP_ONLY"></span> `VFS.ZIP_ONLY` "Mmeb" — [<a href="https://github.com/beyond-all-reason/RecoilEngine/blob/8688dcc2690a8db4e6624dd516ef5da8cf3c5ec8/rts/Lua/LuaVFS.cpp#L178-L181" target="_blank">source</a>]
