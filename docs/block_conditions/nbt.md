---
title: NBT (Block Condition)
date: 2021-10-02
---
# NBT

[Block Condition](../block_conditions.md)

Checks the NBT of the block entity.

Type ID: `origins:nbt`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`nbt` | [String](../data_types/string.md) | | The NBT data to check for.

### Example
```json
"block_condition": {
    "type": "origins:and",
    "conditions": [
        {
            "type": "origins:block",
            "block": "minecraft:beacon"
        },
        {
            "type": "origins:nbt",
            "nbt": "{Levels: 1}"
        }
    ]
}
```
This example checks if a beacon block has a level value of 1.