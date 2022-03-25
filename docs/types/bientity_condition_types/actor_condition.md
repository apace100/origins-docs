---
title: Actor Condition (Bi-entity Condition Type)
date: 2021-10-07
---

# Actor Condition

[Bi-entity Condition Type](../bientity_condition_types.md)

Checks for an [Entity Condition Type](../entity_condition_types.md) on the actor entity.

Type ID: `apoli:actor_condition`

### Fields

| Field       | Type                                                  | Default | Description                                                  |
| ----------- | ----------------------------------------------------- | ------- | ------------------------------------------------------------ |
| `condition` | [Entity Condition Type](../entity_condition_types.md) |         | The entity condition type to check for on the acting entity. |

### Examples

```json
"bientity_condition": {
    "type": "apoli:actor_condition",
    "condition": {
       "type": "apoli:tamed"
    }
}
```

This example will check if the actor entity is a tamable and tamed mob.
