---
title: Block State (Block Condition Type)
date: 2021-04-05
---

# Block State

[Block Condition Type](../block_condition_types.md)

Checks a block state property of the block.

Type ID: `origins:block_state`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`property` | [String](../data_types/string.md) | | The name of the property that will be checked. Examples are `facing` or `age`. See: [Minecraft Fandom Wiki: Block States (List of block states)](https://minecraft.fandom.com/wiki/Block_states#List_of_block_states)
`comparison` | [Comparison](../data_types/comparison.md) | _optional_ | If specified, determines how the specified property will be compared to a specified value.
`compare_to` | [Integer](../data_types/integer.md) | _optional_ | If specified, the value to compare to the value of the specified property.
`value` | [Boolean](../data_types/boolean.md) | _optional_ | If specified, the boolean to compare to the value of the specified property if the specified property is a boolean.
`enum` | [String](../data_types/string.md) | _optional_ | If specified, the string to compare to the specified property if the specified property is a string.


### Examples

```json
"block_condition": {
    "type": "origins:and",
    "conditions": [
        {
            "type": "origins:block",
            "block": "minecraft:chest"
        },
        {
            "type": "origins:block_state",
            "property": "facing",
            "enum": "north"
        }
    ]
}
```

This example will check if a Chest block is facing north.