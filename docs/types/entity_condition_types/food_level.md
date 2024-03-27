---
title: Food Level (Entity Condition Type)
date: 2021-04-04
---

# Food Level

[Entity Condition Type](../entity_condition_types.md)

Checks the entity's food level (chicken legs / hunger meter / whatever you wanna call it). The food level is in the range of 0 to 20.

Type ID: `origins:food_level`

!!! note

    **This entity condition type will only work on players.**


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the food level of the player should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value at which the food level of the player will be compared to.


### Examples

```json
"condition": {
    "type": "origins:food_level",
    "comparison": "==",
    "compare_to": 0
}
```

This example will check if the player have 0 hunger shanks (or 0 food points).
