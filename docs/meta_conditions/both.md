---
title: Both (Meta Condition)
date: 2021-10-07
---

# Both

[Meta Condition](../meta_conditions.md)

Checks for an entity condition on both the actor and target entities.

Type ID: `origins:both`

!!! note

	**Only available as a [Bi-entity Condition](../bientity_conditions.md).**

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`condition` | [Entity Condition](../entity_conditions.md) | | The condition to check on both the actor and target entity.

### Example
```json
"bientity_condition": {
    "type": "origins:both",
    "condition": {
        "type": "origins:entity_type",
        "entity_type": "minecraft:player"
    }
}
```
This example will only return true if both the actor entity and the target entity is a player.