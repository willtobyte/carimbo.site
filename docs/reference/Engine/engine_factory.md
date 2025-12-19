---
title: EngineFactory
sidebar_position: 1
---


A builder class for configuring and creating game engine instances. Uses a fluent interface pattern where methods can be chained together.

## Constructor

### `EngineFactory()`

Creates a new EngineFactory instance with default settings.

**Example:**
```lua
local factory = EngineFactory()
```

## Methods

### `with_title(title)`

Sets the window title for the game.

**Parameters:**
- `title` (string) - The window title text.

**Returns:** `EngineFactory` - Returns self for method chaining.

**Example:**
```lua
factory:with_title("My Game")
```

### `with_width(width)`

Sets the window width in pixels.

**Parameters:**
- `width` (number) - The window width.

**Returns:** `EngineFactory` - Returns self for method chaining.

**Example:**
```lua
factory:with_width(1280)
```

### `with_height(height)`

Sets the window height in pixels.

**Parameters:**
- `height` (number) - The window height.

**Returns:** `EngineFactory` - Returns self for method chaining.

**Example:**
```lua
factory:with_height(720)
```

### `with_scale(scale)`

Sets the rendering scale factor.

**Parameters:**
- `scale` (number) - The scale multiplier.

**Returns:** `EngineFactory` - Returns self for method chaining.

**Example:**
```lua
factory:with_scale(2.0)
```

### `with_gravity(gravity)`

Sets the physics gravity value.

**Parameters:**
- `gravity` (number) - The gravity force value.

**Returns:** `EngineFactory` - Returns self for method chaining.

**Example:**
```lua
factory:with_gravity(9.8)
```

### `with_fullscreen(fullscreen)`

Enables or disables fullscreen mode.

**Parameters:**
- `fullscreen` (boolean) - `true` for fulls