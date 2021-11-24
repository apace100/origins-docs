---
title: Shader (Power Type)
date: 2021-07-13
---

# Shader

[Power Type](../power_types.md)

Applies a post-processing shader to the vision of the entity that has the power.

Type ID: `origins:shader`

!!! note

    For more information about post-processing shaders, visit [Minecraft Wiki: Shaders (Before 1.9)](https://minecraft.fandom.com/wiki/Shaders/Before_1.9)

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`shader` | [Identifier](../types/data_types/identifier.md) | | Specifies the location of the shader resource file to use.
`toggleable` | [Boolean](../types/data_types/boolean.md) | `true` | Determines if the applied shader can be toggled.

### Example
```json
{
  	"type": "origins:shader",
  	"shader": "minecraft:shaders/post/pencil.json"
}
```
This makes the player view the world as a pencil sketch!
