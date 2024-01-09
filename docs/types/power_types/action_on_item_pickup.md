---
title: Action on Item Pickup (Power Type)
date: 2024-01-10
---


#	Action on Item Pickup

[Power Type](../power_types.md)

Execute actions upon picking up an item.

Type ID: `origins:action_on_item_pickup`


!!!	note

	In the context of this power type, the '**actor**' entity is the entity that may have thrown the item while the '**target**' entity is the entity that picked up the item.


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | *optional* | If specified, this bi-entity action will be executed on either or both the '**actor**' and '**target**' entities.
`item_action` | [Item Action Type](../item_action_types.md) | *optional* | If specified, this item action will be executed on the item that was picked up.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | *optional* | If specified, the actions will only be executed if this bi-entity condition is fulfilled by either or both the '**actor**' and '**target**' entities.
`item_condition` | [Item Condition Type](../item_condition_types.md) | *optional* | If specified, the actions will only be executed if this item condition is fulfilled by the item about to be picked up.
`priority` | [Integer](../data_types/integer.md) | `0` | Determines the execution priority of the powers that use this power type (in a low-to-high priority order.)


###	Examples

```json
{
	"type": "origins:action_on_item_pickup",
	"bientity_action": {
		"type": "origins:target_action",
		"action": {
			"type": "origins:heal",
			"amount": 2
		}
	},
	"item_condition": {
		"type": "origins:ingredient",
		"ingredient": {
			"tag": "minecraft:flowers"
		}
	}
}
```

This example will recover 1 heart to the entity upon the entity picking up an item included in the `#minecraft:flowers` (`data/minecraft/tags/items/flowers.json`) item tag.
<br>

```json
{
	"type": "origins:action_on_item_pickup",
	"bientity_action": {
		"type": "origins:if_else",
		"condition": {
			"type": "origins:actor_condition",
			"condition": {
				"type": "origins:exists"
			}
		},
		"if_action": {
			"type": "origins:and",
			"actions": [
				{
					"type": "origins:actor_action",
					"action": {
						"type": "apoli:execute_command",
						"command": "tag @s add item_thrower"
					}
				},
				{
					"type": "origins:target_action",
					"action": {
						"type": "origins:execute_command",
						"command": "tellraw @a [{\"selector\": \"@s\", \"color\": \"yellow\"}, {\"text\": \"has picked up an item throwned by \", \"color\": \"green\"}, {\"selector\": \"@e[tag = item_thrower]\"}]"
					}
				},
				{
					"type": "origins:actor_action",
					"action": {
						"type": "apoli:execute_command",
						"command": "tag @s remove item_thrower"
					}
				}
			]
		}
	}
}
```

This example will notify all players that the entity that has the power has picked up an item thrown by another entity.
