---
title: Block In Radius
date: 2021-04-04
---
# Block In Radius

[Entity Condition](../entity_conditions.md).

Checks whether the player has a specified number of blocks that match a specified block condition in a specified radius. The radius originates at the player's lower body block position.

Type ID: `origins:block_in_radius`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](../block_conditions.md) | |  The block condition which is applied to the block at the player's feet.
`radius` | [Integer](../data_types/integer.md) | |  The radius to check blocks in.
`shape` | [String](../data_types/string.md) | `"cube"` | Whether to check in a cube- or a star-shaped form. Either `"cube"` or `"star"`.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | How the number of blocks in the radius which fulfill `block_condition` should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` | The value to compare the number to.

### Example:
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
This example checks for 4 or more blocks that is inside the [`#origins:natural_stone`](https://github.com/apace100/origins-fabric/blob/master/src/main/resources/data/origins/tags/blocks/natural_stone.json) block tag (`data\origins\tags\blocks\natural_stone.json`) within a 1 block radius of a player.