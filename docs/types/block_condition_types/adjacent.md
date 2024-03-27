---
title: Adjacent (Block Condition Type)
date: 2021-04-05
---

# Adjacent

[Block Condition Type](../block_condition_types.md)

Checks whether a specified amount of blocks adjacent to the block in question fulfills a specified [Block Condition Type](../block_condition_types.md).

Type ID: `origins:adjacent`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`adjacent_condition` | [Block Condition Type](../block_condition_types.md) | | The block condition that needs to be fulfilled by adjacent blocks to count towards this condition.
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the number of adjacent blocks which fulfill the `adjacent_condition` block condition should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value at which the number of adjacent blocks which fulfill `adjacent_condition` will be compared to.


### Examples

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

This example will check if there are four or more Iron Ore blocks next to the block in question.
