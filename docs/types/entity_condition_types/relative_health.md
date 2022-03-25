---
title: Relative Health (Entity Condition Type)
date: 2021-04-04
---

# Relative Health

[Entity Condition Type](../entity_condition_types.md)

Checks the current (and the percentage) health value of the entity.

Type ID: `apoli:relative_health`

!!! note

    The percentage of the health value can be calculated with the `currentHealth / maxHealth` formula.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the relative health of the player should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | Which value the relative health should be compared to.


### Examples

```json
"condition": {
    "type": "apoli:relative_health",
    "comparison": "<=",
    "compare_to": 0.5
}
```

This example will check if the player has half or less of their max health.