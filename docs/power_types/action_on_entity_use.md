---
title: Action On Entity Use (Power Types)
date: 2021-10-05
---

# Action On Entity Use

[Power Type](../power_types.md)

Executes a bi-entity action or item actions when the player that has the power "uses" (right-clicks) an entity.

Type ID: `origins:action_on_entity_use`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | _optional_ | If specified, this action will be executed on either or both 'actor' (the player that has the power) or 'target' (the entity that's been right-clicked) entity.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by either or both 'actor' (the player that has the power) or 'target' (the entity that's been right-clicked) entity.
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by the item in the 'actor' (the player that has the power) entity's specified hand(s) determined by the `hands` string field.
`hands` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand" , "main_hand"]` | Determines if the power should be activated if the player used the specified hand(s). Accepts `"off_hand"`, `"main_hand"` or both.
`result_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, gives the item to the 'actor' (the player that has the power) entity.
`held_item_action` | [Item Action](../item_actions.md) | _optional_ | If specified, this action will be executed on the item used for right-clicking the 'target' entity in the specified hand(s) determined by the `hands` string field.
`result_item_action` | [Item Action](../item_actions.md) | _optional_ | If specified, this action will be executed on the item that is given to the 'actor' (the player that has the power) entity.
`action_result` | [String](../data_types/string.md) | `"success"` | Determines the result of the 'use action'. Accepts `"consume"`, `"consume_partial"`, `"fail"`, `"pass"` or `"success"`.

### Example
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
This example heals and displays the heart particle effects at a tamed mob if the mob in question is owned by the player with this power.
