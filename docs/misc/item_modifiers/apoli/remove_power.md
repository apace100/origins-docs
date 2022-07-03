---
title: Remove Power (Apoli) (Item Modifier)
date: 2022-07-03
---

#   Remove Power (Apoli)

[Item Modifier](../../item_modifiers.md)

Removes a power from an item stack.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | [Identifier](../../../types/data_types/identifier.md) | | The namespace and ID of the power that will be removed from the item.
`slot` | [String](../../../types/data_types/string.md) | | The equipment slot to remove the power from.


### Examples

```json
{
    "function": "apoli:remove_power",
    "power": "origins:arcane_skin",
    "slot": "chest"
}
```

This example will remove the `origins:arcane_skin` power from the item if it's applicable to the `"chest"` equipment slot.
