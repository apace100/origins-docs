---
title: Action On Being Used (Power Type)
date: 2021-10-06
---

# Action On Being Used

[Power Type](../power_types.md)

Executes a bi-entity action, optionally gives a result item stack and executes an item action on both the result item stack and the item stack that's in the player's specified hand when a player "uses" (right-click) the entity that has the power.

Type ID: `origins:action_on_being_used`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | _optional_ | The action to be executed if specified.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, only execute the specified actions if the bi-entity condition is fulfilled.
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If specified, only execute the specified actions if the item condition is fulfilled by the item in the player's specified hand(s) determined by the `hands` string field.
`hands`| [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand", "main_hand"]` | Determines if the power should be activated if the player used the specified hand(s). Accepts `"off_hand"`, `"main_hand"` or both.
`result_stack`| [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, gives an item stack to the player.
`held_item_action`| [Item Action](../item_actions.md) | _optional_ | If specified, executes an item action on the item stack used for right-clicking the entity in the specified hand slot.
`result_item_action` | [Item Action](../item_actions.md) | _optional_ | The action to be executed on the result item stack if specified.
`action_result` | [String](../data_types/string.md) | `"success"` | Determines the result of the action. Accepts `"consume"`, `"consume_partial"`, `"fail"`, `"pass"` or `"success"`.

### Example
```json
{
    "type": "origins:action_on_being_used",
    "bientity_action": {
        "type": "origins:and",
        "actions": [
            {
                "type": "origins:target_action",
                "action": {
                    "type": "origins:execute_command",
                    "command": "clear @s minecraft:diamond 1"
                }
            },
            {
                "type": "origins:actor_action",
                "action": {
                    "type": "origins:execute_command",
                    "command": "give @s minecraft:diamond 1"
                }
            }
        ]
    },
    "bientity_condition": {
        "type": "origins:target_condition",
        "condition": {
            "type": "origins:command",
            "command": "clear @s minecraft:diamond 0",
            "comparison": ">",
            "compare_to": 0
        }
    },
    "hands": [
        "main_hand"
    ]
}
```
This example enables other players to steal diamonds from the player that has the power.