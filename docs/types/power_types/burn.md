---
title: Burn (Power Type)
date: 2021-04-07
---

# Burn

[Power Type](../power_types.md)

Sets the entity that has the power on fire within the specified interval.

Type ID: `apoli:burn`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`interval` | [Integer](../data_types/integer.md) |  | Interval between being set on fire, in ticks.
`burn_duration` | [Integer](../data_types/integer.md) |  | Determines how long the fire should last on the entity each time it is set, in seconds.



### Examples

```json
{
    "type": "apoli:burn",
    "interval": 20,
    "burn_duration": 1,
    "condition": {
        "type": "apoli:equipped_item",
        "equipment_slot": "head",
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "item": "minecraft:leather_helmet"
            }
        },
        "inverted": true
    }
}
```

This example will set the entity on fire for 1 second, within an interval of 20 ticks if the said entity is not wearing a Leather Helmet.
