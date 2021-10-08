---
title: Actor Condition (Bi-Entity Condition)
date: 2021-10-07
---
# Actor Condition

[Bi-Entity Condition](../bientity_conditions.md).

Checks for an entity condition on the acting entity.

Type ID: `origins:actor_condition`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_condition` | [Entity Condition](../entity_conditions.md) | | The condition to check for on the acting entity.

### Example

```json
"bientity_condition": {
    "type": "origins:actor_condition",
    "entity_condition": {
       "type": "origins:tamed"
    }
}
```

This checks if the acting entity is a tamable, and tamed mob.
