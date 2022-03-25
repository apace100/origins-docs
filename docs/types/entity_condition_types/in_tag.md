---
title: In Tag (Entity Condition Type)
date: 2021-04-04
---

# In Tag

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity's entity type is in a specific tag.

Type ID: `apoli:in_tag`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`tag` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the entity type tag the entity type needs to be in to pass the check.


### Examples

```json
"condition": {
    "type": "apoli:in_tag",
    "tag": "minecraft:skeletons"
}
```

This example will check if the entity is inside the `#minecraft:skeletons` entity type tag. (`data/minecraft/tags/entity_types/skeletons.json`)
