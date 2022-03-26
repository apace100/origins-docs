---
title: Target Condition (Bi-entity Condition Type)
date: 2021-10-07
---

# Target Condition

[Bi-entity Condition Type](../bientity_condition_types.md)

Checks for an [Entity Condition Type](../entity_condition_types.md) on the target entity.

Type ID: `origins:target_condition`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Entity Condition Type](../entity_condition_types.md) | | The entity condition type to check for on the target entity.


### Examples

```json
"bientity_condition": {
    "type": "origins:target_condition",
    "condition": {
       "type": "origins:tamed"
    }
}
```

This example will check if the target entity is a tamable and a tamed mob.
