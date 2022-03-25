---
title: Particle (Power Type)
date: 2021-04-08
---

# Particle

[Power Type](../power_types.md)

Spawns particles on the body of the entity that has the power for visual effects.

Type ID: `apoli:particle`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`particle` | [Particle Effect](../data_types/particle_effect.md) | | The particle type that will be spawned.
`frequency` | [Integer](../data_types/integer.md) | | Determines how often the particles should spawn (interval in ticks).
`visible_in_first_person` | [Boolean](../data_types/boolean.md) | `false` | Determines whether the particle should be visible in first person.


### Examples

```json
{
  	"type": "apoli:particle",
  	"particle": "minecraft:portal",
  	"frequency": 4
}
```

This example will continuously spawn portal particles on the entity that has the power.
