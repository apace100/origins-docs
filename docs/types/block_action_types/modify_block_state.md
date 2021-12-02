---
title: Modify Block State (Block Action Type)
date: 2021-11-30
---

# Modify Block State

[Block Action Type](../block_action_types.md)

Modifies the "block state" of a block.

Type ID: `origins:modify_block_state`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`property` | [String](../data_types/string.md) | | The name of the property that should be modified. Examples are `facing` or `age`. See: [Minecraft Fandom Wiki: Block States (List of block states)](https://minecraft.fandom.com/wiki/Block_states#List_of_block_states)
`operation` | [String](../data_types/string.md) | `"add"` | If the property contains a boolean value, determines if the action should add or set the value of the property. Accepts `"add"` or `"set"`.
`change` | [Integer](../data_types/integer.md) | _optional_ | If the property contains a boolean value, this value will be applied to the value of the property.
`value` | [Boolean](../data_types/boolean.md) | _optional_ | If the property contains a boolean value, this is the value the property needs to be modified.
`enum` | [String](../data_types/string.md) | _optional_ | If the property contains different string values, this is the string value the property needs to be modified.
`cycle` | [Boolean](../data_types/boolean.md) | false | If set, cycles through all available states of the specified property.

### Examples

```json
"block_action": {
	"type": "origins:modify_block_state",
	"property": "facing",
	"cycle": true
}
```

This example will cycle through the values of the `facing` property if available.
