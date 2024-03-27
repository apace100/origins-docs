---
title: Harvest Level (Item Condition Type)
date: 2021-04-05
---

# Harvest Level

[Item Condition Type](../item_condition_types.md)

Checks whether the material of the item has a certain harvest level value. Refer to [Minecraft Wiki: Tiers](https://minecraft.wiki/w/Tiers) for the harvest level of the materials (there it's called "mining level"). Items without a material are considered to have a harvest level of 0.

Type ID: `origins:harvest_level`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the harvest level of the material from the item stack should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | | The value at which the harvest level of the material from the item stack will be compared to.


### Examples

```json
"item_condition": {
    "type": "origins:harvest_level",
    "comparison": ">",
    "compare_to": 1
}
```

This example checks if the item has a harvest level higher than 1, which is the value for stone tools.
