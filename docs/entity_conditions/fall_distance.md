---
title: Fall Distance
date: 2021-04-04
---
# Fall Distance

[Entity Condition](../entity_conditions.md).

Used to check how much distance (in blocks) the player has fallen. Note that this is 0 if the player has slow falling.

Type ID: `origins:fall_distance`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the fall distance should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value to compare the fall distance to.

### Example
```json
"condition": {
    "type": "origins:fall_distance",
    "comparison": ">=",
    "compare_to": 4
}
```
This example checks if the player has been falling for 4 or more blocks.