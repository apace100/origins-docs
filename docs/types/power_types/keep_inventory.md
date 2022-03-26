---
title: Keep Inventory (Power Type)
date: 2021-12-03
---

# Keep Inventory

[Power Type](../power_types.md)

Makes certain items persist in the entity's inventory.

Type ID: `origins:keep_inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, only make the items that fulfill the specified item condition type persist in the entity's inventory.
`slots` | [Array](../data_types/array.md) of [Integers](../data_types/integer.md) | _optional_ | If specified, only make the items that are in the listed inventory slots persist in the entity's inventory. See [Positioned Item Stack Slots](../../misc/extras/positioned_item_stack_slots.md) for possible values.


### Examples

```json
{
    "type": "origins:keep_inventory",
    "slots": [
        0,
        1,
        2,
        3,
        4,
        5,
        6,
        7,
        8
    ]
}
```

This example will make items in the hotbar slots persist.
