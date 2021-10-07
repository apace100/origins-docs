---
title: Constant (Bi-Entity Condition)
date: 2021-10-06
---
# Distance

[Meta Condition](../meta_conditions.md).

This condition is either always fulfilled or always not fulfilled. Mainly added as a backup in case a condition isn't optional in some place.

Type ID: `origins:constant`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How to compare the distance against the specified value.
`compare_to` | [Float](../data_types/float.md) | | The distance (in blocks) to compare the distance between the actor and target to.

### Example

```json
"condition": {
  "type": "origins:distance",
  "comparison": "<=",
  "compare_to": 30
}
```
This condition checks if the target is at most 30 blocks away from the actor.
