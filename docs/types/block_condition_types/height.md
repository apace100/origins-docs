---
title: Height (Block Condition Type)
date: 2021-04-05
---

# Height

[Block Condition Type](../block_condition_types.md)

Compares the Y position of the block to a value.

Type ID: `apoli:height`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the Y position of the block should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value to compare the Y position of the block to.


### Examples

```json
"block_condition": {
    "type": "apoli:height",
    "comparison": "<=",
    "compare_to": 11
}
```

This example will check if the block is within Y=11 or lower.
