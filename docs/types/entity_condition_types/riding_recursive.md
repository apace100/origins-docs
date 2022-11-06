---
title: Riding Recursive (Entity Condition Type)
date: 2021-10-07
---

# Riding Recursive

[Entity Condition Type](../entity_condition_types.md)

Checks whether the '**actor**' entity is directly riding the '**target**' entity or the passenger(s) of the '**target**' entity.

Type ID: `origins:riding_recursive`


!!! note

    In the context of this entity condition type, the '**actor**' entity is the passenger and the entity that invoked the condition whilst the '**target**' entities are the entity that is being directly ridden and the passenger(s) of the said entity.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, this condition type will only evaluate to true if this condition is fulfilled by either or both the '**actor**' and '**target**' entities.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | How the amount of entities currently being ridden should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` | Which value the amount of entities currently being ridden should be compared to.


### Examples

```json
"condition": {
    "type": "origins:riding_recursive",
    "comparison": ">=",
    "compare_to": 2
}
```

This example will check if the '**actor**' entity is currently riding an entity directly or an entity that has one or multiple passengers, regardless of their entity type.
<br>

```json
"condition": {
    "type": "origins:riding_recursive",
    "bientity_condition": {
        "type": "origins:target_condition",
        "condition": {
            "type": "origins:entity_type",
            "entity_type": "minecraft:strider"
        }
    },
    "comparison": ">=",
    "compare_to": 2
}
```

This example will check if the '**actor**' entity is currently riding a Strider directly or an entity that has Striders as its passengers. 
