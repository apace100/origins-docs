---
title: Target Action (Bi-Entity Action)
date: 2021-10-07
---
# Target Action

[Bi-Entity Action](../bientity_actions.md).

Executes an entity action on the target entity.

Type ID: `origins:target_action`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | | The action to execute on the target entity.

### Example

```json
"bientity_action": {
    "type": "origins:target_action",
    "entity_action": {
        "type": "origins:set_on_fire",
        "duration": 5
    }
}
```

This will set the target of the action on fire for 5 seconds.
