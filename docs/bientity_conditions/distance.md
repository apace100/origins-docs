---
title: Distance (Bi-entity Condition)
date: 2021-10-06
---
# Distance

[Bi-Entity Condition](../bientity_conditions.md).

Checks the distance between the target entity and the actor entity.

Type ID: `origins:distance`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How to compare the distance against the specified value.
`compare_to` | [Float](../data_types/float.md) | | The distance (in blocks) to compare the distance between the actor and target to.

### Example

```json
"bientity_condition": {
  "type": "origins:distance",
  "comparison": "<=",
  "compare_to": 30
}
```
This condition checks if the target is at most 30 blocks away from the actor.
