---
title: NBT (Entity Condition Type)
date: 2021-10-02
---

# NBT

[Entity Condition Type](../entity_condition_types.md)

Checks the entity's NBT.

Type ID: `origins:nbt`

!!! caution

    Be cautious of using this entity condition type, as some NBT data *(e.g: tags added via `/tag`)* from the server are not synchronized to the client.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`nbt` | [NBT](../data_types/nbt.md) | | The NBT data to check for.


### Examples

```json
"condition": {
    "type": "origins:nbt",
    "nbt": "{Tags: ['example_tag']}"
}
```

This example will check if the entity has the `example_tag` added via `/tag` or by modifying the entity's `Tags` NBT string list.
