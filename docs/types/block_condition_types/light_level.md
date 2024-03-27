---
title: Light Level (Block Condition Type)
date: 2021-04-05
---

# Light Level

[Block Condition Type](../block_condition_types.md)

Allows checking the light level at the block's position.

Type ID: `origins:light_level`


!!! note

    If no light type is specified in the `light_type` field, the highest light level between the block light level and **internal** sky light level will be used as the "resulting" light level of the position of the block.

    See [Minecraft Wiki: Light (Internal light level)](https://minecraft.wiki/w/Light#Internal_light_level) for more information about internal sky light levels.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`light_type` | [String](../data_types/string.md) | _optional_ | If specified, determines the type of light level to compare. Accepts `"sky"` or `"block"`.
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the light level should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value at which the light level will be compared to.


### Examples

```json
"block_condition": {
    "type": "origins:light_level",
    "light_type": "block",
    "comparison": ">",
    "compare_to": 10
}
```

This example will check if the light level at the specified position is more than 10, and is emitted by a block.
