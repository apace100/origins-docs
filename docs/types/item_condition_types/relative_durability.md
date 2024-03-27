---
title: Relative Durability (Item Condition Type)
date: 2022-07-03
---

#   Relative Durability

[Item Condition Type](../item_condition_types.md)

Checks the current durability of the item relative to its max durability (in percentage.)

Type ID: `origins:relative_durability`

!!! note

    The relative durability of an item can be calculated with the `currentDurability / maxDurability` formula.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the relative durability of the item should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) |  | The value at which the relative durability of the item will be compared to.


### Examples

```json
"item_condition": {
    "type": "origins:relative_durability",
    "comparison": ">=",
    "compare_to": 0.9
}
```

This example will check if the item has a 90% durability or greater.
