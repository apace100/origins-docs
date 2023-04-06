---
title: Ingredient (Item Condition Type)
date: 2021-04-05
---

# Ingredient

[Item Condition Type](../item_condition_types.md)

Checks whether the item matches the specified [ingredient](../data_types/ingredient.md). Essentially, checking either for the item ID or whether the item is in a specified tag.

Type ID: `origins:ingredient`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`ingredient` | [Ingredient](../data_types/ingredient.md) | |  The ingredient this item must match to pass the check.


### Examples

```json
"item_condition": {
    "type": "origins:ingredient",
    "ingredient": {
        "item": "minecraft:egg"
    }
}
```

This example will check if the item is a `minecraft:egg` item.
<br>

```json
"item_condition": {
    "type": "origins:ingredient",
    "ingredient": {
        "tag": "minecraft:flowers"
    }
}
```

This example will check if the item is included in the `#minecraft:flowers` (`data/minecraft/tags/items/flowers.json`) item tag.
<br>

```json
"item_condition": {
    "type": "origins:ingredient",
    "ingredient": [
        {
            "tag": "minecraft:planks"
        },
        {
            "item": "minecraft:oak_log"
        }
    ]
}
```

This example will check if the item is included in the `#minecraft:planks` (`data/minecraft/tags/items/planks.json`) item tag or if the item is a `minecraft:oak_log` item.
