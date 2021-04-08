---
title: Particle (Power Type)
date: 2021-04-08
---
# Particle

[Power Type](../power_types.md).

Spawns particles on the player's body for visual effects.

**Note:** Currently, the particles are only available for other players to see (they won't even be visible in F5 on yourself, if you have this power). This will change in a future update (very likely the next one).

Type ID: `origins:particle`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`particle` | [Identifier](../data_types/identifier.md) | | ID of the particle type to use.
`frequency` | [Integer](../data_types/integer.md) | | How often the particles should spawn (interval in ticks).

### Example
```json
{
  	"type": "origins:particle",
  	"particle": "minecraft:portal",
  	"frequency": 4
}
```
Continuously spawns portal particles on the player.
