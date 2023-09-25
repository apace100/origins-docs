---
title: Entity Group (Power Type)
date: 2021-07-13
---

# Entity Group

[Power Type](../power_types.md)

Defines the entity group of the entity that has the power.

Type ID: `origins:entity_group`

!!! note

    See [Minecraft Wiki: Mob (Classification)](https://minecraft.wiki/w/Mob#Classification) for more information about entity groups.

!!! note

    This power type is mostly used for determining the enchantment bonus damage towards the entity that has the power. That being said, there should only be one power that uses this power type.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`group` | [String](../data_types/string.md) | | The group to associate with the player. One of `default`, `undead`, `arthropod`, `illager`, or `aquatic`.


### Examples

```json
{
    "type": "origins:entity_group",
	"group": "arthropod"
}
```

This example will classify the entity that has the power as an arthropod, meaning that they will take more damage from the Bane of Arthropods enchantment.
