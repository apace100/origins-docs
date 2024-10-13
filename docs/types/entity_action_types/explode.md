---
title: Explode (Entity Action Type)
date: 2021-10-02
---

# Explode

[Entity Action Type](../entity_action_types.md)

Summons an explosion with a specific explosion power.

Type ID: `origins:explode`

!!! note

    See [Minecraft Wiki: Explosion (Causes)](https://minecraft.wiki/w/Explosion#Causes) for a list of power values that are used in vanilla.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Float](../data_types/float.md) | | Determines the power of the explosion.
`destruction_type` | [Destruction Type](../data_types/destruction_type.md) | `"break"` | Determines the effect of the explosion to the terrain.
`damage_self` | [Boolean](../data_types/boolean.md) | `true` | Determines if the entity that invoked the action should take damage from the summoned explosion.
`indestructible` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the blocks that fulfill this condition will not be destroyed by the summoned explosion.
`destructible` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, only the blocks that fulfill this condition will be destroyed by the summoned explosion.
`create_fire` | [Boolean](../data_types/boolean.md) | `false` | Determines if the summoned explosion should create fire.


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

This example will summon an explosion that will **not** damage the entity that invoked the action, the terrain, or create fire.
