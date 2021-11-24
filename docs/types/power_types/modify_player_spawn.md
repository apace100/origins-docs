---
title: Modify Player Spawn (Power Type)
date: 2021-04-06
---

# Modify Player Spawn

[Power Type](../power_types.md)

Modifies the location of the player's spawnpoint to the specified dimension, biome and/or structure.

Type ID: `origins:modify_player_spawn`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`dimension` | [Identifier](../types/data_types/identifier.md) | | The namespace and ID of the dimension the player should spawn in.
`biome` | [Identifier](../types/data_types/identifier.md) | _optional_ | If specified, the player will only spawn in the biome that matches the specified namespace and ID.
`structure` | [Identifier](../types/data_types/identifier.md) | _optional_ | If specified, the player will only spawn in the specified namespace and ID of the structure. **The structure needs to generate in the specified dimension.**
`spawn_strategy` | [String](../data_types/string.md) | `"default"` | Determines whether the player should spawn near the world spawnpoint (0, 0) of the dimension (`"center"`) or near the coordinates of the Overworld spawnpoint (whilst considering the value of the `dimension_distance_multiplier` field) (`"default"`).
`dimension_distance_multiplier` | [Float](../types/data_types/float.md) | _optional_ | Defines the ratio of Overworld blocks to blocks in the specified dimension. e.g: for The Nether dimension, this would be set to `0.125`. **This needs to be set when `spawn_strategy` is set to `"default"`**

### Example

```json
{
  "type": "origins:modify_player_spawn",
  "dimension": "minecraft:the_end",
  "structure": "minecraft:endcity",
  "spawn_strategy": "center"
}
```
With this power, players will spawn in the End at an End City. Keep in mind that structure location is costly and it might take one or two seconds before the player gets teleported there when choosing this power. I will look into improving performance in the future.
