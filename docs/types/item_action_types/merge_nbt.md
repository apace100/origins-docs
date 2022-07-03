---
title: Merge NBT (Item Action Type)
date: 2022-07-03
---

#   Merge NBT

[Item Action Type](../item_action_types.md)

Merges the specified NBT to the item's NBT.

Type ID: `origins:merge_nbt`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`nbt` | [String](../data_types/string.md) | | The NBT to merge to the item's NBT.


### Examples

```json
"item_action": {
    "type": "origins:merge_nbt",
    "nbt": "{custom_stuff: 1b}"
}
```

This example will merge the `{custom_stuff: 1b}` NBT to the item's NBT.
