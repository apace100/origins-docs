---
title: Block Collision (Entity Condition Type)
date: 2021-04-04
---

# Block Collision

[Entity Condition Type](../entity_condition_types.md)

Checks whether the bounding box of the entity collides with a block.

Type ID: `origins:block_collision`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the condition type will only evaluate to true if the bounding box of the entity is colliding with a block that fulfills this condition.
`offset_x` | [Float](../data_types/float.md) | `0` |  By how much of the bounding box size should the box be offset in the X direction (e.g.: 0 = no offset, 1 = offset of exact width, 2 = offset of twice the width of the bounding box)
`offset_y` | [Float](../data_types/float.md) | `0` |  By how much of the bounding box size should the box be offset in the Y direction (e.g.: 0 = no offset, 1 = offset of exact height, 2 = offset of twice the height of the bounding box)
`offset_z` | [Float](../data_types/float.md) | `0` | By how much of the bounding box size should the box be offset in the Z direction (e.g.: 0 = no offset, 1 = offset of exact depth, 2 = offset of twice the depth of the bounding box)


### Examples

```json
"condition": {
    "type": "origins:block_collision",
    "offset_x": 0.1,
    "offset_y": 0,
    "offset_z": 0.1
}
```

This example will check if the entity is colliding with the positive X or Z faces of a block.
<br>

```json
"condition": {
    "type": "origins:or",
    "conditions": [
        {
            "type": "origins:block_collision",
            "block_condition": {
                "type": "origins:block",
                "block": "minecraft:slime_block"
            },
            "offset_x": 0.1,
            "offset_z": 0.1
        },
        {
            "type": "origins:block_collision",
            "block_condition": {
                "type": "origins:block",
                "block": "minecraft:slime_block"
            },
            "offset_x": -0.1,
            "offset_z": -0.1
        }
    ]
}
```

This example will check if the entity is colliding with the X and Z faces of a Slime block.
