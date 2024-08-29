---
title: Entity Type Tag-like (Data Type)
date: 2023-06-27
---

#   Entity Type Tag-like

[Data Type](../data_types.md)

Entity Type Tag-likes are an [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) that refers to an entity type or an entity type tag (if prefixed with `#`), similar to how entries in a tag are defined.


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
