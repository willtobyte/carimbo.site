---
title: unlock
---

## `unlock()`

### Description

Unlocks the achievement for the current user.

**Parameters:**
- `achievement_id` (string) - The unique identifier of the achievement registered on the platform (like steam) to unlock.

**Returns:** `boolean` - `true` if the achievement was successfully unlocked, `false` otherwise.

**Example:**
```lua
achievement:unlock()
```

## Notes

- Achievements are tied to the Steam API and require a valid Steam connection.
- Unlocking an achievement that's already unlocked will have no effect.
- Changes are synchronized with Steam servers automatically.