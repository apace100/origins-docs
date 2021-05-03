---
title: Block Action At (Action)
date: 2021-04-05
---
# Block Action At

[Entity Action](../entity_actions.md).

Executes a [Block Action](../block_actions.md) at the position of the entity.

Type ID: `origins:block_action_at`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_action` | [Block Action](../block_actions.md) |  | The block action to execute.

### Example
```json
"entity_action": {
  "type": "origins:block_action_at",
  "block_action": {
    "type": "origins:set_block",
    "block": "minecraft:sand"
  }
}
```
This action will set the block at the position of the entity (usually at their feet) to a sand block.
