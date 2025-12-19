---
sidebar_position: 1
title: Introduction
---

# Introduction

## Platforms

Carimbo runs on multiple platforms—Windows, Linux, macOS, Android, iOS, WebAssembly, etc.—but currently, releases are only compiled for Windows (amd64), macOS (Apple Silicon), and WebAssembly.

## Lua Runtimes

Carimbo supports both `PUC-Rio` Lua and `LuaJIT`, PUC-Rio Lua is only used when compiling to WebAssembly or targeting iOS, since LuaJIT is not compatible with WebAssembly and JIT compilation is not permitted on iOS. For all other platforms, LuaJIT is used to take advantage of its Just-In-Time compilation performance benefits.

It’s important to always write code that is compatible with both runtimes to ensure maximum portability across all supported platforms.

### Essentials

#### Filesystem Structure

This is a basic filesystem structure for a project using `Carimbo`, check 

```
.
├── blobs
│   ├── myscene
│   │   ├── background.png
│   │   └── myitem.png
│   └── overlay
│       ├── myfont.png
│       └── mycursor.png
├── cursors
│   └── mycursor.json
├── fonts
│   └── myfont.json
├── objects
│   └── myscene
│       └── myitem.json
├── scenes
│   ├── myscene.json
│   └── myscene.lua
└── scripts
    ├── helpers
    │   └── functional.lua
    └── main.lua
```


`blobs/`

Binary asset storage for all media used by the game.

_Subdirectories:_

- myscene/: Assets specific to a given scene.
- overlay/: UI-related assets, both visual and audio.

_Includes:_

- Images (`.png`): Scene backgrounds or objects.
- Audio (`.ogg`): Sound effects or music.

`cursors/`

Cursor definitions in `.json` format.

`fonts/`

Font metadata files in `.json` format used by the UI renderer.

`objects/`

Scene-specific object definitions in `.json` format, grouped by scene slug.

`scenes/`

Scene logic and configuration. Must contains:

- A `.json` metadata file.
- A `.lua` script for behavior.

`scripts/`

All general Lua code.

- `helpers/`: Shared helper modules.
- `main.lua`: Game entry point.

Continue reading further details and functions at the [docs](/docs/category/get-started)