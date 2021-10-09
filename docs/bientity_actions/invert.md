---
title: Invert (Bi-Entity Action)
date: 2021-10-07
---
# Invert

[Bi-Entity Action](../bientity_actions.md).

Swaps the context of the target entity and the actor entity.

Type ID: `origins:invert`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | | The bi-entity action to execute which will have its 'target' and 'actor' contexts swapped.

### Example

```json
"bientity_action": {
    "type": "origins:inverted",
    "action": {
        "type": "origins:mount"
    }
}
```

This will make the target of the action mount the actor, as the roles are swapped.
