---
title: Area of Effect (Block Action Type)
date: 2023-05-21
---

# Area of Effect

[Block Action Type](../block_action_types.md)

Executes the provided [Block Action Type](../block_action_types.md) on all blocks within the specified radius and shape.

Type ID: `origins:area_of_effect`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_action` | [Block Action Type](../block_action_types.md) | | The action to apply to the blocks.
`radius` | [Integer](../data_types/integer.md) | `16` | Determines the radius of the area to execute the action on.
`shape` | [String](../data_types/string.md) | `"cube"` | The shape in which to affect blocks, accepts `cube`, `star` or `sphere`.
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the specified action will only apply to blocks that fulfill this condition.


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

This example will replace all blocks that aren't included in the `#minecraft:dragon_immune` block tag with air within a 4 blocks radius with a shape of a star.