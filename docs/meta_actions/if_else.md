---
title: If-Else (Meta Action)
date: 2021-04-07
---

# If-Else

[Meta Action](../meta_actions.md)

Executes an action only if a condition holds, and optionally executes another action when it doesn't hold.

Type ID: `origins:if_else`

!!! note

    Depending on the condition type, a different action type is expected:
    
    Action Type | Condition Type
    ------------|----------------
    [Entity Action](../entity_actions.md) | [Entity Condition](../entity_conditions.md)
    [Block Action](../block_actions.md) | [Block Condition](../block_conditions.md)
    [Item Action](../item_actions.md) | [Item Condition](../item_conditions.md)

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Condition](../conditions.md) | | A condition based on the type of action.
`if_action` | [Action](../actions.md) | | The action which is executed when the condition evaluates to true.
`else_action` | [Action](../actions.md) | _optional_ | If present, this action will be executed when the condition evaluates to false.

### Example

```json
"entity_action": {
  "type": "origins:if_else",
  "condition": {
    "type": "origins:fall_flying"
  },
  "if_action": {
    "type": "origins:set_on_fire",
    "duration": 5
  },
  "else_action": {
    "type": "origins:heal",
    "amount": 6
  }
}
```
This action will set the target on fire if they are in Elytra flight, or, if not in Elytra flight, will heal the target. The `else_action` can be omitted to just execute nothing if the `condition` doesn't hold.
