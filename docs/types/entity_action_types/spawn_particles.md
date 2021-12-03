---
title: Spawn Particles (Entity Action Type)
date: 2021-12-03
---

# Spawn Particles

[Entity Action Type](../entity_action_types.md)

Spawns particles on the body of the entity that has the power for visual effects.

Type ID: `origins:spawn_particles`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`particle` | [Particle Effect](../data_types/particle_effect.md) | | The particle type that will be spawned.
`count` | [Integer](../data_types/integer.md) | | How much of the specified particle type will be spawned.
`speed` | [Float](../data_types/float.md) | `0.0` | Determines the speed of the specified particle type.
`force` | [Boolean](../data_types/boolean.md) | `false` | If set to `true`, the specified particle type that will be spawned can be seen from a far distance.
`spread` | [Vector](../data_types/vector.md) | `{"x": 0.5, "y": 0.25, "z": 0.5}` | Determines the size of the three-dimensional cuboid volume to spawn the specified particle type in.
`offset_y` | [Float](../data_types/float.md) | `0.5` | The offset of where the particle will be centered in the Y axis.


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
        "x": 0.8,
        "y": 0.8,
        "z": 0.8
    }
}
```

This example will display a block particle that will use the Redstone Block texture.
