---
title: Relative Health (Entity Condition Type)
date: 2021-04-04
---

# Relative Health

[Entity Condition Type](../entity_condition_types.md)

Checks the current (and the percentage) health value of the entity.

Type ID: `origins:relative_health`

!!! note

    The percentage of the health value can be calculated with the `currentHealth / maxHealth` formula.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | Determines how the relative health of the entity should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | The value at which the relative health of the entity will be compared to.


### Examples

```json
"condition": {
    "type": "origins:relative_health",
    "comparison": "<=",
    "compare_to": 0.5
}
```

This example will check if the player has half or less of their max health.