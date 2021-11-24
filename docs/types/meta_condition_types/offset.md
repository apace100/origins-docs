---
title: Offset (Meta Condition Type)
date: 2021-04-05
---

# Offset

[Meta Condition Type](../meta_condition_types.md)

Checks the provided [Block Condition](../block_conditions.md) at a position offset from the current position.

Type ID: `origins:offset`

!!! note

    **Only available as a [Block Condition](../block_conditions.md)**

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Block Condition](../block_conditions.md) | | The condition to check with the given offset.
`x` | [Integer](../types/data_types/integer.md) | `0` |  How much to offset the position on the x-axis.
`y` | [Integer](../types/data_types/integer.md) | `0` |  How much to offset the position on the y-axis.
`z` | [Integer](../types/data_types/integer.md) | `0` |  How much to offset the position on the z-axis.

### Example:
```json
"block_condition": {
    "type": "origins:offset",
    "condition": {
        "type": "origins:block",
        "block": "minecraft:grass_block"
    },
    "y": 1
}
```
This example checks if the block above the block is a grass block.