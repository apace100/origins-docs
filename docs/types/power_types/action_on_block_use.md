---
title: Action On Block Use (Power Types)
date: 2021-11-30
---

# Action On Block Use

[Power Type](../power_types.md)

Executes a [Block Action Type](../bientity_action_types.md) and/or [Item Action Types](../item_action_types.md) when the player that has the power "uses" (right-clicks) a block.

Type ID: `origins:action_on_block_use`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`block_action` | [Bi-entity Action Type](../block_action_types.md) | _optional_ | If specified, the used block will run this action if all conditions are met.
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by the used block.
`item_condition` | [Item Condition Type](../item_condition_types.md) | _optional_ | If specified, only execute the specified actions if this condition is fulfilled by the item in the 'actor' (the player that has the power) entity's specified hand(s) determined by the `hands` string field.
`directions` |[Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["north", "east", "south", "west", "up", "down"]` | If specified, only execute the specified actions if you used the specified face of the block.
`hands` | [Array](../data_types/array.md) of [Strings](../data_types/string.md) | `["off_hand", "main_hand"]` | Determines if the power should be activated if the player used the specified hand(s). Accepts `"off_hand"`, `"main_hand"` or both.
`result_stack` | [Item Stack](../data_types/item_stack.md) | _optional_ | If specified, gives the item to the 'actor' (the player that has the power) entity.
`held_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item used for right-clicking the 'target' entity in the specified hand(s) determined by the `hands` string field.
`result_item_action` | [Item Action Type](../item_action_types.md) | _optional_ | If specified, this action will be executed on the item that is given to the 'actor' (the player that has the power) entity.
`action_result` | [String](../data_types/string.md) | `"success"` | Determines the result of the 'use action'. Accepts `"consume"`, `"consume_partial"`, `"fail"`, `"pass"` or `"success"`.


### Examples

```json
{
	"type": "origins:action_on_block_use",
	"block_action": {
		"type": "origins:set_block",
		"block": "minecraft:gold_block"
	},
	"block_condition": {
		"type": "origins:block",
		"block": "minecraft:iron_block"
	},
	"directions": [
		"up",
		"down"
	],
	"condition": {
		"type": "origins:sprinting"
	}
}
```

This example will replace any iron blocks with gold blocks if you right click the top or bottom of the block while sprinting.
