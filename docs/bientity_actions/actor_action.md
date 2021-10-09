---
title: Actor Action (Bi-Entity Action)
date: 2021-10-07
---
# Actor Action

[Bi-Entity Action](../bientity_actions.md).

Executes an entity action on the actor entity.

Type ID: `origins:actor_action`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Entity Action](../entity_actions.md) | | The action to execute on the actor entity.

### Example

```json
"bientity_action": {
    "type": "origins:actor_action",
    "action": {
        "type": "origins:set_on_fire",
        "duration": 5
    }
}
```

This will set the actor of the action on fire for 5 seconds.
