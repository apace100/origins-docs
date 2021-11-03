---
title: NBT (Item Condition)
date: 2021-10-02
---

# NBT

[Item Condition](../item_conditions.md)

Checks the item's NBT.

Type ID: `origins:nbt`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`nbt` | [String](../data_types/string.md) | | The NBT data to check for.

### Example
```json
"item_condition": {
    "type": "origins:nbt",
    "nbt": "{exampleCustomTag: 1b}"
}
```
This example checks if the item stack has the `exampleCustomTag: 1b` NBT.