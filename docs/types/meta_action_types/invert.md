---
title: Invert (Meta Action Type)
date: 2021-10-07
---

# Invert

[Meta Action Type](../meta_action_types.md)

Swaps the context of the target entity and the actor entity.

Type ID: `origins:invert`

!!! note

    **Only available as a [Bi-entity Action](../bientity_actions.md).**

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`action` | [Bi-entity Action](../bientity_actions.md) | | The bi-entity action to execute which will have its 'target' and 'actor' contexts swapped.

### Example

```json
"bientity_action": {
    "type": "origins:invert",
    "action": {
        "type": "origins:mount"
    }
}
```

This will make the target of the action mount the actor, as the roles are swapped.
