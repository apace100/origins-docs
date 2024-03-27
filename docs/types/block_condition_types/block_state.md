---
title: Block State (Block Condition Type)
date: 2021-04-05
---

# Block State

[Block Condition Type](../block_condition_types.md)

Checks a block state property of the block.

Type ID: `origins:block_state`


!!! note

    If none of the expected fields are specified, this condition will just check if the block has the specified property.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`property` | [String](../data_types/string.md) | | The name of the property that will be checked. Examples are `facing` or `age`. See: [Minecraft Wiki: Block States (List of block states)](https://minecraft.wiki/w/Block_states#List_of_block_states)
`comparison` | [Comparison](../data_types/comparison.md) | _optional_ | If specified and if the property uses an integer, determines how the integer value of the specified property should be compared to the specified value. <span style="color: goldenrod;"><b>Only used if the specified property has an [integer](../data_types/integer.md) value.</b></span>
`compare_to` | [Integer](../data_types/integer.md) | _optional_ | If specified, the itneger at which the integer value of the specified property will be compared to. <span style="color: goldenrod;"><b>Only used if the specified property has an [integer](../data_types/integer.md) value.</b></span>
`value` | [Boolean](../data_types/boolean.md) | _optional_ | If specified, the boolean to compare to the boolean value of the specified property. <span style="color: goldenrod;"><b>Only used if the specified property has a [boolean](../data_types/boolean.md) value.</b></span>
`enum` | [String](../data_types//string.md) | _optional_ | If specified, the string at which the string value of the specified property will be compared to. <span style="color: goldenrod;"><b>Only used if the specified property has a [string](../data_types/string.md) value.</b></span>


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
