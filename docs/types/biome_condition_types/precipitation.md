---
title: Precipitation (Biome Condition Type)
date: 2021-04-05
---

# Precipitation

[Biome Condition Type](../biome_condition_types.md)

Checks for the precipitation type of the biome the entity is currently in.

Type ID: `origins:precipitation`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`precipitation` | [String](../data_types/string.md) | |  Which precipitation the biome has to have in order to succeed the check. One of `none`, `rain` and `snow`.


### Examples

```json
"condition": {
    "type": "origins:biome",
    "condition": {
        "type": "origins:precipitation",
        "precipitation": "snow"
    }
}
```

This example will check if the biome the entity is currently in has a snowy precipitation. (e.g: `minecraft:snowy_taiga`, `minecraft:ice_spikes`, etc.)