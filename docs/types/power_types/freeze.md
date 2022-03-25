---
title: Freeze (Power Type)
date: 2021-10-02
---

# Freeze

[Power Type](../power_types.md)

Freezes the entity that has the power, as if they're in a Powder Snow block.

Type ID: `apoli:freeze`


### Fields

_None._



### Examples

```json
{
    "type": "apoli:freeze"
}
```

This example will freeze the entity that has the power.
<br>

```json
{
    "type": "apoli:freeze",
    "condition": {
        "type": "apoli:biome",
        "condition": {
            "type": "apoli:precipitation",
            "precipitation": "snow"
        }
    }
}
```

This example will freeze the entity that has the power if the entity is in a biome that snows.
