--- 
sidebar_position: 1
title: Scenes
--- 

Every game needs at least one scene. It is used to load objects, sound effects, and handle input logic through callbacks.

```lua 
-- Scene script with basic setup, interaction, and cleanup logic.

local scene = {}

-- Object pool.
local pool = {}

function scene.on_enter()
  -- On scene enter.

  -- Retrieve a sound effect from the scenario.
  pool.theme = scene:get("theme", SceneKind.effect)
  pool.theme:play(true)

  -- Retrieve an object from the scenario, useful when you need to manipulate it.
  pool.object = scene:get("object", SceneKind.object)
end

function scene.on_loop()
  -- Every loop.
end

function scene.on_text(text)
  -- On text input.
end

function scene.on_keypress(code)
  -- On key press.

  -- Set an action for the play of the object.
  pool.object.action = "play"
end

function scene.on_motion(x, y)
  -- On mouse motion.
end

function scene.on_leave()
  -- On scene leave.

  -- No need to stop any sound effects manually.
  -- SceneManager will handle stopping all sounds before the transition.

  -- Clean up the object pool.
  for o in pairs(pool) do
    pool[o] = nil
  end
end

return scene
```

Before using it, you must always `register` the scene. This can be done all at once during the engine’s boot process, or `lazily ` as the player progresses, like this:

After registering one or more scenes, call `set` to make the SceneManager use the selected scene.

```lua 
local scenemanager = engine:scenemanager()

function setup()
  scenemanager:register("myscene")
  -- ...Other scenes.

  scenemanager:set("myscene")
end
```