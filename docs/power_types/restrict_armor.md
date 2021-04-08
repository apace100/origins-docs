---
title: Restrict Armor (Power Type)
date: 2021-04-07
---
# Restrict Armor

[Power Type](../power_types.md).

Blocks the player from equipping items as armor (via right-click, from dispensing, and by dragging them over in the inventory). Does **NOT** support a `condition`, use [Conditioned Restrict Armor](conditioned_restrict_armor.md) instead if you need one.

Type ID: `origins:restrict_armor`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`head` | [Item Condition](../item_conditions.md) | _optional_ | If set, items which satisfy this condition can not be equipped in the head slot.
`chest` | [Item Condition](../item_conditions.md) | _optional_ | If set, items which satisfy this condition can not be equipped in the chest slot.
`legs` | [Item Condition](../item_conditions.md) | _optional_ | If set, items which satisfy this condition can not be equipped in the legs slot.
`feet` | [Item Condition](../item_conditions.md) | _optional_ | If set, items which satisfy this condition can not be equipped in the feet slot.

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
