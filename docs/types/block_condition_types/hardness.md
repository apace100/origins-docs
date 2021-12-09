---
title: Hardness (Block Condition Type)
date: 2021-12-09
---

# Hardness

[Block Condition Type](../block_condition_types.md)

Checks the hardness value of the block.

Type ID: `origins:hardness`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the hardness value of the block is compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value to compare the hardness value of the block to.


### Examples

```json
"block_condition": {
    "type": "origins:hardness",
    "comparison": "==",
    "compare_to": 1.5
}
```

This example will check if the block is as hard as Stone.
