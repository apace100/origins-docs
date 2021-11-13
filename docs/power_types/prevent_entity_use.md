---
title: Prevent Entity Use (Power Type)
date: 2021-10-06
---

# Prevent Entity Use

[Power Type](../power_types.md)

Prevents the player that has the power from "using" (right-clicking) an entity and executes a bi-entity action, item action and/or give an item upon being prevented.

Type ID: `origins:prevent_entity_use`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | _optional_ | If specified, this action will be executed on either or both 'actor' (the player that has the power) or 'target' (the entity that is right-clicked) entities.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by either or both 'actor' (the player that has the power) or 'target' (the entity that is right-clicked) entities.
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by the item in the 'actor' (the player that has the power) entity's specified hand(s) determined by the `hands` string array field.
`hands` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand", "main_hand"]` | Determines if the power should be activated if the 'actor' (the player that has the power) entity used the specified hand(s). Accepts `"off_hand"`, `"main_hand"` or both.
`result_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item will be given to the 'actor' (the player that has the power) entity.
`held_item_action` | [Item Action](../item_actions.md) | _optional_ | If specified, this action will be executed on the item used for right-clicking the 'target' (the entity that is right-clicked) entity in the 'actor' (the player that has the power) entity's specified hand(s) determined by the `hands` string array field.
`result_item_action` | [Item Action](../item_actions.md) | _optional_ | If specified, this action will be executed on the item that is given to the 'actor' (the player that has the power) entity.

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