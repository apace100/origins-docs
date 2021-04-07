---
title: Active Self (Power Type)
date: 2021-04-04
---
# Active Self

[Power Type](../power_types.md).

Executes an entity action on the player when the player uses a specified [Key](../data_types/key.md) (default: G).

Type ID: `origins:active_self`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action](../entity_actions.md) | | The action to execute on the player.
`cooldown` | [Integer](../data_types/integer.md) | | Interval of ticks this power needs to recharge before the action can be executed again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | | Determines how the cooldown of this power is visualized on the HUD.
`key` | [Key](../data_types/key.md) | `{"key": "key.origins.primary_active"}` | Which active key this power should respond to.

### Example

```json
{
	"type": "origins:active_self",
	"entity_action": {
		"type": "origins:if_else",
		"condition": {
	    	"type": "origins:on_fire"
    	},
    	"if_action": {
    		"type": "origins:extinguish"
    	},
    	"else_action": {
    		"type": "origins:set_on_fire",
    		"duration": 8
    	}
  	},
  	"cooldown": 20,
  	"hud_render": {
    	"should_render": false
  	}
}
```
This power allows players to press G in order to set themselves on fire for 8 seconds, or, if they are already burning, extinguish themselves.
