---
title: Explode (Entity Action)
date: 2021-10-02
---
# Explode

[Entity Action](../entity_actions.md)

Makes the entity explode, and whether if they take damage from the explosion or be able to destroy the terrain.

Type ID: `origins:explode`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Float](../data_types/float.md) | | Determines the power of the explosion.
`destruction_type` | [String](../data_types/string.md) | `"break"` | Determines if the explosion should destroy the terrain, destroy the terrain and drop the loot of the blocks, or none. Accepts either `"destroy"`, `"break"` or `"none"`.
`damage_self` | [Boolean](../data_types/boolean.md) | true | Determines if the player should take damage from the explosion.
`indestructible` | [Block Condition](../block_conditions.md) | _optional_ | If set, blocks specified in this block condition object is not destroyed by the explosion.
`destructible` | [Block Condition](../block_conditions.md) | _optional_ | If set, blocks specified in this block condition object will be the only blocks destroyed by the explosion.
`create_fire` | [Boolean](../data_types/boolean.md) | false | Determines if the explosion should create fire.

### Example
```json
"entity_action": {
    "type": "origins:explode",
    "power": 5,
    "destruction_type": "none",
    "damage_self": false,
    "create_fire": false
}
```
Makes the entity explode without damaging itself and the terrain.