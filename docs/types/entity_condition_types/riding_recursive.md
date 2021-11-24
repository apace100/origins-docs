---
title: Riding Recursive (Entity Condition Type)
date: 2021-10-07
---

# Riding Recursive

[Entity Condition Type](../entity_condition_types.md)

Checks whether any of the entities in the riding chain (starting from the actor entity) is the target entity.

Type ID: `origins:riding_recursive`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, it will only check for the entity/entities that fulfills the bi-entity condition.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | How the amount of entities currently being ridden should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` | Which value the amount of entities currently being ridden should be compared to.

### Example
```json
"condition": {
    "type": "origins:riding_recursive",
    "bientity_condition": {
        "type": "origins:target_condition",
        "condition": {
            "type": "origins:entity_type",
            "entity_type": "minecraft:strider"
        },
        "comparison": ">=",
        "compare_to": 2
    }
}
```
This example checks if the actor entity is riding a strider that is also riding a strider (and so on).