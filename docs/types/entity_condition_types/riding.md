---
title: Riding (Entity Condition Type)
date: 2021-10-07
---

# Riding

[Entity Condition Type](../entity_condition_types.md)

Checks whether the actor entity is directly riding the target entity.

Type ID: `apoli:riding`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, it will only check for the entity/entities that fulfills the bi-entity condition.


### Examples

```json
"condition": {
    "type": "apoli:riding",
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "type": "apoli:entity_type",
            "entity_type": "minecraft:minecart"
        }
    }
}
```

This example will check if the actor entity is currently riding a minecart (target entity).
