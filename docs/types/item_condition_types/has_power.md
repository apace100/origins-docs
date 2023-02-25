---
title: Has Power (Item Condition Type)
date: 2023-02-26
---

#   Has Power

[Item Condition Type](../item_condition_types.md)

Checks if the item has a power embedded to it.

Type ID: `origins:has_power`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | [Identifier](../data_types/identifier.md) | | The ID of the power to check for.
`slot` | [String](../data_types/string.md) | *optional* | If specified, this will check if the power embedded to the item is assigned to this equipment slot. Accepts one of `"head"`, `"chest"`, `"legs"`, `"feet"`, `"mainhand"` or `"offhand"`.


### Examples

```json
"item_condition": {
    "type": "origins:has_power",
    "power": "origins:water_breathing"
}
```

This example will check if the item has Merling's Gills *(`origins:water_breathing`)* power embedded to it.
<br>

```json
"item_condition": {
    "type": "origins:has_power",
    "power": "origins:elytra",
    "slot": "chest"
}
```

This example will check if the item has Elytrian's Winged *(`origins:elytra`)* power embedded to it.
