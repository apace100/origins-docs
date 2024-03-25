---
title: Passenger (Entity Condition Type)
date: 2021-10-07
---

# Passenger

[Entity Condition Type](../entity_condition_types.md)

Checks how many passengers are currently riding the entity.

Type ID: `origins:passenger`


!!! note

    In the context of this entity condition type, the '**actor**' entity/entities is/are the passenger(s) and the '**target**' is the entity that invoked the condition.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, only increase the amount of passengers if either or both the '**actor**' entity/entities and the '**target**' entity fulfills this bi-entity condition.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | How the amount of passengers of the entity should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` | The value at which the amount of passengers of the entity will be compared to.


### Examples

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

This example will check if the target entity is being ridden by a player (actor entity).
