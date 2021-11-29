---
title: Block (Block Condition Type)
date: 2021-04-05
---

# Block

[Block Condition Type](../block_condition_types.md)

Checks whether the block is a certain block (by ID).

Type ID: `origins:block`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the block that this block needs to be to pass the check.


### Examples

```json
"block_condition": {
    "type": "origins:block",
    "block": "minecraft:diamond_block"
}
```

This example checks if the block is a Diamond Block.
<br>

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

This example will check if the block is either a Diamond Block or an Emerald Block.
