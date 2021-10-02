---
title: NBT (Entity Condition)
date: 2021-10-02
---
# NBT

[Entity Condition](../entity_conditions.md)

Checks the entity's NBT.

Type ID: `origins:nbt`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`nbt` | [String](../data_types/string.md) | | The NBT data to check for.

### Example
```json
"condition": {
    "type": "origins:nbt",
    "nbt": "{Tags: ['example_tag']}"
}
```
This example checks if the entity has the `example_tag` added via `/tag` or by modifying the entity's `Tags` NBT string list.