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
`cooldown` | [Integer](../data_types/integer.md) | `1` | Interval of ticks this power needs to recharge before the action can be executed again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | `{"should_render": false}` | Determines how the cooldown of this power is visualized on the HUD.
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
<br>

```json
{
	"type": "origins:active_self",
	"entity_action": {
		"type": "origins:and",
		"actions": [
			{
				"type": "origins:equipped_item_action",
				"equipment_slot": "mainhand",
				"action": {
					"type": "origins:consume",
					"amount": 1
				}
			},
			{
				"type": "origins:apply_effect",
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
		"type": "origins:equipped_item",
		"equipment_slot": "mainhand",
		"item_condition": {
			"type": "origins:ingredient",
			"ingredient": {
				"item": "minecraft:sugar"
			}
		}
	}
}
```

This example allows the player to consume a sugar item, which would apply a Speed II status effect that would last for 5 seconds. The example is bound to the `key.use` keybind, as seen inside the [`key`](../data_types/key.md) object field.
