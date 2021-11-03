---
title: Passenger Action (Entity Action)
date: 2021-10-06
---

# Passenger Action

[Entity Action](../entity_actions.md)

Executes an action on the passengers of the entity.

Type ID: `origins:passenger_action`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`action` | [Entity Action](../entity_actions.md) | _optional_ | If set, executes the specified action on the passenger entity.
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | _optional_ | If set, executes the specified action that can execute on both the passenger and the entity that's being ridden.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If set, only execute the specified actions if the bi-entity condition is fulfilled.
`recursive` | [Boolean](../data_types/boolean.md) | false | If set to true, executes the specified actions on all the passenger entities, if there are more than one.

### Example
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
This example will heal all entities that are currently riding the entity that executed this action.