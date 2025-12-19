---
title: Operating System 
sidebar_position: 1
--- 

## object 

Provides information about the current operating system.

## Methods

### `compute()`

Retrieves computational information about the system.

**Returns:** System compute information.

**Example:**
```lua
os:compute()
```

### `memory()`

Retrieves memory information about the system.

**Returns:** System memory information.

**Example:**
```lua
os:memory()
```

### `name()`

Gets the name of the operating system.

**Returns:** `string` - The operating system name.

**Example:**
```lua
os:name()
```

## Notes

- This object provides read-only system information.
- Information is retrieved from the host operating system at runtime.
- **Draft:** This documentation is preliminary and will be expanded with detailed return types and parameters.

