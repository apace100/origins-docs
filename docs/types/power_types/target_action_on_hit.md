---
title: Target Action On Hit (Power Type)
date: 2021-04-04
---

# Target Action On Hit

[Power Type](../power_types.md)

Executes an entity action on every entity that is hit by the entity that has the power.

Type ID: `origins:target_action_on_hit`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | | The action to execute on the entity that has been hit.
`cooldown` | [Integer](../data_types/integer.md) | `1` | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | _optional_ | If specified, determines how the cooldown of this power is visualized on the HUD.
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the specified action will only execute if the damage dealt by the entity that has the power fulfills this condition.
`target_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified, the specified action will only execute if the entity that has been hit fulfills this condition.


### Examples

```json
{
  	"type": "origins:target_action_on_hit",
  	"entity_action": {
    	"type": "origins:apply_effect",
    	"effect": {
      		"effect": "minecraft:slowness",
      		"amplifier": 3,
      		"duration": 100
    	}
  	},
  	"cooldown": 200,
  	"hud_render": {
    	"should_render": true,
    	"bar_index": 5
  	}
}
```

This example will apply a Slowness IV status effect on the target entity that would last for 5 seconds for every 10 seconds of usage.
