---
title: Equipped Item
date: 2021-04-04
---
# Equipped Item

[Entity Condition](../entity_conditions.md).

Checks whether the player has an item equipped in a specific slot which matches a provided item condition.

Type ID: `origins:equipped_item`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`equipment_slot` | [String](../data_types/string.md) | |  Which equipped item to check. One of: `"mainhand"`, `"offhand"`, `"head"`, `"chest"`, `"legs"`, `"feet"`.
`item_condition` | [Item Condition](../item_conditions.md) | |  Which condition will be applied to the item in the specified slot.

### Example:

```json
"condition": {
  "type": "origins:equipped_item",
  "equipment_slot": "mainhand",
  "item_condition": {
    "type": "origins:harvest_level",
    "comparison": ">=",
    "compare_to": 2
  }
}
```

This condition checks whether the player is holding a tool or weapon of iron material or better in the mainhand (as defined per the harvest level).
