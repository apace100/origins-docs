---
title: Power Count (Item Condition Type)
date: 2023-02-26
---

#   Power Count

[Item Condition Type](../item_condition_types.md)

Checks how many powers are embedded in the item.

Type ID: `origins:power_count`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`slot` | [String](../data_types/string.md) | _optional_ | If specified, this will check how many powers are assigned to this equipment slot. Accepts one of `"head"`, `"chest"`, `"legs"`, `"feet"`, `"mainhand"` or `"offhand"`.
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the amount of powers embedded in the item stack should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value at which the amount of powers embedded in the item stack will be compared to.


### Examples

```json
"item_condition": {
    "type": "origins:power_count",
    "comparison": ">",
    "compare_to": 0
}
```

This example will check if the item has more than 0 powers embedded in it.
<br>

```json
"item_condition": {
    "type": "origins:power_count",
    "slot": "mainhand",
    "comparison": "<",
    "compare_to": 10
}
```

This example will check if the item has less than 10 powers embedded in it.
