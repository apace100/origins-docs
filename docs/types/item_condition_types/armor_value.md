---
title: Armor Value (Item Condition Type)
date: 2021-04-05
---

# Armor Value

[Item Condition Type](../item_condition_types.md)

Checks whether the item has a certain armor value. Non-armor items are considered as having an armor value of 0.

Type ID: `origins:armor_value`

!!! note

    You can visit these pages to get the armor values for each armor item piece:

    * [Helmet](https://minecraft.fandom.com/wiki/Helmet#Defense_points)
    * [Chestplate](https://minecraft.fandom.com/wiki/Chestplate#Defense_points)
    * [Leggings](https://minecraft.fandom.com/wiki/Leggings#Defense_points)
    * [Boots](https://minecraft.fandom.com/wiki/Boots#Defense_points)


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | |  How to compare the item's armor value to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | Which value to compare the item's armor value to.


### Examples

```json
"item_condition": {
    "type": "origins:armor_value",
    "comparison": ">",
    "compare_to": 3
}
```

This example will check if the armor item (in this context, a chestplate) has a higher armor value than 3, which is the armor value for the leather chestplate armor item.
