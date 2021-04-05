---
title: Action Over Time (Power Type)
date: 2021-04-04
---
# Action Over Time

[Power Type](../power_types.md).

Executes an entity or item action when the player finishes using an item (such as eating food or drinking a potion).

Type ID: `origins:action_on_item_use`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`interval` | [Integer](../data_types/integer.md) | | Interval of ticks between subsequent executions of the action.
`entity_action` | [Entity Action](../entity_actions.md) | _optional_ | The action to execute on the player each interval.
`rising_action` | [Entity Action](../entity_actions.md) | _optional_ | The action to execute on the first interval tick in which the condition became true.
`falling_action` | [Entity Action](../entity_actions.md) | _optional_ | The action to execute on the first interval tick in which the condition became false.

### Example
```json
{
  	"type": "origins:action_over_time",
  	"entity_action": {
    	"type": "origins:set_on_fire",
    	"duration": 4
  	},
  	"interval": 20,
  	"condition": {
    	"type": "origins:on_fire"
  	}
}
```
When a player with this power is burning, the power will set the player on fire for 4 seconds every second. Effectively, this power makes players burn forever once set on fire, unless they extinguish themselves by stepping in water.
