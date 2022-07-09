---
title: Stacking Status Effect (Power Type)
date: 2021-04-08
---

# Stacking Status Effect

[Power Type](../power_types.md)

Provides a system where the entity that has the power gains/loses a stack per specified interval if the power is active or inactive respectively. If the stack count is greater than 0, the specified status effect(s) will be applied to the entity.

Type ID: `origins:stacking_status_effect`

!!! note

    The actual duration of the specified status effect(s) is determined by the `stacks * duration_per_stack` formula.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`min_stacks` | [Integer](../data_types/integer.md) | | The minimum number of stacks. Negative numbers are allowed.
`max_stacks` | [Integer](../data_types/integer.md) | | The maximum number of stacks.
`duration_per_stack` | [Integer](../data_types/integer.md) | | Determines the duration of the specified status effect(s) for each stack.
`tick_rate` | [Integer](../data_types/integer.md) | `10` | Determines how fast the power will gain/lose stacks in ticks.
`effect` | [Status Effect Instance](../data_types/status_effect_instance.md) | _optional_ | If specified, this status effect will be applied on the entity that has the power.
`effects` | [Array](../data_types/array.md) of [Status Effect Instances](../data_types/status_effect_instance.md) | _optional_ | If specified, these status effects will be applied on the entity that has the power.


### Examples

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

This example will apply the Weakness I and Slowness I status effects that would last for 1 second to the entity that has the power if the entity is under a low ceiling.
<br>

```json
{
    "type": "origins:stacking_status_effect",
    "min_stacks": -3,
    "max_stacks": 1,
    "duration_per_stack": 100,
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

This example will apply the Blindness I status effect that would last for 5 seconds after being exposed to the sun for at least 4 seconds.
