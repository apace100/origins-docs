---
title: Blast Resistance (Block Condition Type)
date: 2021-12-09
---

# Blast Resistance

[Block Condition Type](../block_condition_types.md)

Checks the blast resistance value of the block.

Type ID: `apoli:blast_resistance`

### Fields

| Field        | Type                                      | Default | Description                                                                          |
| ------------ | ----------------------------------------- | ------- | ------------------------------------------------------------------------------------ |
| `comparison` | [Comparison](../data_types/comparison.md) |         | Determines how the blast resistance of the block is compared to the specified value. |
| `compare_to` | [Float](../data_types/float.md)           |         | The value to compare the blast resistance of the block to.                           |

### Examples

```json
"block_condition": {
    "type": "apoli:blast_resistance",
    "comparison": ">=",
    "compare_to": 1200
}
```

This example will check if the blast resistance value of the block is that of an Obsidian block or greater.
