---
title: Hardness (Block Condition Type)
date: 2021-12-09
---

# Hardness

[Block Condition Type](../block_condition_types.md)

Checks the hardness value of the block.

Type ID: `origins:hardness`


!!! note

    A block's hardness value is used for determining how long it takes to break the block. If you want to see the hardness values of each block, you can refer to [Minecraft Wiki: Breaking (Blocks by hardness)](https://minecraft.wiki/w/Breaking#Blocks_by_hardness) page.


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
