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
`return_stack`| [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item stack will be given to the player.
`consume_action` | [String](../data_types/string.md) | `"eat"` | Determines whether the action of consuming the item is considered "eating" (`"eat"`) or "drinking" (`"drink"`).
`consume_sound` | [Identifier](../data_types/identifier.md) |  | If specified, the sound event with this namespace and ID will be played when the item is eaten.
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
    "return_stack": {
        "item": "minecraft:water_bucket",
        "amount": 1
    }
}
```

This example will grant the players the ability to eat axolotls in buckets. It will give 4 hunger shanks and 8 saturation (4 * 1 * 2), it also counts as meat. This returns a water bucket upon consumption and uses the eat action.