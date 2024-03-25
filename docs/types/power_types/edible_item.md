---
title: Edible Item (Power Type)
date: 2023-10-09
---

# Edible Item

[Power Type](../power_types.md)

Makes an item edible.

Type ID: `origins:edible_item`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player upon consuming an item.
`item_action`| [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item consumed by the player.
`result_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item that is given to the player as a result of consuming an item.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, will only make the item edible and the specified actions will only be executed if this condition is fulfilled by the item.
`food_component`| [Food Component](../data_types/food_component.md) |  | The food component that the item grants upon eating it.
[`result_stack`](## "Aliases: return_stack") | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item stack will be given to the player.
[`consume_animation`](## "Aliases: use_action") | [String](../data_types/string.md) | `"eat"` | Determines whether the action of consuming the item is considered "eating" (`"eat"`) or "drinking" (`"drink"`).
[`consume_sound`](## "Aliases: sound") | [Identifier](../data_types/identifier.md) |  | If specified, the sound event with this namespace and ID will be played when the item is eaten.
`consuming_time_modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | *optional* | If specified, this modifier will be applied on the maximum time the item is being consumed (in ticks).
`consuming_time_modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | *optional* | If specified, these modifiers will be applied on the the maximum time the item is being consumed (in ticks).
`priority` | [Integer](../data_types/integer.md) | `0` | Determines the priority of which the power will apply its modification to the item. Must be higher than 0 if the item is already edible.


### Examples

```json
{
    "type": "origins:edible_item",
    "item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:axolotl_bucket"
        }
    },
    "food_component": {
        "hunger": 4,
        "saturation": 1,
        "meat": true
    },
    "use_action": "eat",
    "result_stack": {
        "item": "minecraft:water_bucket",
        "amount": 1
    }
}
```

This example will grant the players the ability to eat axolotls in buckets. It will give 4 hunger shanks and 8 saturation (4 * 1 * 2), it also counts as meat. This returns a water bucket upon consumption and uses the eat action.
<br>


```json
{
    "type": "origins:edible_item",
    "item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:cookie"
        }
    },
    "food_component": {
        "hunger": 4.0,
        "saturation": 0.4,
        "snack": true
    },
    "use_action": "eat",
    "consuming_time_modifier": {
        "operation": "multiply_total_multiplicative",
        "value": 2
    },
    "priority": 1
}
```

This example will replace the food component of Cookies, making it take 3 times longer to eat while also giving 4 hunger shanks and 3.2 saturation (4.0 * 0.4 * 2).
