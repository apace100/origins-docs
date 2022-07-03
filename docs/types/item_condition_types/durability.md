---
title: Durability
date: 2022-07-03
---

#   Durability

[Item Condition Type](../item_condition_types.md)

Checks the current and absolute durability value of the item.

Type ID: `origins:durability`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the durability value of the item should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value which the durability value of the item should be compared to.


### Examples

```json
"item_condition": {
    "type": "origins:durability",
    "comparison": "<=",
    "compare_to": 100
}
```

This example will check if the item has a durability value of 100 or less.
