---
title: Particle (Power Type)
date: 2021-04-08
---

# Particle

[Power Type](../power_types.md)

Spawns particles on the body of the entity that has the power for visual effects.

Type ID: `origins:particle`

!!! caution

    This power type does **not** currently support particle types that require additional parameters. Those particle types being:

    * `minecraft:block`
    * `minecraft:dust_color_transition`
    * `minecraft:dust`
    * `minecraft:falling_dust`
    * `minecraft:item`
    * `minecraft:vibration`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`particle` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the partice type to use.
`frequency` | [Integer](../data_types/integer.md) | | Determines how often the particles should spawn (interval in ticks).
`visible_in_first_person` | [Boolean](../data_types/boolean.md) | `false` | Determines whether the particle should be visible in first person.


### Examples

```json
{
  	"type": "origins:particle",
  	"particle": "minecraft:portal",
  	"frequency": 4
}
```

This example will continuously spawn portal particles on the entity that has the power.
