---
title: Entity Type Tag-like (Data Type)
date: 2023-06-27
---

#   Entity Type Tag-like

[Data Type](../data_types.md)

An [array](array.md) of either [identifiers](identifier.md) or [objects](object.md) that refers to an entity type or an entity type tag (if prefixed with `#`), similar to how entries in a tag are defined.


### Examples

```json
"entity_types": [
    "minecraft:dolphin"
]
```
This example defines an entity type tag-like that contains the `minecraft:dolphin` entity type.
<br>

```json
"entity_types": [
    "#minecraft:fall_damage_immune",
    "#minecraft:skeletons",
    "minecraft:creeper"
]
```
This example defines an entity type tag-like that contains the `#minecraft:fall_damage_immune` and `#minecraft:skeletons` entity type tags, and the `minecraft:creeper` entity type.
<br>

```json
"entity_types": [
    {
        "id": "#example:is_creepy",
        "required": false
    },
    "minecraft:creeper"
]
```
This example defines an entity type tag-like that contains the `#example:is_creepy` (without causing an error if the data pack that adds the said tag is absent), and the `minecraft:creeper` entity type.
