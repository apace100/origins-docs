---
title: Riding Action (Entity Action Type)
date: 2021-10-06
---

# Riding Action

[Entity Action Type](../entity_action_types.md)

Executes an action on the entity/entities that's being ridden by the entity.

Type ID: `origins:riding_action`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, executes the specified entity action type on the entity that's been ridden.
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | | If specified, executes the specified bi-entity action type that can execute on both the passenger and the entity that's being ridden.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | | If set, only execute the specified actions if the bi-entity condition is fulfilled.
`recursive` | [Boolean](../data_types/boolean.md) | `false` | If set to true, executes the specified actions on all entities that are being ridden, if there are more than one.


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
