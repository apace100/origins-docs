---
title: In Block (Entity Condition Type)
date: 2021-04-04
---

# In Block

[Entity Condition Type](../entity_condition_types.md)

Checks whether a block that fulfills the specified [Block Condition Type](../block_condition_types.md) is overlapping with the entity's feet.

Type ID: `origins:in_block`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | | The block condition type to check for on the block that is overlapping with the entity's feet.


### Examples

```json
"condition": {
    "type": "origins:in_block",
    "block_condition": {
        "type": "origins:block",
        "block": "minecraft:grass"
    }
}
```

This example will check if Grass (foliage) is currently overlapping the entity's feet.
<br>

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
                "condition": {
                    "type": "origins:block",
                    "block": "minecraft:sand"
                },
                "y": 1
            }
        ]
    }
}
```

This example will check if there are Sand blocks at the entity's feet and eyes, essentially checking if the entity is buried in sand.
