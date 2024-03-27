---
title: Distance (Bi-entity Condition Type)
date: 2021-10-06
---

# Distance

[Bi-entity Condition Type](../bientity_condition_types.md)

Checks the distance between the target entity and the actor entity.

Type ID: `origins:distance`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the distance (in blocks) between the actor and target entities should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value at which the distance (in blocks) between the actor and target entities will be compared to.


### Examples

```json
"bientity_condition": {
    "type": "origins:distance",
    "comparison": "<=",
    "compare_to": 30
}
```

This example will check if the target entity is within 30 blocks radius relative from the actor entity.
