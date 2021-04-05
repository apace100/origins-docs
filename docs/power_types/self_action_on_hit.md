---
title: Self Action On Hit (Power Type)
date: 2021-04-04
---
# Self Action On Hit

[Power Type](../power_types.md).

Executes an entity action on the player when the player hits another entity.

Type ID: `origins:self_action_on_hit`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | | The action to execute on the player.
`cooldown` | [Integer](../data_types/integer.md) | | Interval of ticks this power needs to recharge before the action can be executed again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | _optional_ | If set, the cooldown of this power is visualized on the HUD in the specified way.
`damage_condition` | [Damage Condition](../damage_conditions.md) | _optional_ | If set, the action will only trigger when this condition holds for the damage that was dealt by the player.
`target_condition` | [Target Condition](../entity_conditions.md) | _optional_ | If set, the action will only be triggered when a target matching this condition is hit.

### Example
```json
{
  	"type": "origins:self_action_on_hit",
  	"entity_action": {
    	"type": "origins:heal",
    	"amount": 8.0
  	},
  	"damage_condition": {
    	"type": "origins:amount",
    	"comparison": ">=",
    	"compare_to": 10.0
  	},
  	"cooldown": 20
}
```
When a player with this power manages to deal 5 hearts or more damage in a single hit, they will heal for 4 hearts.
