---
title: Set Block
date: 2021-04-05
---
# Set Block

[Block Action](../block_actions.md).

Overwrites the block at the targeted position with the default state of another one.

Type ID: `origins:set_block`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block` | [Identifier](../data_types/identifier.md) | | The ID of the block to place.

### Example

```json
"block_action": {
  "type": "origins:set_block",
  "block": "minecraft:coal_ore"
}
```

This action sets the block at the position of the action to a coal ore.
