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
`action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, executes the specified entity action type on the passenger entity.
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, executes the specified bi-entity action type that can execute on both the passenger and the entity that's being ridden.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, only execute the specified actions if the bi-entity condition is fulfilled.
`recursive` | [Boolean](../data_types/boolean.md) | `false` | If set to true, executes the specified actions on all the passenger entities, if there are more than one.


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
