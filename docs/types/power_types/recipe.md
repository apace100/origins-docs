---
title: Recipe (Power Type)
date: 2021-04-08
---

# Recipe

[Power Type](../power_types.md)

Allows a player with this power to craft the defined crafting recipe.

Type ID: `origins:recipe`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`recipe` | [Crafting Recipe](../data_types/crafting_recipe.md) | | The recipe to craft, including an `id` field which can be any arbitrary (but unique) identifier.


### Examples

```json
{
    "type": "origins:recipe",
    "recipe": {
      	"id": "origins:master_of_webs/web_crafting",
      	"type": "minecraft:crafting_shapeless",
      	"ingredients": [
        	{
          		"item": "minecraft:string"
        	},
        	{
          		"item": "minecraft:string"
        	}
      	],
      	"result": {
        	"item": "minecraft:cobweb"
      	}
    }
}
```

This example will allow the player that has the power to craft Cobwebs by combining two strings in a crafting grid.
