---
title: Amount (Item Condition Type)
date: 2021-10-02
---

# Amount

[Item Condition Type](../item_condition_types.md)

Checks the amount of the item in the item stack.

Type ID: `origins:amount`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the amount of the item in the item stack should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value at which the amount of the item in the item stack will be compared to.


### Examples

```json
"item_condition": {
    "type": "origins:amount",
    "comparison": ">=",
    "compare_to": 10
}
```

This example will check if there are 10 or more items in the item stack.
