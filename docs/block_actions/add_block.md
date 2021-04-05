---
title: Add Block
date: 2021-04-05
---
# Add Block

[Block Action](../block_actions.md).

Adds a block at the specified action position. Adding means setting the block at the position, offset by the direction of the action.

Type ID: `origins:add_block`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block` | [Identifier](../data_types/identifier.md) | | The ID of the block to place.

### Example

```json
"block_action": {
  "type": "origins:add_block",
  "block": "minecraft:coal_ore"
}
```

This action sets the block at the position of the action, offset by the direction of the action, to a coal ore.
