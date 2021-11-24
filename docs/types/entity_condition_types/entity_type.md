---
title: Entity Type (Entity Condition Type)
date: 2021-04-04
---

# Entity Type

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity is of a specific entity type.

Type ID: `origins:entity_type`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_type` | [Identifier](../data_types/identifier.md) | |  ID of the entity type the entity needs to have to pass the check.

### Example
```json
"condition": {
    "type": "origins:entity_type",
    "entity_type": "minecraft:creeper"
}
```
This example checks if the entity is a Creeper.
