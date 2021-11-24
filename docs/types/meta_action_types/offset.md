---
title: Offset (Meta Action Type)
date: 2021-04-05
---

# Offset

[Meta Action Type](../meta_action_types.md)

Executes the provided [Block Action](../block_actions.md) at the position offset from the current position.

Type ID: `origins:offset`

!!! note

    **Only available as a [Block Action](../block_actions.md).**

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Block Action](../block_actions.md) | | The action to apply with the given offset.
`x` | [Integer](../data_types/integer.md) | `0` | How much to offset the position on the x-axis.
`y` | [Integer](../data_types/integer.md) | `0` | How much to offset the position on the y-axis.
`z` | [Integer](../data_types/integer.md) | `0` | How much to offset the position on the z-axis.

### Example
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
This example offsets the [`origins:add_block`](../block_actions/add_block.md) block action in the positive Y axis, raising the positional context of the block action to be 1 block above to where it initially was.