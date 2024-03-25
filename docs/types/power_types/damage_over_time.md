---
title: Damage Over Time (Power Type)
date: 2021-04-08
---

# Damage Over Time

[Power Type](../power_types.md)

Inflicts damage on the entity that has the power from a specified damage source within the specified interval.

Type ID: `origins:damage_over_time`


!!! info

    See [Minecraft Wiki: Damage type](https://minecraft.wiki/w/Damage_type) and [Minecraft Wiki: Tags (Damage types)](https://minecraft.wiki/w/Tag#Damage_types) for more information about vanilla damage types and damage type tags.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`interval` | [Integer](../data_types/integer.md) | `20` | Duration of ticks to wait between the damage.
`onset_delay` | [Integer](../data_types/integer.md) | _optional_ | How many ticks the power has to be active in order to apply the first damage. If not set, this will be equal to `interval`.
`damage` | [Float](../data_types/float.md) | | How much damage will be dealt each interval.
`damage_easy` | [Float](../data_types/float.md) | _optional_ | How much damage will be dealt each interval on Easy difficulty. If not set, this will be equal to `damage`.
`damage_source` | [Damage Source](../data_types/damage_source.md) | <span style="color:darkred"><b>DEPRECATED</b></span> | Use `damage_type` instead. See [Damage Source (Data Type)](../data_types/damage_source.md) for more details.
`damage_type` | [Identifier](../data_types/identifier.md) | `apoli:damage_over_time` | Defines the properties of the damage source that will be dealt, such as part of its death message, and whether it can bypass armor, shield, etc. (via damage type tags.)
`protection_enchantment` | [Identifier](../data_types/identifier.md) | _optional_ | If set, the total amount of levels of this enchantment will be counted on the player's armor to increase the `onset_delay`.
`protection_effectiveness` | [Float](../data_types/float.md) | `1.0` | If `protection_enchantment` is set, this multiplier scales how effective it will be (1.0 = time the `onset_delay` is increased is the same as with Hydrophobia and Water Protection).


### Examples

```json
{
  	"type": "origins:damage_over_time",
  	"interval": 20,
  	"onset_delay": 1,
  	"damage": 2,
  	"damage_easy": 1,
  	"damage_type": "origins:hurt_by_water",
  	"protection_enchantment": "origins:water_protection",
  	"protection_effectiveness": 1.0,
  	"condition": {
    	"type": "origins:or",
    	"conditions": [
	      	{
	        	"type": "origins:fluid_height",
		        "fluid": "minecraft:water",
	        	"comparison": ">",
	        	"compare_to": 0.0
	      	},
	      	{
	        	"type": "origins:in_rain"
	      	}
    	]
  	}
}
```

This example will deal damage to the entity if the entity is in water.
