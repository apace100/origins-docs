---
title: Action On Entity Use (Power Types)
date: 2021-10-05
---

# Action On Entity Use

[Power Type](../power_types.md)

Executes an action when the player that has the power "uses" (right-clicks) an entity.

Type ID: `origins:action_on_entity_use`

!!! note

    In the context of this power type, the '**actor**' entity is the entity that has the power whilst the '**target**' entity is the entity that was "used" (right-clicked).


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this action will be executed on either or both the '**actor**' and '**target**' entities.
`held_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item used by the '**actor**' entity for right-clicking the '**target**' entity.
`result_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item that is given to the '**actor**' entity.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if this condition is fulfilled by the item used by the '**actor**' entity for right-clicking the '**target**' entity.
`hands` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand" , "main_hand"]` | Determines if the power should be activated if the '**actor**' entity used the specified hand(s). Accepts `"off_hand"`, `"main_hand"` or both
`result_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, this item stack will be given to the '**actor**' entity.
`action_result` | [Action Result](../../misc/extras/action_results.md) | `"success"` | Determines the result of the 'use' action.
`priority` | [Integer](../data_types/integer.md) | `0` | Determines the execution priority of the power.


### Examples

```json
{
    "type": "origins:action_on_entity_use",
    "bientity_action": {
        "type": "origins:target_action",
        "action": {
            "type": "origins:and",
            "actions": [
                {
                    "type": "origins:heal",
                    "amount": 2
                },
                {
                    "type": "origins:execute_command",
                    "command": "particle heart ~ ~0.5 ~ 0.3 0.3 0.3 0.009 4 normal @a"
                }
            ]
        }
    },
    "bientity_condition": {
        "type": "origins:owner"
    },
    "item_condition": {
        "type": "origins:empty"
    },
    "hands": [
        "main_hand"
    ],
    "condition": {
        "type": "origins:sneaking"
    }
}
```

This example will heal and display the heart particle effects at the tamed mob if the mob in question is owned by the player that has the power.
