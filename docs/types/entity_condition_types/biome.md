---
title: Biome (Entity Condition Type)
date: 2021-04-04
---

# Biome

[Entity Condition Type](../entity_condition_types.md)

Checks whether the player is in a specific biome.

Type ID: `origins:biome`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`biome` | [Identifier](../data_types/identifier.md) | _optional_ |  If set, this is the ID of the biome the player needs to be in for this condition to evaluate to true, e.g. `minecraft:savanna`.
`biomes` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ |  If set, these are the allowed biome IDs the player can be in for this condition to evaluate to true.
`condition` | [Biome Condition](../biome_conditions.md) | _optional_ | If set, this condition needs to be fulfilled (in addition to having the right ID, if provided) by the biome in order for the condition to evaluate to true.

### Examples:
```json
"condition": {
    "type": "origins:biome",
    "biome": "minecraft:plains"
}
```
This example checks if the player is in a Plains biome.

```json
"condition": {
    "type": "origins:biome",
    "condition": {
        "type": "origins:category",
        "category": "forest"
    }
}
```
This example checks if the player is in a Forest-like biome.