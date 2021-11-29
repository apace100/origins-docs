---
title: Health (Entity Condition Type)
date: 2021-04-04
---

# Health

[Entity Condition Type](../entity_condition_types.md)

Checks the current (and absolute) health value of the entity.

Type ID: `origins:health`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the health of the entity should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | Which value the health should be compared to.


### Examples

```json
"condition": {
    "type": "origins:health",
    "comparison": "<",
    "compare_to": 20
}
```

This example will check if the entity's health is less than 10 hearts (or 20 health points).
