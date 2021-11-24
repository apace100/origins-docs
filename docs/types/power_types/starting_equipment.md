---
title: Starting Equipment (Power Type)
date: 2021-04-08
---

# Starting Equipment

[Power Type](../power_types.md)

Provides the player with items when the power is granted.

Type ID: `origins:starting_equipment`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`stack` | [Positioned Item Stack](../data_types/positioned_item_stack.md) | _optional_ | If specified, this item will be given to the player (can be specified in an inventory slot). 
`stacks` | [Array](../types/data_types/array.md) of [Positioned Item Stacks](../data_types/positioned_item_stack.md) | _optional_ | If specified, these items will be given to the player (can be specified in an inventory slot). 
`recurrent` | [Boolean](../types/data_types/boolean.md) | `false` | Determines whether the specified item(s) should be given after respawning.

### Examples
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

```json
{
    "type": "origins:starting_equipment",
    "stacks": [
        {
            "item": "minecraft:white_stained_glass",
            "amount": 1,
            "slot": 39
        },
        {
            "item": "minecraft:leather_chestplate",
            "amount": 1,
            "tag": "{display: {color: 16383998}}",
            "slot": 38
        },
        {
            "item": "minecraft:leather_leggings",
            "amount": 1,
            "tag": "{display: {color: 16383998}}",
            "slot": 37
        },
        {
            "item": "minecraft:leather_boots",
            "amount": 1,
            "tag": "{display: {color: 16383998}}",
            "slot": 36
        },
        {
            "item": "minecraft:written_book",
            "amount": 1,
            "tag": "{display: {Name: '{\"text\": \"Example Book\", \"color\": \"light_purple\", \"italic\": false}'}, title: \"Example Book\", author: \"eggohito\", pages: ['{\"text\": \"This is page one.\"}', '{\"text\": \"This is page two, the last page.\"}']}",
            "slot": 8
        }
    ]
}
```
This example equips the player with a White Stained Glass Block in its head armor slot, a white-colored Leather Chestplate, Leggings and Boots in its chest, legs, and feet armor slots respectively, and a Written Book with two pages in the 9th hotbar slot.