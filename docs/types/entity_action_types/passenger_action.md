---
title: Passenger Action (Entity Action Type)
date: 2021-10-06
---

# Passenger Action

[Entity Action Type](../entity_action_types.md)

Executes an action on the passengers of the entity.

Type ID: `origins:passenger_action`

!!! note

    Not to be confused with [Riding Action](./riding_action.md)


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the passenger entity.
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this action will be executed on either the 'actor' (the entity being ridden) or the 'target' (the passenger entity) or both.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if this condition is fulfilled by either the 'actor' (the entity being ridden) or the 'target' (the passenger entity) or both.
`recursive` | [Boolean](../data_types/boolean.md) | `false` | If set to `true`, the specified action(s) will be executed on all the passenger entities.


### Examples

```json
"entity_action": {
    "type": "origins:passenger_action",
    "action": {
        "type": "origins:heal",
        "amount": 2
    },
    "recursive": true
}
```

This example will heal all entities that are currently riding the entity that executed this entity action type.
