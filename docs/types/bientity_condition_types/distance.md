---
title: Distance (Bi-entity Condition Type)
date: 2021-10-06
---

# Distance

[Bi-entity Condition Type](../bientity_condition_types.md)

Checks the distance between the target entity and the actor entity.

Type ID: `apoli:distance`

### Fields

| Field        | Type                                      | Default | Description                                                                       |
| ------------ | ----------------------------------------- | ------- | --------------------------------------------------------------------------------- |
| `comparison` | [Comparison](../data_types/comparison.md) |         | How to compare the distance against the specified value.                          |
| `compare_to` | [Float](../data_types/float.md)           |         | The distance (in blocks) to compare the distance between the actor and target to. |

### Examples

```json
"bientity_condition": {
    "type": "apoli:distance",
    "comparison": "<=",
    "compare_to": 30
}
```

This example will check if the target entity is within 30 blocks radius relative from the actor entity.
