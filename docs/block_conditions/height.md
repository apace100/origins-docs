---
title: Height (Condition)
date: 2021-04-05
---
# Height

[Block Condition](../block_conditions.md).

Compares the y position of the block to a value.

Type ID: `origins:height`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the Y position of the block should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value to compare the Y position of the block to.

### Example:
```json
"block_condition": {
    "type": "origins:height",
    "comparison": "<=",
    "compare_to": 11
}
```
This example checks if the block is within Y=11 or lower.