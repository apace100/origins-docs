---
title: Riding Root (Entity Condition Type)
date: 2021-10-07
---

# Riding Root

[Entity Condition Type](../entity_condition_types.md)

Checks whether the actor entity is riding the target entity from the very end of the riding chain.

Type ID: `apoli:riding_root`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, it will only check for the entity/entities that fulfills the bi-entity condition.


### Examples

```json
"condition": {
    "type": "apoli:riding_root",
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "type": "apoli:entity_type",
            "entity_type": "minecraft:pig"
        }
    }
}
```

This example will check if the actor entity is riding a pig. It will also return true if the pig has an additional passenger and if the actor entity is riding that passenger.
