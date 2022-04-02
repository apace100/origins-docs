---
title: Explode (Entity Action Type)
date: 2021-10-02
---

# Explode

[Entity Action Type](../entity_action_types.md)

Summons an explosion at the position of the entity.

Type ID: `origins:explode`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Float](../data_types/float.md) | | Determines the power of the explosion.
`destruction_type` | [Destruction Type](../../misc/extras/destruction_types.md) | `"break"` | Determines the effect of the explosion on the terrain.
`damage_self` | [Boolean](../data_types/boolean.md) | `true` | Determines if the player should take damage from the summoned explosion.
`indestructible` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the blocks that fulfills the specified block condition type is not destroyed by the summoned explosion.
`destructible` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the blocks that fulfills this specified block condition type are the **only** blocks that are destroyed by the summoned explosion.
`create_fire` | [Boolean](../data_types/boolean.md) | `false` | Determines if the explosion should create fire.


### Examples

```json
"entity_action": {
    "type": "origins:explode",
    "power": 5,
    "destruction_type": "none",
    "damage_self": false,
    "create_fire": false
}
```

This example will summon an explosion that will **not** damage the entity that has summoned the explosion, or the terrain, or create fire.
