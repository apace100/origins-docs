---
title:  Food Effect Entry (Data Type)
date:   2026-04-23
---

#   Food Effect Entry

[Data Type](../data_types.md)

An [object](object.md) used to define the effect to be applied (at a probability) when consuming an item stack.


### Fields

Field           |   Type                                                |   Default |   Description
----------------|-------------------------------------------------------|-----------|--------------
`effect`        |   [Status Effect Instance](status_effect_instance.md) |           |   The effect to apply upon consumption.
`probability`   |   [Float](float.md)                                   |   `1.0`   |   The probability of applying the specified effect.


### Examples

```json
"effect": {
    "effect": {
        "id": "minecraft:regeneration",
        "duration": 200
    },
    "probability": 0.5
}
```
This example will apply Regeneration I (that will last for 10 seconds) at a 50% chance when consuming the item stack.
<br>

```json
"effects": [
    {
        "effect": {
            "id": "minecraft:poison",
            "duration": 100,
            "amplifier": 1
        },
        "probability": 0.5
    },
    {
        "effect": {
            "id": "minecraft:blindness",
            "duration": 100
        },
        "probability": 0.25
    }
]
```
This example will apply Poison II (that will last for 5 seconds) at a 50% chance, and/or Blindness I (that will last for 5 seconds) at a 25% chance.
