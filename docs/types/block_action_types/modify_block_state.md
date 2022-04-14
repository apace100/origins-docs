---
title: Modify Block State (Block Action Type)
date: 2021-11-30
---

# Modify Block State

[Block Action Type](../block_action_types.md)

Modifies the block state property of the block. Depending on the property type, different values are expected: boolean properties use `value`, enumeration properties use `enum`, and integer properties use `operation` and `change`.

Type ID: `origins:modify_block_state`

!!! note

    If none of the expected fields are specified, this action will do nothing.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`property` | [String](../data_types/string.md) | | The name of the property that will be modified. Examples are `facing` or `age`. See [Minecraft Fandom Wiki: Block States (List of block states)](https://minecraft.fandom.com/wiki/Block_states#List_of_block_states) for possible values.
`operation` | [String](../data_types/string.md) | `"add"` | Determines how the value specified in the `change` field is operated on the specified property. Accepts `"add"` or `"set"`.
`change` | [Integer](../data_types/integer.md) | _optional_ | If specified, the value to add, remove or set to/from the specified property if the specified property is an integer.
`value` | [Boolean](../data_types/boolean.md) | _optional_ | If specified, the boolean to use as the new value for the specified property if the specified property is a boolean.
`enum` | [String](../data_types/string.md) | _optional_ | If specified, the string to use as the new value for the specified property if the specified property is a string.
`cycle` | [Boolean](../data_types/boolean.md) | `false` | If set to true, changes the property to the next state in the cycle, ignoring all other optional fields. All property types can use this operation.


### Examples

```json
"block_action": {
	"type": "origins:modify_block_state",
	"property": "facing",
	"cycle": true
}
```

This example will cycle through the values of the `facing` property if available.
