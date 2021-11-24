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
`entity_action` | [Entity Action](../entity_actions.md) | | The action to execute on the entity that has been hit.
`cooldown` | [Integer](../types/data_types/integer.md) | | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](../types/data_types/hud_render.md) | _optional_ | If specified, determines how the cooldown of this power is visualized on the HUD.
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If specified, the specified action will only execute if the damage dealt by the entity that has the power fulfills this condition.
`target_condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If specified, the specified action will only execute if the entity that has been hit fulfills this condition.

### Example
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
When a player with this power hits another entity, they will apply a strong slowness effect on the enemy for 5 seconds. This effect has a cooldown of 10 seconds, so you can't easily stack it on a single enemy! In order to give the player an indication of when this power is ready again, a `hud_render` was specified.
