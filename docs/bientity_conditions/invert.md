---
title: Invert (Bi-Entity Action)
date: 2021-10-07
---
# Invert

[Bi-Entity Condition](../bientity_conditions.md).

Swaps the context of the target entity and the actor entity.

Type ID: `origins:invert`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`bientity_condition` | [Bi-entity Action](../bientity_conditions.md) | | The bi-entity condition to check which will have its 'target' and 'actor' contexts swapped.

### Example

```json
"bientity_condition": {
    "type": "origins:inverted",
    "bientity_condition": {
        "type": "origins:can_see"
    }
}
```

This will check if the target of the action can see the actor, as the roles are swapped.
