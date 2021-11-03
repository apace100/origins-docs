---
title: Freeze (Power Type)
date: 2021-10-02
---

# Freeze

[Power Type](../power_types.md)

Freezes the player, as if they're in a Powdered Snow block.

Type ID: `origins:freeze`

### Fields

_None._


### Examples
```json
{
    "type": "origins:freeze"
}
```
Freezes the player.
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
Freezes the player if the player in question is in a biome that snows.