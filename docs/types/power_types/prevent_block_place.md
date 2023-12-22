---
title: Prevent Block Place (Power Type)
date: 2023-10-26
---


#	Prevent Block Place

[Power Type](../power_types.md)

Prevents the player from placing a block.

Type ID: `origins:prevent_block_place`


###	Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_action` | [Entity Action Type](../entity_action_types.md) | *optional* | If specified, this entity action will be executed on the player upon being prevented from placing a block.
`held_item_action` | [Item Action Type](../item_action_types.md) | *optional* | If specified, this item action will be executed on the item the player has used to try to place a block.
`place_to_action` | [Block Action Type](../block_action_types.md) | *optional* | If specified, this block action will be executed at the position of the block the player tried to place.
`place_on_action` | [Block Action Type](../block_action_types.md) | *optional* | If specified, this block action will be executed on the block the player tried to place a block on.
`item_condition` | [Item Condition Type](../item_condition_types.md) | *optional* | If specified, the specified actions will only be executed if the item the player has used to try to place a block fulfills this item condition.
`place_to_condition` | [Block Condition Type](../block_condition_types.md) | *optional* | If specified, the specified actions will only be executed if the block at the position of the block the player tried to place fulfills this block condition.
`place_on_condition` | [Block Condition Type](../block_condition_types.md) | *optional* | If specified, the specified actions will only be executed if the block the player tried to place a block on fulfills this block condition.
`directions` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["up", "down", "north", "south", "east", "west"]` | Determines whether the specified actions should be executed if the player tried to place a block at the specified side(s) of a block.
`hands` | [Array](../data_types/array.md) of [Hands](../data_types/string.md) | `["main_hand", "off_hand"]` | Determines whether the specified actions should be executed if the player used the specified hand(s) when trying to place a block.
`result_stack` | [Item Stack](../data_types/item_stack.md) | *optional* | If specified, this item stack will be given to the player upon trying to place a block.
`result_item_action` | [Item Action Type](../item_action_types.md) | *optional* | If specified, this item action will be executed on the item that will be given to the player upon trying to place a block.


###	Examples

```json
{
	"type": "origins:prevent_block_place",
	"entity_action": {
		"type": "origins:execute_command",
		"command": "tellraw @s {\"text\": \"Cannot place a block here!\", \"color\": \"red\"}"
	},
	"place_to_condition": {
		"type": "origins:fluid",
		"fluid_condition": {
			"type": "origins:still",
			"inverted": true
		}
	}
}
```

This example will prevent the player from placing blocks in spaces occupied by source fluids.
