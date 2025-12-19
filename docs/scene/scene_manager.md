---
title: SceneManager 
sidebar_position: 1
---

Manager is responsible for registering, setting, and destroying scenes. A scene can include a background, objects, and sound effects, all declared in a metadata JSON. Additionally, every scene must include a Lua script to handle specific situations.

Before calling set, all scenes must be registered. The destroy function is used to free memory when the game no longer intends to use a scene, which is useful for releasing resources.

```lua
local scenemanager = engine:scenemanager()

-- Register a scene by its name. It must have both scenename.json and scenename.lua files in the scenes directory.
scenemanager:register("scenename")

-- Set the current scene in the game.
scenemanager:set("scenename")

-- Destroys a previously registered scene that will no longer be used.
scenemanager:destroy("scenename")
```