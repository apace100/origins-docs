---
title: Riding Action (Entity Action Type)
date: 2021-10-06
---

# Riding Action

[Entity Action Type](../entity_action_types.md)

Executes an action on the entity/entities that's being ridden by the entity.

Type ID: `origins:riding_action`

!!! note

    Not to be confused with [Passenger Action](./passenger_action.md).


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity being ridden.
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | _optional_ | If specified, this action will be executed on either the 'actor' (the passenger entity) or the 'target' (the entity being ridden) or both.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by either the 'actor' (the passenger entity) or the 'target' (entity being ridden) or both.
`recursive` | [Boolean](../data_types/boolean.md) | `false` | If set to `true`, the specified action(s) will be executed on all entities that are being ridden.


### Examples

```json
"entity_action": {
    "type": "origins:riding_action",
    "action": {
        "type": "origins:apply_effect",
        "effect": {
            "effect": "minecraft:speed",
            "duration": 100,
            "amplifier": 1
        }
    }
}
```

This example will apply a Speed II status effect to the entity that is currently being ridden by the entity that executed the entity action type.
