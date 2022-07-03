---
title: Relative Durability (Item Condition Type)
date: 2022-07-03
---

#   Relative Durability

[Item Condition Type](../item_condition_types.md)

Checks the current and the percentage durability value of the item.

Type ID: `origins:relative_durability`

!!! note

    The percentage of the durability value can be calculated with the `currentDurability / maxDurability` formula.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the relative durability value of the item should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value which the durability value of the item should be compared to.


### Examples

```json
"item_condition": {
    "type": "origins:relative_durability",
    "comparison": ">=",
    "compare_to": 0.9
}
```

This example will check if the item has a 90% durability or greater.
