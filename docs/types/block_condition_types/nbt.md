---
title: NBT (Block Condition Type)
date: 2021-10-02
---

# NBT

[Block Condition Type](../block_condition_types.md)

Checks the NBT of the block entity.

Type ID: `origins:nbt`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`nbt` | [NBT](../data_types/nbt.md) | | The NBT data to check for.


### Examples

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

This example will check if Beacon block has a `Level` value of 1.
