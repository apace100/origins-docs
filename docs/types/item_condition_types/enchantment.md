---
title: Enchantment (Item Condition Type)
date: 2021-04-05
---

# Enchantment

[Item Condition Type](../item_condition_types.md)

Checks the level of a certain enchantment, or the amount of individual enchantments on the item.

Type ID: `origins:enchantment`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`enchantment` | [Identifier](../data_types/identifier.md) | _optional_ | ID of the enchantment of interest, e.g. `minecraft:protection`. If not set, amount of enchantments will be checked instead.
`use_modifications` | [Boolean](../data_types/boolean.md) | `true` | Determines whether to account for enchantments that were added/modified by unnatural means (e.g: via the [Modify Enchantment Level (Power Type)](../power_types/modify_enchantment_level.md).)
`comparison` | [Comparison](../data_types/comparison.md) | | How to compare the enchantment level, or the amount of enchantments, to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value to compare the enchantment level or amount against.


### Examples

```json
"item_condition": {
    "type": "origins:enchantment",
    "enchantment": "minecraft:fortune",
    "comparison": "==",
    "compare_to": 3
}
```

This example will check if the item has the Fortune III enchantment.

```json
"item_condition": {
    "type": "origins:enchantment",
    "comparison": ">=",
    "compare_to": 3
}
```

This example will check if the item has 3 or more enchantments.
