---
title: Particle (Power Type)
date: 2021-04-08
---

# Particle

[Power Type](../power_types.md)

Spawns particles on the body of the entity that has the power for visual effects.

Type ID: `origins:particle`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`particle` | [Particle Effect](../data_types/particle_effect.md) | | The particle type that will be spawned.
`frequency` | [Integer](../data_types/integer.md) | | Determines how often the particles should spawn (interval in ticks).
`count` | [Integer](../data_types/integer.md) | `1` | Determines the amount of particles to spawn.
`speed` | [Float](../data_types/float.md) | `0.0` | Determines the speed of the specified particle type.
`spread` | [Vector](../data_types/vector.md) | `{"x": 0.25, "y": 0.5, "z": 0.25}` | Determines the size of the three-dimensional cuboid volume to spawn the specified particle type in.
`offset_y` | [Float](../data_types/float.md) | `1.0` | The offset of where the particle will be centered in the Y axis.
`visible_in_first_person` | [Boolean](../data_types/boolean.md) | `false` | Determines whether the particle type should be visible in first person.
`visible_while_invisible` | [Boolean](../data_types/boolean.md) | `false` | Determines whether the particle type should be visible if the entity is invisible.


### Examples

```json
{
  	"type": "origins:particle",
  	"particle": "minecraft:portal",
  	"frequency": 4
}
```

This example will continuously spawn portal particles on the entity that has the power.
