---
title: Passenger Recursive (Entity Condition)
date: 2021-10-07
---
# Passenger Recursive

[Entity Condition](../entity_conditions.md)

Checks whether any of the entities in the riding chain is the actor entity.

Type ID: `origins:passenger_recursive`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, only check for the entities that fulfills the bi-entity condition.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | How the number of entities that are currently riding the entity should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` | Which value the number of entities currently riding the entity should be compared to.

### Example
```json
"condition": {
    "type": "origins:passenger_recursive",
    "bientity_condition": {
        "type": "origins:actor_condition",
        "condition": {
            "type": "origins:entity_type",
            "entity_type": "minecraft:armor_stand"
        }
    },
    "comparison": ">=",
    "compare_to": 2
}
```
This example checks if the target entity is being ridden by an armor stand that is also being ridden by an armor stand (and so on).