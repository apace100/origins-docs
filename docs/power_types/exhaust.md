---
title: Exhaust (Power Type)
date: 2021-04-08
---
# Exhaust

[Power Type](../power_types.md).

Applies exhaustion to the player over time.

Type ID: `origins:exhaust`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`interval` | [Integer](../data_types/integer.md) | | Duration of ticks to wait between applying exhaustion.
`exhaustion` | [Float](../data_types/float.md) | | How much exhaustion will be applied each interval.

### Example
```json
{
  	"type": "origins:exhaust",
  	"interval": 20,
  	"exhaustion": 4.0,
	"condition": {
		"type": "origins:fluid_height",
		"fluid": "minecraft:water",
		"comparison": ">",
		"compare_to": 0.0
	}
}
```
This power will quickly exhaust the player if they are touching water.
