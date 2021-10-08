---
title: Riding Root (Entity Condition)
date: 2021-10-07
---
# Riding Root

[Entity Condition](../entity_conditions.md)

Checks whether the actor entity is riding the target entity from the very end of the riding chain.

Type ID: `origins:riding_root`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, it will only check for the entity/entities that fulfills the bi-entity condition.

### Example
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
This example checks if the actor entity is riding a pig. It will also return true if the pig has an additional passenger and if the actor entity is riding that passenger.