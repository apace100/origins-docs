---
title: Offset (Block Action Type)
date: 2021-04-05
---

# Offset

[Block Action Type](../block_action_types.md)

Executes the provided [Block Action Type](../block_action_types.md) at the position offset from the current position.

Type ID: `origins:offset`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Block Action Type](../block_action_types.md) | | The action to apply with the given offset.
`x` | [Integer](../data_types/integer.md) | `0` | How much to offset the position on the x-axis.
`y` | [Integer](../data_types/integer.md) | `0` | How much to offset the position on the y-axis.
`z` | [Integer](../data_types/integer.md) | `0` | How much to offset the position on the z-axis.


### Examples

```json
"block_action": {
    "type": "origins:offset",
    "action": {
        "type": "origins:add_block",
        "block": "minecraft:gravel"
    },
    "y": 1
}
```

This example will offset the position of the [Add Block (Block Action Type)](../block_action_types/add_block.md) in the positive Y axis, raising the positional context of the block action to be 1 block above to where it initially was.
