---
title: Crafting Recipe (Badge Type)
date: 2022-07-03
---

#   Crafting Recipe

[Badge Type](../badge_types.md)

Displays a tooltip with an image that shows the pattern of a certain recipe upon being hovered with a Mouse cursor.

Type ID: `origins:crafting_recipe`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`sprite` | [Identifier](../data_types/identifier.md) | | The namespace, path and ID of the texture to use as the icon of the badge.
`recipe` | [Crafting Recipe](../data_types/crafting_recipe.md) | | The recipe to display, including an `id` field which can be any arbitrary identifier.
`suffix` | [Text Component](../data_types/text_component.md) | _optional_ | If specified, this text will be used as the suffix for the tooltip.
`prefix` | [Text Component](../data_types/text_component.md) | _optional_ | If specified, this text will be used as the prefix for the tooltip.


### Examples

```json
{
    "type": "origins:crafting_recipe",
    "sprite": "minecraft:textures/item/wooden_sword.png",
    "recipe": {
		"id": "minecraft:wooden_sword",
		"type": "minecraft:crafting_shaped",
		"key": {
			"#": {
	    		"item": "minecraft:stick"
	    	},
	    	"X": {
	    		"tag": "minecraft:planks"
	    	}
	  	},
	  	"pattern": [
	    	"X",
	    	"X",
	    	"#"
	  	],
	  	"result": {
	    	"item": "minecraft:wooden_sword"
	  	}
	}
}
```

This example will display the [`minecraft:textures/item/wooden_sword.png`](https://github.com/misode/mcmeta/blob/assets/assets/minecraft/textures/item/wooden_sword.png) texture and a tooltip that'd display the pattern for the Wooden Sword recipe.
