---
title: Add Block (Block Action Type)
date: 2021-04-05
---

# Add Block

[Block Action Type](../block_action_types.md)

Adds a block at the specified action position. Adding means setting the block at the position, offset by the direction of the action.

Type ID: `origins:add_block`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the block to place.


### Examples

```json
"block_action": {
    "type": "origins:add_block",
    "block": "minecraft:coal_ore"
}
```

This example will add a Coal Ore block at the position of the block action type.
<br>

```json
"block_action": {
    "type": "origins:add_block",
    "block": "minecraft:chest[facing=north]"
}
```

This example will add a Chest block facing north at the position of the block action type.
