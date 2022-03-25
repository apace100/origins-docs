---
title: NBT (Block Condition Type)
date: 2021-10-02
---

# NBT

[Block Condition Type](../block_condition_types.md)

Checks the NBT of the block entity.

Type ID: `apoli:nbt`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`nbt` | [String](../data_types/string.md) | | The NBT data to check for.


### Examples

```json
"block_condition": {
    "type": "apoli:and",
    "conditions": [
        {
            "type": "apoli:block",
            "block": "minecraft:beacon"
        },
        {
            "type": "apoli:nbt",
            "nbt": "{Levels: 1}"
        }
    ]
}
```

This example will check if Beacon block has a `Level` value of 1.
