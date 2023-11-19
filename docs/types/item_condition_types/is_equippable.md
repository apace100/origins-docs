---
title: Is Equippable
date: 2022-07-03
---

#   Is Equippable

[Item Condition Type](../item_condition_types.md)

Checks if the item is equippable.

Type ID: [`origins:is_equippable`](## "Aliases: ["origins:equippable"]")


### Fields

Field | Type | Default | Description
------|------|---------|------------
equipment_slot | [String](../data_types/string.md) | *optional* | If specified, checks if the item is equippable in the specified equipment slot. Accepts `"head"`, `"chest"`, `"legs"`, `"feet"`, or `"offhand"`.


### Examples

```json
"item_condition": {
    "type": "origins:is_equippable"
}
```

This example will check if the item is generally equippable.
<br>

```json
"item_condition": {
    "type": "origins:is_equippable",
    "equipment_slot": "chest"
}
```

This example will check if the item can be equipped in the chest equipment slot.
