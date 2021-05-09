---
title: In Tag (Entity Condition)
date: 2021-04-04
---
# In Tag

[Entity Condition](../entity_conditions.md).

Checks whether the entity's entity type is in a specific tag.

Type ID: `origins:in_tag`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`tag` | [Identifier](../data_types/identifier.md) | |  ID of the tag the entity type needs to be in to pass the check.

### Example:
```json
"condition": {
    "type": "origins:in_tag",
    "tag": "minecraft:skeletons"
}
```
This example checks if the entity is inside the `#minecraft:skeletons` entity type tag. (`data\minecraft\tags\entity_types\skeletons.json`)