---
title: Riding (Entity Condition Type)
date: 2021-10-07
---

# Riding

[Entity Condition Type](../entity_condition_types.md)

Checks whether the actor entity is directly riding the target entity.

Type ID: `origins:riding`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, it will only check for the entity/entities that fulfills the bi-entity condition.

### Example
```json
"condition": {
    "type": "origins:riding",
    "bientity_condition": {
        "type": "origins:target_condition",
        "condition": {
            "type": "origins:entity_type",
            "entity_type": "minecraft:minecart"
        }
    }
}
```
This example checks if the actor entity is currently riding a minecart (target entity).