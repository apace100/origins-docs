---
title: Modify Food (Power Type)
date: 2021-04-06
---

# Modify Food

[Power Type](../power_types.md)

Executes an [Entity Action Type](../entity_action_types.md) and modifies the food and saturation level gain of a food item when a player that has the power eats food item.

Type ID: `apoli:modify_food`

!!! note

    The actual food saturation level of the food item is determined by the `food * saturation * 2` formula. If you are going to refer to the [Minecraft Fandom Wiki: Food (Nourishment value)](https://minecraft.fandom.com/wiki/Food#Nourishment_value)' page for the saturation value of the food item, you would have to divide the value by 2.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the specified actions and modifier(s) will only apply to food items that fulfills this condition.
`item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this item action type will be executed on the remaining item stacks that was consumed.
`replace_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item stack will replace the item stack that was consumed *after* consuming it.
`food_modifier` | [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to the food amount gained by eating a food item.
`food_modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the food amount gained by eating a food item.
`saturation_modifier` | [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to the saturation amount gained by eating a food item.
`saturation_modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the saturation amount gained by eating a food item.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player that has ate a food item.
`always_edible` | [Boolean](../data_types/boolean.md) | `false` | Determines whether a food item can be eaten regardless of the player's hunger bar being full.
`prevent_effects` | [Boolean](../data_types/boolean.md) | `false` | If set to `true`, prevent status effects from being applied.


### Examples

```json
{
    "type": "apoli:modify_food",
    "item_condition": {
        "type": "apoli:ingredient",
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

This example will add 1 and a half shanks of hunger, and 1 saturation point if a player eats a dried kelp, totalling to 2 shanks of hunger and 6.4 saturation points.
