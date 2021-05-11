---
title: Adjacent (Condition)
date: 2021-04-05
---
# Adjacent

[Block Condition](../block_conditions.md).

Checks whether a certain amount of blocks adjacent to the block in question fulfill a certain block condition.

Type ID: `origins:adjacent`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`adjacent_condition` | [Block Condition](../block_conditions.md) | | The block condition that needs to be fulfilled by adjacent blocks to count towards this condition.
`comparison` | [Comparison](../data_types/comparison.md) | |  How the number of adjacent blocks which fulfill `adjacent_condition` should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value to compare the number to.

### Example:
```json
"block_condition": {
    "type": "origins:adjacent",
    "adjacent_condition": {
        "type": "origins:block",
        "block": "minecraft:iron_ore"
    },
    "comparison": ">=",
    "compare_to": 4
}
```
This example checks if there are two or more Iron Ore blocks next to the block in question.