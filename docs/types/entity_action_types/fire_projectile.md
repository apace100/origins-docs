---
title: Fire Projectile (Entity Action Type)
date: 2023-08-02
---

#   Fire Projectile

[Entity Action Type](../entity_action_types.md)

Fires one or more projectiles or entities.

Type ID: `origins:fire_projectile`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_type` | [Identifier](../data_types/identifier.md) | | The identifier of the projectile or entity that will be launched.
`divergence` | [Float](../data_types/float.md) | `1.0` | Determines how much the projectile or entity that will be launched is affected by random spread.
`speed` | [Float](../data_types/float.md) | `1.0` | Determines the speed of the projectile or entity that will be launched.
`count` | [Integer](../data_types/integer.md) | `1` | Determines the count of projectiles or entities that will be launched.
`tag` | [NBT](../data_types/nbt.md) | _optional_ | If specified, this NBT data will be added to the projectile or entity that will be launched.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this entity action will be executed on the projectile or entity that will be launched.


### Examples

```json
"entity_action": {
    "type": "origins:fire_projectile",
    "entity_type": "minecraft:snowball",
    "divergence": 3.0,
    "count": 3
}
```

This example will fire three snowballs at where the player is facing.
