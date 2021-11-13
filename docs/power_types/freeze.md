---
title: Freeze (Power Type)
date: 2021-10-02
---

# Freeze

[Power Type](../power_types.md)

Freezes the entity that has the power, as if they're in a Powdered Snow block.

Type ID: `origins:freeze`

### Fields

_None._


### Examples
```json
{
    "type": "origins:freeze"
}
```
Freezes the entity that has the power.
<br>

```json
{
    "type": "origins:freeze",
    "condition": {
        "type": "origins:biome",
        "condition": {
            "type": "origins:precipitation",
            "precipitation": "snow"
        }
    }
}
```
Freezes the entity that has the power if the entity is in a biome that snows.