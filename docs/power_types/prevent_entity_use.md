---
title: Prevent Entity Use (Power Type)
date: 2021-10-06
---

# Prevent Entity Use

[Power Type](../power_types.md)

Prevents the player from "using" (right-clicking) an entity and optionally gives a result item stack, execute a bi-entity action and an item action on both the result item stack and the item stack in the player's specified hand.

Type ID: `origins:prevent_entity_use`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | _optional_ | The action to execute upon being prevented from right-clicking an entity.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, only execute the specified actions if the bi-entity condition is fulfilled.
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If specified, only execute the specified actions if the item condition is fulfilled by the item in the player's specified hand(s) equipment slot determined by the `hands` string field.
`hands` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand", "main_hand"]` | Determines if the power should be activated if the player used the specified hand slot(s). Accepts `"off_hand"`, `"main_hand"` or both.
`result_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, gives the result item stack to the player.
`held_item_action` | [Item Action](../item_actions.md) | _optional_ | If specified, executes an item action on the item stack used for right-clicking the entity in the specified hand slot.
`result_item_action` | [Item Action](../item_actions.md) | _optional_ | If specified, executes an item action on the result item stack.

### Example
```json
{
    "type": "origins:prevent_entity_use",
    "bientity_action": {
        "type": "origins:actor_action",
        "action": {
            "type": "origins:execute_command",
            "command": "title @s actionbar {\"text\": \"Cannot interact with pigs!\", \"color\": \"red\"}"
        }
    },
    "bientity_condition": {
        "type": "origins:target_condition",
        "condition": {
            "type": "origins:entity_type",
            "entity_type": "minecraft:pig"
        }
    }
}
```
This example prevents you from interacting with a pig (also prevents powers that enables you to interact with a pig) and executes an `origins:execute_command` entity action to the entity that has attempted to interact with a pig.