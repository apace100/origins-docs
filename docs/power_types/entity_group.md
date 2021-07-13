---
title: Entity Group (Power Type)
date: 2021-07-13
---
# Entity Group

[Power Type](../power_types.md).

Defines the entity group of the player, mostly used for determining enchantment bonus damage towards the player. A player should only have one of these powers.

Type ID: `origins:entity_group`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`group` | [String](../data_types/string.md) | | The group to associate with the player. One of `default`, `undead`, `arthropod`, `illager`, or `aquatic`. [See here for more information about the entity groups](https://minecraft.fandom.com/wiki/Mob#Classification)

### Example
```json
{
    "type": "origins:entity_group",
	"group": "arthropod"
}
```
This power marks the player as an arthropod, meaning they will take more damage from Bane of Arthropods.
