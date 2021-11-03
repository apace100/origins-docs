---
title: Either (Meta Condition)
date: 2021-10-07
---

# Either

[Meta Condition](../meta_conditions.md)

Checks for an entity condition on either the actor or the target entities.

Type ID: `origins:either`

!!! note

	**Only available as a [Bi-entity Condition](../bientity_conditions.md).**

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`condition` | [Entity Condition](../entity_conditions.md) | | The condition to check on either actor or target entities.

### Example
```json
"bientity_condition": {
    "type": "origins:either",
    "condition": {
        "type": "origins:in_rain"
    }
}
```
This example will return true if either the actor or the target entities are in rain.