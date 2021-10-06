---
title: Action On Entity Use (Power Types)
date: 2021-10-05
---
# Action On Entity Use

[Power Type](../power_types.md)

Executes a bi-entity action, optionally gives an result item stack and executes an item action on both the result item stack and the item stack that's in the player's specified hand when the player "uses" (right-click) an entity.

Type ID: `origins:action_on_entity_use`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | _optional_ | If set, executes a bi-entity action that can execute on both the 'actor' (player) and 'target' entity.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If set, only execute the specified actions if the bi-entity condition is fulfilled.
`item_condition` | [Item Condition](../item_conditions.md) | _optional_ | If set, only execute the specified actions if the item condition is fulfilled by the item in the player's specified hand(s) equipment slot determined by the `hands` string field.
`hands` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand" , "main_hand"]` | Determines if the power should be activated if the player used a specific hand slot. Accepts `"off_hand"`, `"main_hand"` or both.
`result_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If set, gives the result item stack to the player.
`held_item_action` | [Item Action](../item_actions.md) | _optional_ | If set, executes an item action on the item stack used for right-clicking the entity in the specified hand slot.
`result_item_action` | [Item Action](../item_actions.md) | _optional_ | If set, executes an item action on the result item stack.
`action_result` | [String](../data_types/string.md) | `"success"` | Determines the result of the action. Accepts `"consume"`, `"consume_partial"`, `"fail"`, `"pass"` or `"success"`.

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
    "condition": {
        "type": "origins:and",
        "conditions": [
            {
                "type": "origins:sneaking"
            },
            {
                "type": "origins:equipped_item",
                "equipment_slot": "mainhand",
                "item_condition": {
                    "type": "origins:empty"
                }
            }
        ]
    }
}
```
This example heals and displays the heart particle effects at a tamed mob if the mob in question is owned by the player with this power.