---
title: Prevent Being Used (Power Type)
date: 2021-10-06
---

# Prevent Being Used

[Power Type](../power_types.md)

Prevents other players from being able to "use" (right-click) the entity that has the power and executes a bi-entity action, item action and/or give an item upon being prevented.

Type ID: `origins:prevent_being_used`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this action will be executed on either or both 'actor' (player) or 'target' (the entity that has the power) entities.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by either or both 'actor' (player) or 'target' (the entity that has the power) entities.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by the item in the 'actor' (player) entity's specified hand(s) determined by the `hands` string array field.
`hands` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand", "main_hand"]` | Determines if the power should be activated if the 'actor' (player) entity used the specified hand(s). Accepts `"off_hand"`, `"main_hand"` or both.
`result_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item will be given to the 'actor' (player) entity.
`held_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item used for right-clicking the 'target' (the entity that has the power) entity in the 'actor' (player) entity's specified hand(s) determined by the `hands` string array field.
`result_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item that is given to the 'actor' (player) entity.


### Examples

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
