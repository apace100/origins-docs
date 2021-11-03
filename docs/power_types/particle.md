---
title: Particle (Power Type)
date: 2021-04-08
---

# Particle

[Power Type](../power_types.md)

Spawns particles on the player's body for visual effects.

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
`particle` | [Identifier](../data_types/identifier.md) | | ID of the particle type to use.
`frequency` | [Integer](../data_types/integer.md) | | How often the particles should spawn (interval in ticks).
`visible_in_first_person` | [Boolean](../data_types/boolean.md) | `false` | Determines whether the particle should be visible in first person.

### Example
```json
{
  	"type": "origins:particle",
  	"particle": "minecraft:portal",
  	"frequency": 4
}
```
Continuously spawns portal particles on the player.
