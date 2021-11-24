---
title: Target Condition (Meta Condition Type)
date: 2021-10-07
---

# Target Condition

[Meta Condition Type](../meta_condition_types.md)

Checks for an entity condition on the target entity.

Type ID: `origins:target_condition`

!!! note

	**Only available as a [Bi-entity Condition](../bientity_conditions.md).**

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Entity Condition](../entity_conditions.md) | | The condition to check for on the target entity.

### Example

```json
"bientity_condition": {
    "type": "origins:target_condition",
    "condition": {
       "type": "origins:tamed"
    }
}
```

This checks if the targetted entity is a tamable, and tamed mob.
