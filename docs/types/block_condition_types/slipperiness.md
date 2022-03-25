---
title: Slipperness (Block Condition Type)
date: 2021-12-09
---

# Slipperiness

[Block Condition Type](../block_condition_types.md)

Checks the slipperiness value of the block.

Type ID: `apoli:slipperiness`

### Fields

| Field        | Type                                      | Default | Description                                                                            |
| ------------ | ----------------------------------------- | ------- | -------------------------------------------------------------------------------------- |
| `comparison` | [Comparison](../data_types/comparison.md) |         | Determines how the slipperiness value of the block is compared to the specified value. |
| `compare_to` | [Float](../data_types/float.md)           |         | The value to compare the slipperiness value of the block to.                           |

### Examples

```json
"block_condition": {
    "type": "apoli:slipperiness",
    "comparison": "<=",
    "compare_to": 0.98
}
```

This example will check if the block has the same slipperiness of an Ice (or Packed Ice) block.
