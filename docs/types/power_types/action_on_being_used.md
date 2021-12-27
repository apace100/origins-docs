---
title: Action On Being Used (Power Type)
date: 2021-10-06
---

# Action On Being Used

[Power Type](../power_types.md)

Executes a [Bi-entity Action Type](../bientity_action_types.md) or [Item Action Types](../item_action_types.md) when a player "uses" (right-clicks) the entity that has the power.

Type ID: `origins:action_on_being_used`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this action will be executed on either or both 'actor' (player) or 'target' (the entity that has the power) entities.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by either or both 'actor' (player) or 'target' (the entity that has the power) entities.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by the item in the 'actor' (player) entity's specified hand(s) determined by the `hands` string array field.
`hands`| [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand", "main_hand"]` | Determines if the power should be activated if the player used the specified hand(s). Accepts `"off_hand"`, `"main_hand"` or both.
`result_stack`| [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item will be given to the 'actor' (player) entity.
`held_item_action`| [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item used for right-clicking the 'target' (the entity that has the power) entity in the 'actor' (player) entity's specified hand(s) determined by the `hands` string array field.
`result_item_action` | [Item Action Type](../item_action_types/consume.md) | _optional_ | If specified, this action will be executed on the item that is given to the 'actor' (player) entity.
`action_result` | [String](../data_types/string.md) | `"success"` | Determines the result of the 'use' action. See [Action Result](../../misc/extras/action_result.md) for possible values.


### Examples

```json
{
    "type": "origins:action_on_being_used",
    "bientity_action": {
        "type": "origins:mount"
    },
    "bientity_condition": {
        "type": "origins:target_condition",
        "condition": {
            "type": "origins:passenger",
            "inverted": true
        }
    }
}
```

This example will grant the players the ability to mount the target entity that has the power upon "using" (right-clicking) the said entity, unless the entity that has the power already has a passenger.
