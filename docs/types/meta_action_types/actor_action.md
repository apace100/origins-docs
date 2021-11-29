---
title: Actor Action (Meta Action Type)
date: 2021-10-07
---

# Actor Action

[Meta Action Type](../meta_action_types.md)

Executes an [Entity Action Type](../entity_action_types.md) on the actor entity.

Type ID: `origins:actor_action`

!!! note

    **Only available as a [Bi-entity Action Type](../bientity_action_types.md).**


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Entity Action Type](../entity_action_types.md) | | The entity action type to execute on the actor entity.


### Examples

```json
"bientity_action": {
    "type": "origins:actor_action",
    "action": {
        "type": "origins:set_on_fire",
        "duration": 5
    }
}
```

This example will set the actor entity on fire for 5 seconds.
