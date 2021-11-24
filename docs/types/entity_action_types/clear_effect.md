---
title: Clear Effect (Entity Action Type)
date: 2021-04-05
---

# Clear Effect

[Entity Action Type](../entity_action_types.md)

Removes one specific type of status effect, or all status effects, from a living entity.

Type ID: `origins:clear_effect`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the effect with this ID will be cleared. If not specified, all effects will be cleared.

### Example
```json
"entity_action": {
    "type": "origins:clear_effect",
    "effect": "minecraft:poison"
}
```
This action clears a poison effect from an entity.
