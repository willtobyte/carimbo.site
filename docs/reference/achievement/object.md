---
title: achievement
sidebar_position: 1
--- 

## object 

Represents a Steam achievement that can be unlocked.

## Methods

### `unlock(achievement_id)`

Unlocks the achievement for the current user.

**Parameters:**
- `achievement_id` (string) - The unique identifier of the achievement to unlock.

**Returns:** `boolean` - `true` if the achievement was successfully unlocked, `false` otherwise.

**Example:**
```lua
achievement:unlock("achievement_id")
```

## Notes

- Achievements are tied to the Steam API and require a valid Steam connection.
- Unlocking an achievement that's already unlocked will have no effect.
- Changes are synchronized with Steam servers automatically.