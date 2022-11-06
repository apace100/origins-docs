---
title: Riding Root (Entity Condition Type)
date: 2021-10-07
---

# Riding Root

[Entity Condition Type](../entity_condition_types.md)

Checks whether the actor entity is riding the target entity from the very start of the riding chain.

Type ID: `origins:riding_root`


!!! note

    In the context for this entity condition type, the actor entity is the passenger and the entity that invoked the condition while the target is the entity that is being ridden at the very start of the riding chain.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, this condition type will only evaluate to true if this condition is fulfilled by either or both the actor and target entities.


### Examples

```json
"condition": {
    "type": "origins:riding_root"
}
```

This example will check if the actor entity is riding an entity.
<br>

```json
"condition": {
    "type": "origins:riding_root",
    "bientity_condition": {
        "type": "origins:target_condition",
        "condition": {
            "type": "origins:entity_type",
            "entity_type": "minecraft:pig"
        }
    }
}
```

This example will check if the actor entity is riding a pig. This will also check if the actor entity is riding the passenger(s) of a pig.
