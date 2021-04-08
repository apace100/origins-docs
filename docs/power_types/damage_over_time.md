---
title: Damage Over Time (Power Type)
date: 2021-04-08
---
# Damage Over Time

[Power Type](../power_types.md).

While this power is active, the player will receive damage in regular intervals.

Type ID: `origins:damage_over_time`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`interval` | [Integer](../data_types/integer.md) | | Duration of ticks to wait between the damage.
`onset_delay` | [Integer](../data_types/integer.md) | _optional_ | How many ticks the power has to be active in order to apply the first damage. If not set, this will be equal to `interval`.
`damage` | [Float](../data_types/float.md) | | How much damage will be dealt each interval.
`damage_easy` | [Float](../data_types/float.md) | _optional_ | How much damage will be dealt each interval on Easy difficulty. If not set, this will be equal to `damage`.
`damage_source` | [Damage Source](../data_types/damage_source.md) | _optional_ | If set, this is the damage source that will be used to deal the damage.
`protection_enchantment` | [Identifier](../data_types/identifier.md) | _optional_ | If set, the total amount of levels of this enchantment will be counted on the player's armor to increase the `onset_delay`.
`protection_effectiveness` | [Float](../data_types/float.md) | 1.0 | If `protection_enchantment` is set, this multiplier scales how effective it will be (1.0 = time the `onset_delay` is increased is the same as with Hydrophobia and Water Protection).

### Example
```json
{
  	"type": "origins:damage_over_time",
  	"interval": 20,
  	"onset_delay": 1,
  	"damage": 2,
  	"damage_easy": 1,
  	"damage_source": {
    	"name": "hurt_by_water",
    	"unblockable": true,
    	"bypasses_armor": true
  	},
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
This power will deal damage to the player when in water.
