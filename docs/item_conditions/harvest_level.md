---
title: Harvest Level (Condition)
date: 2021-04-05
---
# Harvest Level

[Item Condition](../item_conditions.md).

Checks whether the material of the item has a certain harvest level value. Refer to [this page on the Minecraft Wiki](https://minecraft.fandom.com/wiki/Tiers) for the harvest level of the materials (there it's called "mining level"). Items without a material are considered to have a harvest level of 0.

Type ID: `origins:harvest_level`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | |  _How to compare the item's harvest level to the specified value._
`compare_to` | [Integer](../data_types/integer.md) | | _Which value to compare the item's harvest level to._
