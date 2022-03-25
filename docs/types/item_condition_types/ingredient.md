---
title: Ingredient (Item Condition Type)
date: 2021-04-05
---

# Ingredient

[Item Condition Type](../item_condition_types.md)

Checks whether the item matches a specified [Item Condition Type](../item_condition_types.md). Essentially, checking either for the item ID or whether the item is in a specified tag.

Type ID: `apoli:ingredient`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`ingredient` | [Ingredient](../data_types/ingredient.md) | |  The ingredient this item must match to pass the check.


### Examples

```json
"item_condition": {
    "type": "apoli:ingredient",
    "ingredient": {
        "item": "minecraft:egg"
    }
}
```

This example will check if the item is a `minecraft:egg` item.
<br>

```json
"item_condition": {
    "type": "apoli:ingredient",
    "ingredient": {
        "tag": "minecraft:flowers"
    }
}
```

This example will check if the item is inside the `#minecraft:flowers` item tag. (`data\minecraft\tags\items\flowers.json`)
