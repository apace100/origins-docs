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
`sprite` | [Identifier](../identifier.md) | | The namespace, path and ID of the texture to use as the icon of the badge.
`recipe` | [Identifier](../identifier.md) | | The namespace, path and ID of the recipe to display in the tooltip.
`suffix` | [String](../string.md) | _optional_ | If specified, this text will be used as the suffix for the tooltip.
`prefix` | [String](../string.md) | _optional_ | If specified, this text will be used as the prefix for the tooltip.


### Examples

```json
{
    "type": "origins:crafting_recipe",
    "sprite": "minecraft:textures/item/wooden_sword.png",
    "recipe": "minecraft:wooden_sword"
}
```

This example will display the [`minecraft:textures/item/wooden_sword.png`](https://github.com/misode/mcmeta/blob/assets/assets/minecraft/textures/item/egg.png) texture and a tooltip that'd display the pattern for the Wooden Sword recipe.
