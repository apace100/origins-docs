---
title: Restrict Armor (Power Type)
date: 2021-04-07
---

# Restrict Armor

[Power Type](../power_types.md)

Restricts the entity that has the power from equipping items as armor (via right-click, dispensing or by dragging and dropping the item in the equipment slot(s)) in the specified equipment slot(s).

Type ID: `origins:restrict_armor`

!!! note

    This power type does not support a `condition`. If the `condition` field is present, it will be ignored. If you wish to check for an entity condition before applying the restriction, you can use the [Conditioned Restrict Armor](conditioned_restrict_armor.md) power type instead.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`head` | [Item Condition](../item_conditions.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the head equipment slot.
`chest` | [Item Condition](../item_conditions.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the chest equipment slot.
`legs` | [Item Condition](../item_conditions.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the legs equipment slot.
`feet` | [Item Condition](../item_conditions.md) | _optional_ | If specified, items which fulfills this condition cannot be equipped in the feet equipment slot.

### Example
```json
{
    "type": "origins:restrict_armor",
    "head": {
        "type": "origins:armor_value",
        "comparison": ">",
        "compare_to": 2
    },
    "chest": {
        "type": "origins:armor_value",
        "comparison": ">",
        "compare_to": 5
    },
    "legs": {
        "type": "origins:armor_value",
        "comparison": ">",
        "compare_to": 4
    },
    "feet": {
        "type": "origins:armor_value",
        "comparison": ">",
        "compare_to": 1
    }
}
```
This power prevents the player from putting on any armor which is more powerful than chainmail.
