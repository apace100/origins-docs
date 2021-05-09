---
title: Food Level
date: 2021-04-04
---
# Food Level

[Entity Condition](../entity_conditions.md).

Checks the player's food level (chicken legs / hunger meter / whatever you wanna call it). The food level is in the range of 0 to 20.

Type ID: `origins:food_level`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the food level should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | Which value the food level should be compared to.

### Example:
```json
"condition": {
    "type": "origins:food_level",
    "comparison": "==",
    "compare_to": 0
}
```
This example checks if the player have 0 hunger shanks (or 0 food points).