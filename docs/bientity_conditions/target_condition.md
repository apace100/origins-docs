---
title: Target Condition (Bi-Entity Condition)
date: 2021-10-07
---
# Target Condition

[Bi-Entity Condition](../bientity_conditions.md).

Checks for an entity condition on the target entity.

Type ID: `origins:target_condition`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_condition` | [Entity Condition](../entity_conditions.md) | | The condition to check for on the target entity.

### Example

```json
"bientity_condition": {
    "type": "origins:target_condition",
    "entity_condition": {
       "type": "origins:tamed"
    }
}
```

This checks if the targetted entity is a tamable, and tamed mob.
