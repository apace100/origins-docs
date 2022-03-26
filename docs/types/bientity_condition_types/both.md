---
title: Both (Bi-entity Condition Type)
date: 2021-10-07
---

# Both

[Bi-entity Condition Type](../bientity_condition_types.md)

Checks for an entity condition on both the actor and target entities.

Type ID: `origins:both`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`condition` | [Entity Condition Type](../entity_condition_types.md) | | The entity condition type to check on both the actor and target entity.


### Examples

```json
"bientity_condition": {
    "type": "origins:both",
    "condition": {
        "type": "origins:entity_type",
        "entity_type": "minecraft:player"
    }
}
```

This example will check if both the actor entity and the target entity is a player.
