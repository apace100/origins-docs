---
title: Armor Value (Condition)
date: 2021-04-05
---
# Armor Value

[Item Condition](../item_conditions.md).

Checks whether the item has a certain armor value. Non-armor items are considered as having an armor value of 0.

Type ID: `origins:armor_value`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | |  _How to compare the item's armor value to the specified value._
`compare_to` | [Integer](../data_types/integer.md) | | _Which value to compare the item's armor value to._
