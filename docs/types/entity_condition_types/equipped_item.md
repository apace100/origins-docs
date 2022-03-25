---
title: Equipped Item (Entity Condition Type)
date: 2021-04-04
---

# Equipped Item

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity has an item equipped in the specified equipment slot that fulfills the specified [Item Condition Type](../item_condition_types.md).

Type ID: `apoli:equipped_item`

### Fields

| Field            | Type                                              | Default | Description                                                                                                                        |
| ---------------- | ------------------------------------------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `equipment_slot` | [String](../data_types/string.md)                 |         | Determines which equipment slot to check for the item. Accepts `"mainhand"`, `"offhand"`, `"head"`, `"chest"`, `"legs"`, `"feet"`. |
| `item_condition` | [Item Condition Type](../item_condition_types.md) |         | The item condition type to check for on the item in the specified equipment slot.                                                  |

### Examples

```json
"condition": {
    "type": "apoli:equipped_item",
    "equipment_slot": "mainhand",
    "item_condition": {
        "type": "apoli:harvest_level",
        "comparison": ">=",
        "compare_to": 2
    }
}
```

This example will check if the item in the entity's mainhand has a harvest level of 2 or more.
