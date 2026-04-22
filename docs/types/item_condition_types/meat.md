---
title: Meat (Item Condition Type)
date: 2021-04-05
---

# Meat

[Item Condition Type](../item_condition_types.md)

Checks whether the item is considered meat by Minecraft (usable for breeding wolves).

Type ID: `origins:meat`


!!! danger

    This item condition type has been <span style="color:darkred"><b>removed</b></span> in Origins 1.13.0 due to the removal of the meat property from items. 
    
    **Please use the [Ingredient (Item Condition Type)](ingredient.md) to check if the item is in the `#minecraft:meat` or `#minecraft:wolf_food` item tag instead.**


### Fields

_None._


### Examples

```json
"item_condition": {
    "type": "origins:meat"
}
```

This example will check if the item is considered meat by Minecraft.
