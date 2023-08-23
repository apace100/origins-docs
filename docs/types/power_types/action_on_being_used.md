---
title: Action On Being Used (Power Type)
date: 2021-10-06
---

# Action On Being Used

[Power Type](../power_types.md)

Executes an action when a player "uses" (right-clicks) the entity that has the power.

Type ID: `origins:action_on_being_used`

!!! note

    In the context of this power type, the '**actor**' entity is the entity that did the "usage" action (right-click) while the '**target**' entity is the entity that has the power.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this action will be executed on either or both the '**actor**' and '**target**' entities.
`held_item_action`| [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item used by the '**actor**' entity for right-clicking the '**target**' entity.
`result_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item that is given to the '**actor**' entity.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if this condition is fulfilled by the item used by the '**actor**' entity for right-clicking the '**target**' entity.
`hands`| [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand", "main_hand"]` | Determines if the power should be activated if the '**actor**' entity used the specified hand(s). Accepts `"off_hand"`, `"main_hand"` or both
`result_stack`| [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item stack will be given to the '**actor**' entity.
`action_result` | [Action Result](../data_types/action_result.md) | `"success"` | Determines the result of the 'use' action.
`priority` | [Integer](../data_types/integer.md) | `0` | Determines the execution priority of the power.


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
