---
title: Harvest Level (Item Condition Type)
date: 2021-04-05
---

# Harvest Level

[Item Condition Type](../item_condition_types.md)

Checks whether the material of the item has a certain harvest level value. Refer to [Minecraft Wiki: Tiers](https://minecraft.wiki/w/Tiers) for the harvest level of the materials (there it's called "mining level"). Items without a material are considered to have a harvest level of 0.

Type ID: `origins:harvest_level`

!!! danger

    This item condition type has been <span style="color:darkred"><b>removed</b></span> in Origins 1.13.0 since items no longer have a harvest level property.
    <br>

    To replicate this, you'll need to create your own item tags for each tier (e.g: wood, stone, iron, diamond, netherite) and check if the item is in one of the said tags with [Ingredient (Item Condition Type)](ingredient.md).


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
