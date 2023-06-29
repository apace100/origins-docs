---
title: Global Power Set (JSON Format)
date: 2023-06-27
---

#   Global Power Set JSON Format

This is the format of a JSON file describing a global power set. Global power sets are sets of powers that are granted to entities globally with the `apoli:global` power source. It can also be filtered so that the set of powers will only be granted to certain entities of certain type or entities included in a certain entity type tag.

Global Power Set JSON files need to be placed inside the `data/<namespace>/global_powers` folder of a datapack.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_types` | [Entity Type Tag-like](../types/data_types/entity_type_taglike.md) | _optional_ | If specified, the specified powers will only be granted to entities that fulfill this tag-like specifier.
`powers` | [Array](../types/data_types/array.md) of [Identifiers](../types/data_types/identifier.md) | | The ID(s) of the power(s) to grant to entities globally.
`order` | [Integer](../types/data_types/integer.md) | `0` | Determines the order at which the global power set is applied.


### Examples

```json
{
    "powers": [
        "origins:damage_from_snowball"
    ]
}
```

This example will grant the `origins:damage_from_snowball` power to all entities.
<br>

```json
{
    "entity_types": [
        "#minecraft:skeletons",
        "minecraft:creeper"
    ],
    "powers": [
        "origins:arcane_skin",
        "origins:like_water"
    ]
}
```

This example will apply the `origins:arcane_skin` and `origins:like_water` powers to Creepers and entities that are included in the `#minecraft:skeletons` entity type tag.
