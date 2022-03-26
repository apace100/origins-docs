---
title: Self Action On Hit (Power Type)
date: 2021-04-04
---

# Self Action On Hit

[Power Type](../power_types.md)

Executes an [Entity Action Type](../entity_action_types.md) on the entity that has the power when the entity hits another entity.

Type ID: `origins:self_action_on_hit`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | | The action to execute on the entity.
`cooldown` | [Integer](../data_types/integer.md) | | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | _optional_ | If specified, determines how the cooldown of this power is visualized on the HUD.
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, the specified action will only be executed if the damage dealt is fulfills this condition.
`target_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified, the specified actions will only be executed if the entity/entities that has been hit fulfills this condition.


### Examples

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

This example will restore 4 hearts of health of the entity that has the power if the entity manages to deal 5 or more hearts of damage.
