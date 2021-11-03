---
title: Passenger (Entity Condition)
date: 2021-10-07
---

# Passenger

[Entity Condition](../entity_conditions.md)

Checks whether the actor entity is directly riding the target entity.

Type ID: `origins:passenger`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, it will check for the entity/entities that fulfills the bi-entity condition.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | How the number of entities that are currently riding the entity should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` | Which value the number of entities currently riding the entity should be compared to.

### Example
```json
"condition": {
    "type": "origins:passenger",
    "bientity_condition": {
        "type": "origins:actor_condition",
        "condition": {
            "type": "origins:entity_type",
            "entity_type": "minecraft:player"
        }
    }
}
```
This example checks if the target entity is being ridden by a player (actor entity).