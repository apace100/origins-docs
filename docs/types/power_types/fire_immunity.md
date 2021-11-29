---
title: Fire Immunity (Power Type)
date: 2021-04-08
---

# Fire Immunity

[Power Type](../power_types.md)

Grants full fire immunity (meaning not only do you take no damage from fire sources, you also can not be set on fire).

Type ID: `origins:fire_immunity`


### Fields

_None._



### Examples

```json
{
    "type": "origins:fire_immunity",
    "condition": {
        "type": "origins:equipped_item",
        "equipment_slot": "mainhand",
        "item_condition": {
            "type": "origins:ingredient",
            "ingredient": {
                "item": "minecraft:magma_block"
            }
        }
    }
}
```

This example will grant immunity to fire if the entity is holding a Magma Block in their mainhand.
