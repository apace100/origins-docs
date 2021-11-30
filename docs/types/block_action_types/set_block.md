---
title: Set Block (Block Action Type)
date: 2021-04-05
---

# Set Block

[Block Action Type](../block_action_types.md)

Overwrites the block at the targeted position with the default state of another one.

Type ID: `origins:set_block`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the block to place.


### Examples

```json
"block_action": {
    "type": "origins:set_block",
    "block": "minecraft:coal_ore"
}
```

This example will set a Coal Ore block at the position of the block action type.
