---
title: Modify Player Spawn (Power Type)
date: 2021-04-06
---
# Modify Player Spawn

[Power Type](../power_types.md).

Moves the player's spawn to another dimension and/or to a structure.

Type ID: `origins:modify_player_spawn`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`dimension` | [Identifier](../data_types/identifier.md) | | ID of the dimension the player should spawn in. Vanilla dimensions are `minecraft:overworld`, `minecraft:the_nether` and `minecraft:the_end`, but IDs of custom/modded dimensions should also work.
`biome` | [Identifier](../data_types/identifier.md) | _optional_ | If set, the player will spawn in the biome with this ID.
`structure` | [Identifier](../data_types/identifier.md) | _optional_ | ID of the structure the player should spawn in. Keep in mind that the structure needs to generate in the specified dimension!
`spawn_strategy` | [String](../data_types/string.md) | "default" | Either `default` or `center`. `default` tries to find a spawn close to the coordinates of the overworld spawn (while considering the `dimension_distance_multiplier`). `center` tries to spawn the player close to 0, 0 of the dimension.
`dimension_distance_multiplier` | [Float](../data_types/float.md) | _optional_ | Needs to be set when `spawn_strategy` is `default`. Defines the ratio of overworld blocks to blocks in this dimension, e.g. for the Nether this would be `0.125`.

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
