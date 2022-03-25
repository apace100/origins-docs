---
title: Self Action When Hit (Power Type)
date: 2021-04-04
---

# Self Action When Hit

[Power Type](../power_types.md)

Executes an [Entity Action Type](../entity_action_types.md) on the entity that has the power when the entity takes damage.

Type ID: `apoli:self_action_when_hit`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | | The action to execute on the entity.
`cooldown` | [Integer](../data_types/integer.md) | | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | _optional_ | If specified, determines how the cooldown of this power is visualized on the HUD.
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the specified action will only execute if the damage taken fulfills this condition.


### Examples
```json
{
	"type": "apoli:self_action_when_hit",
	"entity_action": {
		"type": "apoli:apply_effect",
		"effect": {
		    "effect": "minecraft:regeneration",
      		"amplifier": 1,
      		"duration": 200
    	}
  	},
  	"damage_condition": {
    	"type": "apoli:amount",
    	"comparison": ">=",
    	"compare_to": 6.0
  	},
  	"cooldown": 1200
}
```
When a player with this power is damaged by 3 hearts or more damage in a single hit, they gain a Regeneration II effect for 10 seconds. This has a cooldown of one minute.
