---
title: Invert (Bi-Entity Action)
date: 2021-10-07
---
# Invert

[Bi-Entity Action](../bientity_actions.md).

Inverts a Bi-Entity Action, switching the Actor and Target.

Type ID: `origins:invert`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`bientity_action` | [Action](../bientity_actions.md) | | The action which will be executed.

### Example

```json
"bientity_action": {
    "type": "origins:inverted",
    "bientity_action": {
        "type": "origins:mount"
    }
}
```

This will make the target of the action mount the actor, as the roles are swapped.
