---
title: Target Action (Bi-entity Action Type)
date: 2021-10-07
---

# Target Action

[Bi-entity Action Type](../bientity_action_types.md)

Executes an [Entity Action Type](../entity_action_types.md) on the target entity.

Type ID: `origins:target_action`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Entity Action Type](../entity_action_types.md) | | The entity action type to execute on the target entity.


### Examples

```json
"bientity_action": {
    "type": "origins:target_action",
    "action": {
        "type": "origins:set_on_fire",
        "duration": 5
    }
}
```

This exampel will set the target entity on fire for 5 seconds.
