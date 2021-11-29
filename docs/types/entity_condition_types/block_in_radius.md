---
title: Block In Radius (Entity Condition Type)
date: 2021-04-04
---

# Block In Radius

[Entity Condition Type](../entity_condition_types.md)

Checks whether there is a specified number of blocks that fulfills the specified [Block Condition Type](../block_condition_types.md) within a specified radius relative to the entity's feet.

Type ID: `origins:block_in_radius`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | |  The block condition type to check for.
`radius` | [Integer](../data_types/integer.md) | | The radius to check the blocks that fulfills the specified block condition type within.
`shape` | [String](../data_types/string.md) | `"cube"` | Determines the shape of the radius. Accepts `"cube"` or `"star"`.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | How the amount of blocks within the specified radius which fulfills the specified block condition type should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` | The value to compare the amount to.


### Examples

```json
"condition": {
    "type": "origins:block_in_radius",
    "block_condition": {
        "type": "origins:in_tag",
        "tag": "origins:natural_stone"
    },
    "radius": 1,
    "shape": "cube",
    "comparison": ">=",
    "compare_to": 4
}
```

This example will check if 4 or more blocks that is included in the [`origins:natural_stone`](https://github.com/apace100/origins-fabric/blob/master/src/main/resources/data/origins/tags/blocks/natural_stone.json) (`data/origins/tags/blocks/natural_stone.json`) block tag is within a 1 block radius relative from the entity.