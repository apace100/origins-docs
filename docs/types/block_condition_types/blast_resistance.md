---
title: Blast Resistance (Block Condition Type)
date: 2021-12-09
---

# Blast Resistance

[Block Condition Type](../block_condition_types.md)

Checks the blast resistance value of the block.

Type ID: `origins:blast_resistance`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the blast resistance of the block should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value at which the blast resistance value of the block will be compared to.


### Examples

```json
"block_condition": {
    "type": "origins:blast_resistance",
    "comparison": ">=",
    "compare_to": 1200
}
```

This example will check if the blast resistance value of the block is that of an Obsidian block or greater.
