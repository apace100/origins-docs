---
title: If-Else (Meta Action Type)
date: 2021-04-07
---

# If-Else

[Meta Action Type](../meta_action_types.md)

Executes an action only if a condition holds, and optionally executes another action when it doesn't hold.

Type ID: `apoli:if_else`

!!! note

    Depending on the condition type, a different action type is expected:
    
    Action Type | Condition Type
    ------------|----------------
    [Bi-entity Action Type](../bientity_action_types.md) | [Bi-entity Condition Type](../bientity_condition_types.md)
    [Entity Action Type](../entity_action_types.md) | [Entity Condition Type](../entity_condition_types.md)
    [Block Action Type](../block_action_types.md) | [Block Condition Type](../block_condition_types.md)
    [Item Action Type](../item_action_types.md) | [Item Condition Type](../item_condition_types.md)


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Condition Type](../condition_types.md) | | A condition based on the type of action.
`if_action` | [Action Type](../action_types.md) | | The action which is executed when the condition evaluates to true.
`else_action` | [Action Type](../action_types.md) | _optional_ | If present, this action will be executed when the condition evaluates to false.


### Examples

```json
"entity_action": {
    "type": "apoli:if_else",
    "condition": {
        "type": "apoli:fall_flying"
    },
    "if_action": {
        "type": "apoli:set_on_fire",
        "duration": 5
    },
    "else_action": {
        "type": "apoli:heal",
        "amount": 6
    }
}
```

This example will set the entity on fire if they are "fall flying" for 5 seconds. Otherwise, it will restore 3 hearts of health to the entity instead.
