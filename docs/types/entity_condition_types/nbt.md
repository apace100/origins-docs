---
title: NBT (Entity Condition Type)
date: 2021-10-02
---

# NBT

[Entity Condition Type](../entity_condition_types.md)

Checks the entity's NBT.

Type ID: `apoli:nbt`

!!! caution

    This condition is only effective server-side. That means client-side power types such as [`apoli:climbing`](../power_types/climbing.md), [`apoli:entity_glow`](../power_types/entity_glow.md), [`apoli:shader`](../power_types/shader.md), etc. won't work with this.    


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`nbt` | [String](../data_types/string.md) | | The NBT data to check for.


### Examples

```json
"condition": {
    "type": "apoli:nbt",
    "nbt": "{Tags: ['example_tag']}"
}
```

This example will check if the entity has the `example_tag` added via `/tag` or by modifying the entity's `Tags` NBT string list.
