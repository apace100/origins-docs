---
title: Enchantment (Condition)
date: 2021-04-05
---
# Enchantment

[Item Condition](../item_conditions.md).

Checks the level of a certain enchantment on the item.

Type ID: `origins:enchantment`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`enchantment` | [String](../data_types/string.md) | |  ID of the enchantment of interest, e.g. `minecraft:protection`.
`comparison` | [Comparison](../data_types/comparison.md) | |  How to compare the enchantment level the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value to compare the enchantment level against.

### Example
```json
"item_condition": {
    "type": "origins:enchantment",
    "enchantment": "minecraft:fortune",
    "comparison": "==",
    "compare_to": 3
}
```
This example checks if the item has the Fortune III enchantment.