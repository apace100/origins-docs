---
title: Block Action At (Entity Action Type)
date: 2021-04-05
---

# Block Action At

[Entity Action Type](../entity_action_types.md)

Executes a [Block Action Type](../block_action_types.md) at the position of the entity.

Type ID: `origins:block_action_at`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_action` | [Block Action Type](../block_action_types.md) |  | The block action type to execute.


### Examples

```json
"entity_action": {
    "type": "origins:block_action_at",
    "block_action": {
        "type": "origins:set_block",
        "block": "minecraft:sand"
    }
}
```

This example will execute a [Set Block (Block Action Type)](../block_action_types/set_block.md) that would set a Sand block at the entity's feet.
