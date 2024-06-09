---
title: Action on Block Place (Power Type)
date: 2023-10-26
---


#	Action On Block Place

[Power Type](../power_types.md)

Executes an action upon placing a block.

Type ID: `origins:action_on_block_place`


!!!	note

	This power type will only work for players.


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | *optional* | If specified, this entity action will be executed on the player upon placing a block.
`held_item_action` | [Item Action Type](../item_action_types.md) | *optional* | If specified, this item action will be executed on the item the player has used to place a block.
`place_to_action` | [Block Action Type](../block_action_types.md) | *optional* | If specified, this block action will be executed at the position of the block the player has placed.
`place_on_action` | [Block Action Type](../block_action_types.md) | *optional* | If specified, this block action will be executed on the block the player placed a block on.
`item_condition` | [Item Condition Type](../item_condition_types.md) | *optional* | If specified, the specified actions will only be executed if the item the player has used to place a block fulfills this item condition.
`place_to_condition` | [Block Condition Type](../block_condition_types.md) | *optional* | If specified, the specified actions will only be executed if the block at the position of the block the player is about to place fulfills this block condition.
`place_on_condition` | [Block Condition Type](../block_condition_types.md) | *optional* | If specified, the specified actions will only be executed if the block the player is about to place a block on fulfills this block condition.
`directions` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["up", "down", "north", "south", "east", "west"]` | Determines whether the specified actions should be executed if the player is about to place a block at the specified side(s) of a block.
`hands` | [Array](../data_types/array.md) of [Hands](../data_types/string.md) | `["main_hand", "off_hand"]` | Determines whether the specified actions should be executed if the player used the specified hand(s) when trying to place a block.
`result_stack` | [Item Stack](../data_types/item_stack.md) | *optional* | If specified, this item stack will be given to the player upon placing a block.
`result_item_action` | [Item Action Type](../item_action_types.md) | *optional* | If specified, this item action will be executed on the item that will be given to the player upon placing a block.


###	Examples

```json
{
	"type": "origins:action_on_block_place",
	"entity_action": {
		"type": "origins:heal",
		"amount": 2
	},
	"item_condition": {
		"type": "origins:ingredient",
		"ingredient": {
			"item": "minecraft:wheat_seeds"
		}
	},
	"place_on_condition": {
		"type": "origins:block",
		"block": "minecraft:farmland"
	},
	"directions": [
		"up"
	]
}
```
This example will heal the player upon the player placing Wheat Seeds on top of Farmland blocks.
<br>

```json
{
	"type": "origins:action_on_block_place",
	"place_to_action": {
		"type": "origins:and",
		"actions": [
			{
				"type": "origins:area_of_effect",
				"block_action": {
					"type": "origins:set_block",
					"block": "minecraft:air"
				},
				"radius": 4,
				"shape": "star"
			},
			{
				"type": "origins:set_block",
				"block": "minecraft:magma_block"
			}
		]
	},
	"place_to_condition": {
		"type": "origins:fluid",
		"fluid_condition": {
			"type": "origins:in_tag",
			"tag": "minecraft:lava"
		}
	},
	"item_condition": {
		"type": "origins:ingredient",
		"ingredient": {
			"item": "minecraft:netherrack"
		}
	}
}
```
This example will make Netherrack blocks placed by the player will absorb Lava fluid with a 4 radius star-shaped area, and replace the placed Netherrack with a Magma block.
