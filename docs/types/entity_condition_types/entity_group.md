---
title: Entity Group (Entity Condition Type)
date: 2021-04-04
---

# Entity Group

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity is of a specific entity group.

Type ID: `origins:entity_group`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`group` | [String](../data_types/string.md) | |  Entity group required for the entity to pass the check. One of `default`, `undead`, `arthropod`, `illager` and `aquatic`.

### Example
```json
"condition": {
    "type": "origins:entity_group",
    "group": "undead"
}
```
This example checks if the entity is included in the `undead` entity group.