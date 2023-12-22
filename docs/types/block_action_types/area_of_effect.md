---
title: Area of Effect (Block Action Type)
date: 2023-05-21
---

# Area of Effect

[Block Action Type](../block_action_types.md)

Executes the provided [Block Action Type](../block_action_types.md) on all blocks within the specified radius and shape.

Type ID: `origins:area_of_effect`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`radius` | [Integer](../data_types/integer.md) | `16` | Determines the radius of the area.
`shape` | [Shape](../data_types/shape.md) | `"cube"` | Determines the shape of the area.
`block_action` | [Block Action Type](../block_action_types.md) | | The block action to execute on the blocks within the specified radius.
`block_condition` | [Block Condition Type](../block_condition_types.md) | *optional* | If specified, the specified block action will only be executed on blocks that fulfill this block condition.


### Examples

```json
"block_action": {
    "type": "origins:area_of_effect",
    "radius": 16,
    "shape": "cube",
    "block_action": {
        "type": "origins:modify_block_state",
        "property": "waterlogged",
        "value": false
    }
}
```

This example will make all waterloggable blocks not waterlogged within 16 blocks radius with a shape of a cube.
<br>

```json
"block_action": {
    "type": "origins:area_of_effect",
    "radius": 4,
    "shape": "star",
    "block_action": {
        "type": "origins:set_block",
        "block": "minecraft:air"
    },
    "block_condition": {
        "type": "origins:in_tag",
        "tag": "minecraft:dragon_immune",
        "inverted": true
    }
}
```

This example will replace all blocks that aren't included in the `#minecraft:dragon_immune` block tag with air within a 4 blocks radius with a shape of a diamond.
