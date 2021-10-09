---
title: Amount (Item Condition)
date: 2021-10-02
---
# Amount

[Item Condition](../item_conditions.md)

Checks the amount of the item.

Type ID: `origins:amount`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how to compare the number of items in this stack to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value to compare the item's count value to.

### Example
```json
"item_condition": {
    "type": "origins:amount",
    "comparison": ">=",
    "compare_to": 10
}
```
This example checks if the item has a count of 10 or more.