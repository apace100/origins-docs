---
title: Active Self (Power Type)
date: 2021-04-04
---

# Active Self

[Power Type](../power_types.md)

Executes an [Entity Action Type](../entity_action_types.md) on the entity that has the power upon pressing the specified [Key](../data_types/key.md).

Type ID: `apoli:active_self`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | | The action to execute on the player.
`cooldown` | [Integer](../data_types/integer.md) | `1` | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | `{"should_render": false}` | Determines how the cooldown of this power is visualized on the HUD.
`key` | [Key](../data_types/key.md) | `{"key": "none"}` | Which active key this power should respond to.


### Examples

```json
{
	"type": "apoli:active_self",
	"entity_action": {
		"type": "apoli:if_else",
		"condition": {
	    	"type": "apoli:on_fire"
    	},
    	"if_action": {
    		"type": "apoli:extinguish"
    	},
    	"else_action": {
    		"type": "apoli:set_on_fire",
    		"duration": 8
    	}
  	},
  	"cooldown": 20,
  	"hud_render": {
    	"should_render": false
  	}
}
```

This example will set the player on fire for 8 seconds, or extinguish themselves if they're already on fire upon pressing the Primary ability key.
<br>

```json
{
	"type": "apoli:active_self",
	"entity_action": {
		"type": "apoli:and",
		"actions": [
			{
				"type": "apoli:equipped_item_action",
				"equipment_slot": "mainhand",
				"action": {
					"type": "apoli:consume",
					"amount": 1
				}
			},
			{
				"type": "apoli:apply_effect",
				"effect": {
					"effect": "minecraft:speed",
					"duration": 100,
					"amplifier": 1,
					"is_ambient": true,
					"show_particles": true,
					"show_icon": true
				}
			}
		]
	},
	"cooldown": 1,
	"hud_render": {
		"should_render": false
	},
	"key": {
		"key": "key.use",
		"continuous": true
	},
	"condition": {
		"type": "apoli:equipped_item",
		"equipment_slot": "mainhand",
		"item_condition": {
			"type": "apoli:ingredient",
			"ingredient": {
				"item": "minecraft:sugar"
			}
		}
	}
}
```

This example will allow the player that has the power to essentially consume a Sugar item if the player is holding a Sugar item, which would then apply a Speed II status effect that would last for 5 seconds upon pressing the `key.use` keybind.
(The example is bound to the `key.use` keybind, as seen inside the [`key`](../data_types/key.md) object field.)
