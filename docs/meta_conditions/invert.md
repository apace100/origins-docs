---
title: Invert (Meta Condition)
date: 2021-10-07
---

# Invert

[Meta Condition](../meta_conditions.md)

Swaps the context of the target entity and the actor entity.

Type ID: `origins:invert`

!!! note

	**Only available as a [Bi-entity Condition](../bientity_conditions.md).**

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Bi-entity Condition](../bientity_conditions.md) | | The bi-entity condition to check which will have its 'target' and 'actor' contexts swapped.

### Example

```json
"bientity_condition": {
    "type": "origins:invert",
    "condition": {
        "type": "origins:can_see"
    }
}
```

This will check if the target of the action can see the actor, as the roles are swapped.
