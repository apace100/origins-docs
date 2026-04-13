---
title: Modify Type Tag (Power Type)
date: 2026-04-13
---

# Modify Type Tag

[Power Type](../power_types.md)

Modifies whether an entity is effectively included in a specific entity type tag.

### Fields

| Field | Type                                      | Default | Description                                                             |
| -------| -------------------------------------------| ---------| -------------------------------------------------------------------------|
| `tag` | [Identifier](../data_types/identifier.md) |         | The ID of the entity type tag to consider the entity to be included in. |

### Examples

```json
{
    "type": "origins:modify_type_tag",
    "tag": "minecraft:undead"
}
```
This example will effectively include the entity in the `#minecraft:undead` (`data/minecraft/tags/entity_type/undead.json`) entity type tag.
<br>

```json
{
    "type": "origins:modify_type_tag",
    "tag": "minecraft:powder_snow_walkable_mobs",
    "condition": {
        "type": "apoli:sprinting"
    }
}
```
This example will effectively include the entity in the `#minecraft:powder_snow_walkable_mobs` (`data/minecraft/tags/entity_type/powder_snow_walkable_mobs.json`) entity type tag **only if the entity is sneaking**.
