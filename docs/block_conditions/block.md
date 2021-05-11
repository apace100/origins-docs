---
title: Block (Condition)
date: 2021-04-05
---
# Block

[Block Condition](../block_conditions.md).

Checks whether the block is a certain block (by ID).

Type ID: `origins:block`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`block` | [String](../data_types/string.md) | | ID of the block that this block needs to be to pass the check.

### Examples:
```json
"block_condition": {
    "type": "origins:block",
    "block": "minecraft:diamond_block"
}
```
This example checks if the block is a Diamond Block.

```json
"block_condition": {
    "type": "origins:or",
    "conditions": [
        {
            "type": "origins:block",
            "block": "minecraft:diamond_block"
        },
        {
            "type": "origins:block",
            "block": "minecraft:emerald_block"
        }
    ]
}
```
This example checks if the block is either a Diamond Block or an Emerald Block, though using the [`origins:in_tag`](../block_conditions/in_tag.md) block condition type would be better for checking multiple block types.