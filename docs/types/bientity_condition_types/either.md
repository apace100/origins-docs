---
title: Either (Bi-entity Condition Type)
date: 2021-10-07
---

# Either

[Bi-entity Condition Type](../bientity_condition_types.md)

Checks for an entity condition on either the actor or the target entities.

Type ID: `origins:either`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`condition` | [Entity Condition Type](../entity_condition_types.md) | | The entity condition type to check on either actor or target entities.


### Examples

```json
"bientity_condition": {
    "type": "origins:either",
    "condition": {
        "type": "origins:in_rain"
    }
}
```

This example will check if either the actor or target entities are in rain.
