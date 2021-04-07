---
title: In Block
date: 2021-04-04
---
# In Block

[Entity Condition](../entity_conditions.md).

Checks whether the player is in a block (at the player's lower body half) that matches a specified block condition.

Type ID: `origins:in_block`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](../block_conditions.md) | |  The block condition which is applied to the block at the player's lower body half.

### Example:

```json
"condition": {
  "type": "origins:in_block",
  "block_condition": {
    "type": "origins:and",
    "conditions": [
      {
        "type": "origins:block",
        "block": "minecraft:sand"
      },
      {
        "type": "origins:offset",
        "y": 1,
        "condition": {
          "type": "origins:block",
          "block": "minecraft:sand"
        }
      }
    ]
  }
}
```

This condition applied to a power will make sure it's only active while the player is buried in sand.
