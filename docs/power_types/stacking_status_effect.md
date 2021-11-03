---
title: Stacking Status Effect (Power Type)
date: 2021-04-08
---

# Stacking Status Effect

[Power Type](../power_types.md)

When reaching more than 0 stacks, the player will receive the provided status effects.

Type ID: `origins:stacking_status_effect`

!!! note

    This power gains or loses 1 stack per set tick rate if the power is active or inactive respectively.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`min_stacks` | [Integer](../data_types/integer.md) | | The minimum number of stacks. Negative numbers are allowed.
`max_stacks` | [Integer](../data_types/integer.md) | | The maximum number of stacks.
`duration_per_stack` | [Integer](../data_types/integer.md) | | When the status effects are applied, their duration will be `stacks * duration_per_stack` in ticks.
`tick_rate` | [Integer](../data_types/integer.md) | 10 | Determines how fast one will gain/lose stacks in ticks.
`effect` | [Status Effect Instance](../data_types/status_effect_instance.md) | _optional_ | If set, this status effect will be applied by this power.
`effects` | [Array](../data_types/array.md) of [Status Effect Instances](../data_types/status_effect_instance.md) | _optional_ | If set, these status effects will be applied by this power.

### Example
```json
{
  	"type": "origins:stacking_status_effect",
  	"min_stacks": -20,
  	"max_stacks": 361,
  	"duration_per_stack": 10,
  	"effects": [
    	{
      		"effect": "minecraft:weakness",
      		"is_ambient": true,
      		"show_particles": false,
      		"show_icon": true
    	},
    	{
      		"effect": "minecraft:slowness",
      		"is_ambient": true,
      		"show_particles": false,
      		"show_icon": true
    	}
  	],
  	"condition": {
    	"type": "origins:block_collision",
    	"offset_x": 0,
    	"offset_y": 1,
    	"offset_z": 0
  	}
}
```
This example makes the player weak and slow after being under a low ceiling for a while. (Yes, it's the Elytrian's claustrophobia power.)
<br>

```json
{
    "type": "origins:stacking_status_effect",
    "min_stacks": -2,
    "max_stacks": 5,
    "duration_per_stack": 20,
    "tick_rate": 20,
    "effect": {
        "effect": "minecraft:blindness",
        "is_ambient": true,
        "show_particles": true,
        "show_icon": true
    },
    "condition": {
        "type": "origins:exposed_to_sun"
    }
}
```
This example makes the player blind after being exposed to the sun for at least 4 seconds.