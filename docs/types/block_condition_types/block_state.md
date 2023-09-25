---
title: Block State (Block Condition Type)
date: 2021-04-05
---

# Block State

[Block Condition Type](../block_condition_types.md)

Checks a block state property of the block.  Depending on the property type, different values are expected: boolean properties use `value`, enumeration properties use `enum`, and integer properties use `comparison` and `compare_to`.

Type ID: `origins:block_state`

!!! note

    If none of the expected fields are specified, this condition will just check if the block has the specified property.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`property` | [String](../data_types/string.md) | | The name of the property that will be checked. Examples are `facing` or `age`. See: [Minecraft Wiki: Block States (List of block states)](https://minecraft.wiki/w/Block_states#List_of_block_states)
`comparison` | [Comparison](../data_types/comparison.md) | _optional_ | If specified, determines how the specified property will be compared to a specified value. If not and the property is an integer, it will just check if the block has the specified property.
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

```json
"block_condition": {
	"type": "origins:block_state",
	"property": "age"
}
```

This example will check if the specified block has the `age` Block State property.
