---
title: Modify Food (Power Type)
date: 2021-04-06
---

# Modify Food

[Power Type](../power_types.md)

Executes an entity action and modifies the food and saturation level gain of a food item when a player that has the power eats food item.

Type ID: `origins:modify_food`

!!! note

    The actual food saturation level of the food item is determined by the `food * saturation * 2` formula. If you are going to refer to the [Minecraft Fandom Wiki: Food (Nourishment value)](https://minecraft.fandom.com/wiki/Food#Nourishment_value)' page for the saturation value of the food item, you would have to divide the value by 2.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If specified, the specified modifier(s) will only apply to food items that fulfills this condition.
`food_modifier` | [Attribute Modifiers](../types/data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to the food amount gained by eating a food item.
`food_modifiers` | [Array](../types/data_types/array.md) of [Attribute Modifiers](../types/data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the food amount gained by eating a food item.
`saturation_modifier` | [Attribute Modifiers](../types/data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to the saturation amount gained by eating a food item.
`saturation_modifiers` | [Array](../types/data_types/array.md) of [Attribute Modifiers](../types/data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the saturation amount gained by eating a food item.
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If specified, this action will be executed on the player that has ate an item.
`always_edible` | [Boolean](../types/data_types/boolean.md) | `false` | Determines whether a food item can be eaten regardless of the player's hunger bar being full.


### Example
```json
{
    "type": "origins:modify_food",
    "item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:dried_kelp"
        }
    },
    "food_modifier": {
        "name": "Increased food points",
        "operation": "addition",
        "value": 3.0
    },
    "saturation_modifier": {
        "name": "Increased saturation points",
        "operation": "addition",
        "value": 1
    }
}
```
This power will add 1 and a half shanks of hunger, and 1 saturation point if a player eats a dried kelp, totalling to 2 shanks of hunger (4 hunger points) and 6.4 saturation points.