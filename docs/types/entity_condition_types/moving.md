---
title: Moving (Entity Condition Type)
date: 2021-04-06
---

# Moving

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity is currently moving.

Type ID: `origins:moving`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`horizontally` | [Boolean](../data_types/boolean.md) | `true` | Determines whether to check if the entity is moving horizontally.
`vertically` | [Boolean](../data_types/boolean.md) | `true` | Determines whether to check if the entity is moving vertically.


### Examples

```json
"condition": {
    "type": "origins:moving"
}
```

This example will check if the entity is moving either horizontally or vertically.
<br>

```json
"condition": {
    "type": "origins:moving",
    "horizontally": false
}
```

This example will check if the entity is only moving vertically.
