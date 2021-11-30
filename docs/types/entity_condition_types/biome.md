---
title: Biome (Entity Condition Type)
date: 2021-04-04
---

# Biome

[Entity Condition Type](../entity_condition_types.md)

Checks whether the entity is in a specified biome.

Type ID: `origins:biome`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`biome` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, only evaluate the condition to true if the biome the entity is in matches the specified namespace and ID.
`biomes` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, only evaluate the condition to true if the biome the entity is in matches one of the specified namespace and IDs.
`condition` | [Biome Condition Type](../biome_condition_types.md) | _optional_ | If specified, only evaluate the condition to true if the biome the entity is in fulfills the specified biome condition type.


### Examples

```json
"condition": {
    "type": "origins:biome",
    "biome": "minecraft:plains"
}
```

This example will check if the entity is currently in a Plains biome.
<br>

```json
"condition": {
    "type": "origins:biome",
    "condition": {
        "type": "origins:category",
        "category": "forest"
    }
}
```

This example will check if the entity is currently in a Forest-like biome.