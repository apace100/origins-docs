---
title: Explode (Block Action Type)
date: 2021-11-30
---

# Explode

[Block Action Type](../block_action_types.md)

Summons an explosion with a specific explosion power.

Type ID: `origins:explode`

!!! note

    See [Minecraft Fandom: Explosion (Explosion strength)](https://minecraft.fandom.com/wiki/Explosion#Explosion_strength) for a list of power values that are used in vanilla.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Float](../data_types/float.md) | | Determines the power of the explosion.
`destruction_type` | [Destruction Type](../../misc/extras/destruction_types.md) | `"break"` | Determines the effect of the explosion to the terrain.
`damage_self` | [Boolean](../data_types/boolean.md) | `true` | Determines if the block that invoked the action should take damage from the summoned explosion.
`indestructible` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the blocks that fulfill this condition will not be destroyed by the summoned explosion.
`destructible` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, only the blocks that fulfill this condition will be destroyed by the summoned explosion.
`create_fire` | [Boolean](../data_types/boolean.md) | `false` | Determines if the summoned explosion should create fire.


### Examples

```json
"block_action": {
    "type": "origins:explode",
    "power": 5,
    "destruction_type": "none",
    "damage_self": false,
    "create_fire": false
}
```

This example will summon an explosion that will **not** damage the block that invoked the action, the terrain, or create fire.
