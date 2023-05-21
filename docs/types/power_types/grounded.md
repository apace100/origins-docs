---
title: Grounded (Power Type)
date: 2023-05-21
---

# Grounded

[Power Type](../power_types.md)

An entity with this power counts as being "on ground", meaning regular walking mechanics can occur even if the entity isn't physically on a block.

Type ID: `origins:grounded`


### Fields

_None._



### Examples

```json
{
    "type": "origins:grounded"
}
```

The most basic example - always counts the player as being on the ground, allowing them to jump even while in the air.
<br>

```json
{
    "type": "origins:multiple",
    "activate": {
        "type": "origins:active_self",
        "key": {
			"key": "key.origins.primary_active"
		},
		"cooldown": 200,
		"entity_action": {
			"type": "origins:trigger_cooldown",
			"power": "*:*_duration"
		}
    },
    "duration": {
        "type": "origins:cooldown",
        "cooldown": 120,
        "hud_render": {
			"bar_index": 5
		}
    },
	"effect_grounded": {
		"type": "origins:grounded",
		"condition": {
			"type": "apoli:resource",
			"resource": "*:*_duration",
			"comparison": ">",
			"compare_to": 0
		}
	},
	"effect_no_velocity": {
		"type": "origins:modify_velocity",
		"axes": ["y"],
		"modifier": {
			"operation": "set_total",
			"value": 0
		},
		"condition": {
			"type": "origins:resource",
			"resource": "*:*_duration",
			"comparison": ">",
			"compare_to": 0
		}
	}
}
```

A combination of powers which allows the player to walk on air (neither jump nor fall) for a short duration when they use their primary ability key.
