---
title: Self Action When Hit (Power Type)
date: 2021-04-04
---
# Self Action When Hit

[Power Type](../power_types.md).

Executes an entity action on the player when the player is hit by another entity.

Type ID: `origins:self_action_when_hit`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | | The action to execute on the player.
`cooldown` | [Integer](../data_types/integer.md) | | Interval of ticks this power needs to recharge before the action can be executed again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | _optional_ | If set, the cooldown of this power is visualized on the HUD in the specified way.
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If set, the action will only trigger when this condition holds for the damage that was dealt by the attacker.

### Example
```json
{
	"type": "origins:self_action_when_hit",
	"entity_action": {
		"type": "origins:apply_effect",
		"effect": {
		    "effect": "minecraft:regeneration",
      		"amplifier": 1,
      		"duration": 200
    	}
  	},
  	"damage_condition": {
    	"type": "origins:amount",
    	"comparison": ">=",
    	"compare_to": 6.0
  	},
  	"cooldown": 1200
}
```
When a player with this power is damaged by 3 hearts or more damage in a single hit, they gain a Regeneration II effect for 10 seconds. This has a cooldown of one minute.
