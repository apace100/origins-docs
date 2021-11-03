---
title: Prevent Being Used (Power Type)
date: 2021-10-06
---

# Prevent Being Used

[Power Type](../power_types.md)

Prevents other players from being able to "use" (right-click) the entity that has the power and optionally gives a result item stack, execute a bi-entity action and an item action on both the result item stack and the item stack in other player's specified hand.

Type ID: `origins:prevent_being_used`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | _optional_ | The action to execute upon preventing other players from right-clicking the entity that has the power if specified.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, only execute the specified actions if the bi-entity condition is fulfilled.
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If specified, only execute the specified actions if the item condition is fulfilled by the item in the other player's specified hand(s) equipment slot determined by the `hands` string field.
`hands` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand", "main_hand"]` | Determines if the power should be activated if the other player used the specified hand slot(s). Accepts `"off_hand"`, `"main_hand"` or both.
`result_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, gives an item stack to the player.
`result_item_action` | [Item Action](../item_actions.md) | _optional_ | If specified, executes an item action on the given item stack.

### Example
```json
{
    "type": "origins:prevent_being_used",
    "bientity_action": {
        "type": "origins:actor_action",
        "action": {
            "type": "origins:execute_command",
            "command": "title @s actionbar {\"text\": \"Entity cannot be interacted with!\", \"color\": \"red\"}"
        }
    }
}
```
This example will prevent other players from "using" (right-clicking) the entity that has the power and inform them that the 'entity cannot be interacted with'.