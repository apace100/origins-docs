---
title: Apply Effect (Entity Action Type)
date: 2021-04-05
---

# Apply Effect

[Entity Action Type](../entity_action_types.md)

Adds one or more status effects to the living entity. Does not have an effect on non-living entities.

Type ID: `origins:apply_effect`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [Status Effect Instance](../data_types/status_effect_instance.md) | _optional_ | If set, this status effect will be applied by this action.
`effects` | [Array](../data_types/array.md) of [Status Effect Instances](../data_types/status_effect_instance.md) | _optional_ | If set, these status effects will be applied by this action.


### Examples

```json
"entity_action": {
    "type": "origins:apply_effect",
    "effect": {
        "effect": "minecraft:speed",
        "duration": 400,
        "amplifier": 0
    }
}
```

This example will apply a Speed I status effect to the entity that would last for 20 seconds.
<br>

```json
"entity_action": {
	"type": "origins:apply_effect",
	"effects": [
		{
			"effect": "minecraft:slow_falling",
			"duration": 400,
			"is_ambient": false,
			"show_particles": false,
			"show_icon": true
		},
		{
			"effect": "minecraft:slowness",
			"duration": 400,
			"is_ambient": false,
			"show_particles": false,
			"show_icon": true
		}
	]
}
```
This example will apply both Slowness I and Slow Falling I status effects that lasts for 20 seconds.
