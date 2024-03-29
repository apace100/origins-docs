---
title: Height (Block Condition Type)
date: 2021-04-05
---

# Height

[Block Condition Type](../block_condition_types.md)

Compares the Y position of the block to a value.

Type ID: `origins:height`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the Y position of the block should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value at which the Y position of the block will be compared to.


### Examples

```json
"block_condition": {
    "type": "origins:height",
    "comparison": "<=",
    "compare_to": 11
}
```

This example will check if the block is within Y=11 or lower.
