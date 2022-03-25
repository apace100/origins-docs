---
title: Modify Player Spawn (Power Type)
date: 2021-04-06
---

# Modify Player Spawn

[Power Type](../power_types.md)

Modifies the location of the player's spawnpoint to the specified dimension, biome and/or structure.

Type ID: `apoli:modify_player_spawn`

!!! note

    Keep in mind that structure location is costly and it might take one or two seconds before the player gets teleported when choosing the power.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`dimension` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the dimension the player should spawn in.
`biome` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the player will only spawn in the biome that matches the specified namespace and ID.
`structure` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the player will only spawn in the specified namespace and ID of the structure. **The structure needs to generate in the specified dimension.**
`spawn_strategy` | [String](../data_types/string.md) | `"default"` | Determines whether the player should spawn near the world spawnpoint (0, 0) of the dimension (`"center"`) or near the coordinates of the Overworld spawnpoint (whilst considering the value of the `dimension_distance_multiplier` field) (`"default"`).
`dimension_distance_multiplier` | [Float](../data_types/float.md) | _optional_ | Defines the ratio of Overworld blocks to blocks in the specified dimension. e.g: for The Nether dimension, this would be set to `0.125`. **This needs to be set when `spawn_strategy` is set to `"default"`**


### Examples

```json
{
  "type": "apoli:modify_player_spawn",
  "dimension": "minecraft:the_end",
  "structure": "minecraft:endcity",
  "spawn_strategy": "center"
}
```

This example will let players spawn at an End City in The End dimension.
