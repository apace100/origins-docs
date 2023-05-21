---
title: Action On Item Use (Power Type)
date: 2021-04-04
---

# Action On Item Use

[Power Type](../power_types.md)

Executes an [Entity Action Type](../entity_action_types.md) or an [Item Action Type](../item_action_types.md) when the player uses an item (e.g: eating food or drinking a potion).

Type ID: `origins:action_on_item_use`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the player after they use an item.
`item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the _remaining_ item.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the actions will only execute if this condition is fulfilled by the item _before use._
`trigger` | [String](../data_types/string.md) | `"finish"` | Defines when the action is executed, see below table for accepted values.
`priority` | [Integer](../data_types/integer.md) | `0` | Determines the execution priority of the power.

### Triggers

Name | Description
-----|------------
`finish` | The action will execute when the entity finishes (as in, completes) using an item which has a use duration, such as eating food.
`start` | The action will execute when the entity starts using an item which has a use duration.
`stop` | The action will execute when the entity stops using an item which has a use duration, before the maximum use duration has been reached. Compared to `finish`, this can be used to detect shooting a bow, for example.
`during` | The action will be called every tick while the entity is using an item which has a use duration.
`instant` | The action will not fire for items with a use duration, but will instead fire when an item is used which triggers its effect instantly, such as an ender pearl or splash potion.

### Examples

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

This example will give half a shank of hunger, and 1 saturation point if the player drinks any kind of potion.
<br>

```json
{
    "type": "origins:action_on_item_use",
    "trigger": "instant",
    "entity_action": {
        "type": "origins:apply_effect",
        "effect": {
            "effect": "minecraft:invisibility",
            "duration": 400,
            "amplifier": 0
        }
    },
    "item_condition": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:ender_pearl"
        }
    }
}
```

This example will give the player 20 seconds of invisibility whenever they throw an ender pearl.