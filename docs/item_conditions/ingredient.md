---
title: Ingredient (Condition)
date: 2021-04-05
---
# Ingredient

[Item Condition](../item_conditions.md).

Checks whether the item matches a specified [Item Condition](../item_conditions.md). Essentially, checking either for the item ID or whether the item is in a specified tag.

Type ID: `origins:ingredient`

### Fields:

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
This example checks if the item is a `minecraft:egg` item.


```json
"item_condition": {
    "type": "origins:ingredient",
    "ingredient": {
        "tag": "minecraft:flowers"
    }
}
```
This example checks if the item is inside the `#minecraft:flowers` item tag. (`data\minecraft\tags\items\flowers.json`)