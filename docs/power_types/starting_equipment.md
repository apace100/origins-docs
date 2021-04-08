---
title: Starting Equipment (Power Type)
date: 2021-04-08
---
# Starting Equipment

[Power Type](../power_types.md).

Provides the player with items when the power is chosen.

Type ID: `origins:starting_equipment`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`stack` | [Positioned Item Stack](../data_types/positioned_item_stack.md) | _optional_ | If set, this item stack will be given to the player, optionally into the specified inventory slot.
`stacks` | [Array](../data_types/array.md) of [Positioned Item Stacks](../data_types/positioned_item_stack.md) | _optional_ | If set, these item stacks will be given to the player, optionally into the specified inventory slots.
`recurrent` | [Boolean](../data_types/boolean.md) | false | When set to true, the starting equipment will always be given to the player after they died, otherwise only once when the power is gained.

### Example
```json
{
  	"type": "origins:starting_equipment",
  	"stacks": [
    	{
      		"item": "minecraft:compass"
    	},
    	{
      		"item": "minecraft:clock"
    	},
    	{
      		"item": "minecraft:map",
	    	"amount": 9
    	}
  	]
}
```
Players with this power will receive the "Explorer Kit" known from Origins: Classes. It contains a compass, a clock, and 9 empty maps.
