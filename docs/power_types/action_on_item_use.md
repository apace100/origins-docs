---
title: Action On Item Use (Power Type)
date: 2021-04-04
---
# Action On Item Use

[Power Type](../power_types.md).

Executes an entity or item action when the player finishes using an item (such as eating food or drinking a potion).

Type ID: `origins:action_on_item_use`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player after they use the item.
`item_action` | [Item Action](../item_actions.md) | _optional_ | If set, this action will be executed on the _remaining_ item stack.
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If set, the actions will only trigger when this item condition is met by the item stack _before use_.


### Example
```json
{
    "type": "origins:action_on_item_use",
    "entity_action": {
        "type": "origins:feed",
        "food": 1.0,
        "saturation": 1.0
    },
    "item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:potion"
        }
    }
}
```
This power will give half a shank of hunger, and 1 saturation point if the player drinks any kind of potion.