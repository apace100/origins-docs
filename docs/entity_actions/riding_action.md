---
title: Riding Action (Entity Action)
date: 2021-10-06
---
# Riding Action

[Entity Action](../entity_actions.md)

Executes an action on the entity/entities that's being ridden by the entity.

Type ID: `origins:riding_action`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`action` | [Entity Action](../entity_actions.md) | _optional_ | If set, executes the specified action on the entity that's been ridden.
`bientity_action` | [Bi-entity Action](../bientity_actions.md) | | If set, executes the specified action that can execute on both the passenger and the entity that's being ridden.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | | If set, only execute the specified actions if the bi-entity condition is fulfilled.
`recursive` | [Boolean](../data_types/boolean.md) | false | If set to true, executes the specified actions on all entities that are being ridden, if there are more than one.

### Example
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
This example will apply a Speed II status effect to the entity that is currently being ridden by the entity that executed the action.