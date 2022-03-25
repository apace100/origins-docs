---
title: Amount (Item Condition Type)
date: 2021-10-02
---

# Amount

[Item Condition Type](../item_condition_types.md)

Checks the amount of the item.

Type ID: `apoli:amount`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how to compare the number of items in this stack to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value to compare the item's count value to.


### Examples

```json
"item_condition": {
    "type": "apoli:amount",
    "comparison": ">=",
    "compare_to": 10
}
```

This example will check if the item has a count of 10 or more.
