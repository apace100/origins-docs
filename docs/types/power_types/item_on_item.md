---
title: Item On Item (Power Type)
date: 2021-10-02
---

# Item On Item

[Power Type](../power_types.md)

Executes an [Entity Action Type](../entity_action_types.md) or [Item Action Types](../item_action_types.md) when the player uses an item on an item, similar to how you would put items in a bundle.

Type ID: `origins:item_on_item`

!!! caution

    This power type currently does not work properly in Creative Mode.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`using_item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the specified actions will only execute if this condition is fulfilled by the item that is used to right-click an item.
`on_item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the specified actions will only execute if this condition is fulfilled by the item that has been right-clicked.
`result` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item will be given to the player.
`result_from_on_stack` | [Integer](../data_types/integer.md) | `0` | Determines how many items based on the `on_item` stack will be given as a result for using an item on an item. Mostly to be used in conjunction with `result_item_action`.
`using_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item that is used to right-click an item.
`on_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item that has been right-clicked.
`result_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item that is given to the player.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player after they used an item on an item.
`click_type` | [String](../data_types/string.md) or [Integer](../data_types/integer.md) | `"secondary"` | Determines whether to execute the actions if the player does a right-click (`0` or `"primary"`) or left-click (`1` or `"secondary"`) action.


### Examples

```json
{
    "type": "origins:item_on_item",
    "on_item_condition": {
        "type": "origins:smeltable"
    },
    "using_item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:coal"
        }
    },
    "result_from_on_stack": 8,
    "result_item_action": {
        "type": "origins:modify",
        "modifier": "example:furnace_smelt"
    },
    "using_item_action": {
        "type": "origins:consume",
        "amount": 1
    }
}
```

This example will smelt smeltable items by using a Coal item on it.
<br>

```json
{
    "function": "minecraft:furnace_smelt"
}
```

This example being the contents of the `example:furnace_smelt` (`data/example/item_modifiers/furnace_smelt.json`) item modifier.
<br>

```json
{
    "type": "origins:item_on_item",
    "using_item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "tag": "fabric:axes"
        }
    },
    "on_item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:oak_log"
        }
    },
    "result": {
        "item": "minecraft:oak_planks",
        "amount": 8
    },
    "using_item_action": {
        "type": "origins:damage",
        "amount": 20,
        "ignore_unbreaking": false
    },
    "on_item_action": {
        "type": "origins:consume",
        "amount": 1
    },
    "entity_action": {
        "type": "origins:play_sound",
        "sound": "minecraft:entity.zombie.break_wooden_door",
        "volume": 0.45,
        "pitch": 2
    }
}
```

This example will give the player 8 Oak Planks if the player were to use any Axe tool item on an Oak Log item (have the Axe tool item in the cursor, and right-click on an Oak Log item). 
