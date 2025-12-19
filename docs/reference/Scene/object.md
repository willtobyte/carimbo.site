---
title: object 
--- 

## SceneKind

An enumeration that defines the different types of scene elements.

## Values

### `SceneKind.object`

Represents a standard scene object.

**Example:**
```lua
local kind = SceneKind.object
```

### `SceneKind.effect`

Represents a visual effect in the scene.

**Example:**
```lua
local kind = SceneKind.effect
```

### `SceneKind.particle`

Represents a particle system in the scene.

**Example:**
```lua
local kind = SceneKind.particle
```

## Usage

SceneKind values are typically used when creating or filtering scene elements to specify their type.

**Example:**
```lua
-- Create a scene element with a specific kind
local element = Scene.create(SceneKind.particle)

-- Check the kind of an existing element
if element.kind == SceneKind.effect then
    print("This is an effect")
end
```

## Notes

- SceneKind is an enumeration and its values are read-only.
- Each scene element should have exactly one kind.
- **Draft:** This documentation is preliminary and will be expanded with more detailed usage examples.