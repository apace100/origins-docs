---
title: NBT (Item Condition Type)
date: 2021-10-02
---

# NBT

[Item Condition Type](../item_condition_types.md)

Checks the item's NBT.

Type ID: `origins:nbt`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`nbt` | [NBT](../data_types/nbt.md) | | The NBT data to check for.


### Examples

```json
"item_condition": {
    "type": "origins:nbt",
    "nbt": "{exampleCustomTag: 1b}"
}
```

This example will check if the item stack has the `exampleCustomTag: 1b` NBT.
