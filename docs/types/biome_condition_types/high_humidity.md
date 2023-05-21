---
title: High Humidity (Biome Condition Type)
date: 2021-04-05
---

# High Humidity

[Biome Condition Type](../biome_condition_types.md)

Checks whether the biome counts as an area with high humidity (downfall value of > 0.85).

!!! note
    
    If you want functional equality to fire burning out quicker (which was defined via this value in previous Minecraft versions), you should check for the biome tag `minecraft:increased_fire_burnout` with an [In Tag (Biome Condition Type](in_tag.md) instead.

Type ID: `origins:high_humidity`


### Fields

_None._


### Examples

```json
"biome_condition": {
    "type": "origins:high_humidity"
}
```