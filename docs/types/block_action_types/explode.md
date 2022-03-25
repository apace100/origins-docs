---
title: Explode (Block Action Type)
date: 2021-11-30
---

# Explode

[Block Action Type](../block_action_types.md)

Summons an explosion at the position of the block.

Type ID: `apoli:explode`

### Fields

| Field              | Type                                                | Default    | Description                                                                                                                                                             |
| ------------------ | --------------------------------------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `power`            | [Float](../data_types/float.md)                     |            | Determines the power of the explosion.                                                                                                                                  |
| `destruction_type` | [String](../data_types/string.md)                   | `"break"`  | Determines if the explosion should destroy the terrain, destroy the terrain and drop the loot of the blocks, or none (`"destroy"`, `"break"` or `"none"` respectively). |
| `damage_self`      | [Boolean](../data_types/boolean.md)                 | `true`     | Determines if the exploding block should be affected by the summoned explosion.                                                                                         |
| `indestructible`   | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the blocks that fulfills the specified block condition type is not destroyed by the summoned explosion.                                                   |
| `destructible`     | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the blocks that fulfills this specified block condition type are the **only** blocks that are destroyed by the summoned explosion.                        |
| `create_fire`      | [Boolean](../data_types/boolean.md)                 | `false`    | Determines if the explosion should create fire.                                                                                                                         |

### Examples

```json
"block_action": {
    "type": "apoli:explode",
    "power": 5,
    "destruction_type": "none",
    "damage_self": false,
    "create_fire": false
}
```

This example will summon an explosion that will **not** damage the block that has summoned the explosion, or the terrain, or create fire.
