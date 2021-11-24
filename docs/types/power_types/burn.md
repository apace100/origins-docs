---
title: Burn (Power Type)
date: 2021-04-07
---

# Burn

[Power Type](../power_types.md)

Sets the entity that has the power on fire within the specified interval.

Type ID: `origins:burn`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`interval` | [Integer](../types/data_types/integer.md) |  | Interval between being set on fire, in ticks.
`burn_duration` | [Integer](../types/data_types/integer.md) |  | Determines how long the fire should last on the entity each time it is set, in seconds.


### Example
```json
{
    "type": "origins:burn",
    "interval": 20,
    "burn_duration": 1,
    "condition": {
        "type": "origins:equipped_item",
        "equipment_slot": "head",
        "item_condition": {
            "type": "origins:ingredient",
            "ingredient": {
                "item": "minecraft:leather_helmet"
            }
        },
        "inverted": true
    }
}
```
This power will only burn the player for 1 second, within a 20 ticks interval if the said player is not wearing a leather helmet.