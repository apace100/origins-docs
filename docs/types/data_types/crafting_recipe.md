---
title: Crafting Recipe (Data Type)
date: 2021-04-04
---

# Crafting Recipe

[Data Type](../data_types.md)

An [Object](object.md) specifying a shapeless or shaped crafting recipe. For some more information, view [the page on recipes on the MC wiki](https://minecraft.wiki/w/Recipe).


### Fields (both types)

Field  | Type | Default | Description
-------|------|---------|-------------
`type` | [Identifier](identifier.md) | | The type of recipe. Either `minecraft:crafting_shaped` or `minecraft:crafting_shapeless`. Other recipe types are not supported.
`id` | [Identifier](identifier.md) | | An ID for this recipe. Has to be unique among all recipes, otherwise there will be a conflict.
`result` | [Object](object.md) with an `item` [ID](identifier.md) and `count` [Integer](integer.md) | | The result of the crafting. **Note that vanilla does _not_ support NBT tags in the result.**

<br>


### Fields (shapeless)

Field  | Type | Default | Description
-------|------|---------|-------------
`ingredients` | [Array](array.md) of [Ingredient](ingredient.md) | | The items that need to be put in the crafting grid for the recipe.


### Examples (shapeless)

```json
"recipe": {
	"type": "minecraft:crafting_shapeless",
	"id": "origins:fire_charge_without_blaze_powder",
	"ingredients": [
	    {
	      	"item": "minecraft:gunpowder"
	    },
	    [
		    {
		        "item": "minecraft:coal"
		    },
		    {
		        "item": "minecraft:charcoal"
		    }
	    ]
	],
	"result": {
	    "item": "minecraft:fire_charge",
	    "count": 3
	}
}
```

A crafting recipe to craft fire charges, but without the blaze powder required by the vanilla recipe.
<br>


### Fields (shaped)

Field  | Type | Default | Description
-------|------|---------|-------------
`pattern` | [Array](array.md) of [Strings](string.md) | | Specifies the pattern, with each element representing one row. Use a single character to describe one item. A space means that position is empty.
`key` | [Object](object.md) of "character": [Ingredient](ingredient.md) fields | | Specifies which character in the pattern corresponds to which [Ingredient](ingredient.md).


### Examples (shaped)

```json
"recipe": {
	"type": "minecraft:crafting_shaped",
	"id": "origins:sideways_birch_boat",
	"pattern": [
	    "##",
	    " #",
	    "##"
	],
	"key": {
	    "#": {
	    	"item": "minecraft:birch_planks"
	    }
  	},
  	"result": {
    	"item": "minecraft:birch_boat"
  	}
}
```

A crafting recipe for a birch boat, but with the planks rotated to the side in the crafting grid.
