---
title: Modify Food (Power Type)
date: 2021-04-06
---
# Modify Food

[Power Type](../power_types.md).

Modifies the food level and saturation gain when a player eats specific food items and optionally allows executing an [Entity Action](../entity_actions.md) on the eater.

Type ID: `origins:modify_food`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If set, the modifiers will only apply to food items which satisfy this condition.
`food_modifier` | [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If set, this modifier will apply to the food amount gained by eating.
`food_modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If set, these modifiers will apply to the food amount gained by eating.
`saturation_modifier` | [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If set, this modifier will apply to the saturation gained by eating.
`saturation_modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If set, these modifiers will apply to the saturation gained by eating.
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the entity eating this item.


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
This power will add 1 and a half shanks of hunger, and 1 saturation point if a player eats a dried kelp.