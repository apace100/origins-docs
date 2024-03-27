---
title: Fuel (Item Condition Type)
date: 2023-10-09
---

# Fuel

[Item Condition Type](../item_condition_types.md)

Checks whether the item is considered as fuel.

Type ID: `origins:fuel`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | `">"` | Determines how the fuel time value (in ticks) of the item stack should be compared to a specific value.
`compare_to` | [Integer](../data_types/integer.md) | `0` | The value at which the fuel time value (in ticks) of the item stack will be compared to.


### Examples

```json
"item_condition": {
    "type": "origins:fuel",
    "comparison": ">=",
    "compare_to": 10
}
```

This example will check if the item fuel time value of 10 or more.
