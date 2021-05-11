---
title: Block State (Condition)
date: 2021-04-05
---
# Block State

[Block Condition](../block_conditions.md).

Checks a block state property of the block.

Type ID: `origins:block_state`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`property` | [String](../data_types/string.md) | | The name of the property that should be checked. Examples are `facing` or `age`. See: [Block States (MC Wiki)](https://minecraft.fandom.com/wiki/Block_states#List_of_block_states)
`comparison` | [Comparison](../data_types/comparison.md) | _optional_ | If the property contains an integer value, this is the comparison the will be used to compare the property's value to the specified `compare_to` integer.
`compare_to` | [Integer](../data_types/integer.md) | _optional_ | If the property contains an integer value, this is the value the property's value will be compared to.
`value` | [Boolean](../data_types/boolean.md) | _optional_ | If the property contains a boolean value, this is the value the property needs to be to pass the check.
`enum` | [String](../data_types/string.md) | _optional_ | If the property contains different string values, this is the string value the property needs to be to pass the check.

### Example:
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
This example checks if a chest block is facing north.