---
title: Temperature (Biome Condition Type)
date: 2021-04-05
---

# Temperature

[Biome Condition Type](../biome_condition_types.md)

Checks for the temperature of a biome.

Type ID: `origins:temperature`

!!! note

    You can visit [Minecraft Fandom: Biome (List of Overworld climates)](https://minecraft.fandom.com/wiki/Biome#List_of_Overworld_climates) for a list of temperature values for the vanilla biomes.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How the temperature should be compared to the specified value.
`compare_to` | [Float](../data_types/float.md) | | Which value the temperature should be compared to.

### Example:
```json
"condition": {
    "type": "origins:biome",
    "condition": {
        "type": "origins:temperature",
        "comparison": ">=",
        "compare_to": 2
    }
}
```
This example checks if the biome the player is currently in has a temperature of 2 or more. (e.g: `minecraft:badlands`, `minecraft:desert`, etc.)
