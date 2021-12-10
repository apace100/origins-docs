---
title: Vector (Data Type)
date: 2021-12-03
---

# Vector

[Data Type](../data_types.md)

An [Object](object.md) that specifies the X, Y and Z coordinates of a certain point in space.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`x` | [Float](float.md) | `0` | The X coordinate of the point.
`y` | [Float](float.md) | `0` | The Y coordinate of the point.
`z` | [Float](float.md) | `0` | The Z coordinate of the point.

### Examples

```json
"entity_action": {
    "type": "origins:spawn_particles",
    "particle": {
        "type": "minecraft:block",
        "params": "minecraft:redstone_block"
    },
    "count": 16,
    "speed": 0.0,
    "force": true,
    "spread": {
        "x": 3.0,
        "y": 0.0,
        "z": 3.0
    }
}
```

A [Spawn Particles (Entity Action Type)](../entity_action_types/spawn_particles.md) that spawns a cuboid of about 5x0x5 in size, which has a volume of 25 blocks.
