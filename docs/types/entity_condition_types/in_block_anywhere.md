---
title: In Block Anywhere (Entity Condition Type)
date: 2021-04-04
---

# In Block Anywhere

[Entity Condition Type](../entity_condition_types.md)

Checks how many blocks are overlapping with the entity's eyes or feet.

Type ID: `origins:in_block_anywhere`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | |  The block condition type which blocks need to fulfill in order to count for this condition.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` |  How the number of blocks which overlap and fulfill block_condition should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` |  The value to compare the number to.


### Examples

```json
"condition": {
    "type": "origins:in_block_anywhere",
    "block_condition": {
        "type": "origins:in_tag",
        "tag": "minecraft:flowers"
    },
    "comparison": ">",
    "compare_to": 1
}
```

This example will check if the entity is currently inside a two-block tall foliage block that belongs in the `#minecraft:flowers` (`data\minecraft\tags\blocks\flowers.json`) block tag. An example is the rose bush block.
