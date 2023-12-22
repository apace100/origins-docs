---
title: Hud Render (Data Type)
date: 2021-04-04
---

#	Hud Render

[Data Type](../data_types.md)

An [object](object.md) or [array](array.md) of [objects](object.md) used to define how a resource or cooldown bar should be rendered.


!!!	note

	If the specified HUD render is an array of objects, then the HUD render will choose the first object that is allowed to be rendered (its `should_render` field set to `true`) and its condition fulfilled (or if its `condition` field is absent) from top to bottom. The `order` value of the very first object will also be inherited by the following objects that do not have the `order` field specified.

!!!	caution

	The entity condition specified in the `condition` field is only evaluated on the <span style="color:goldenrod"><b>client-side</b></span>, therefore, using entity condition types that only work on the server-side will not work.


###	Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`should_render` | [Boolean](boolean.md) | `true` | Whether the bar should be visible or not.
`sprite_location` | [Identifier](identifier.md) | `"origins:textures/gui/resource_bar.png"` | The path to the file in the assets which contains what the bar looks like. See the [List of sprites](../../misc/extras/sprites.md) for a list of files included by default in the mod.
`bar_index` | [Integer](integer.md) | `0` | The indexed position of the bar on the sprite to use. Please note that indexes start at `0`.
`icon_index` | [Integer](integer.md) | `0` | The indexed position of the icon on the sprite to use. Please note that indexes start at `0`.
`condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If set (and `should_render` is true), the bar will only display when the entity with the power fulfills this condition.
`inverted` | [Boolean](boolean.md) | `false` | If set to true, inverts the way the hud render process (it'll look like its value is being decreased).
`order` | [Integer](integer.md) | *optional* | If specified, this determines the position of the HUD render when being rendered. The higher the `order` value is, the higher it is on the rendered HUD render stack.


### Examples

```json
"hud_render": {
	"bar_index": 4,
	"condition": {
		"type": "origins:power_active",
		"power": "origins:phantomize"
	}
}
```

This definition shows the resource/cooldown as the Elytrian bar (white and with a wings icon), but only while the player is phantomized.
<br>

```json
"hud_render": {
    "sprite_location": "origins:textures/gui/community/spiderkolo/resource_bar_03.png",
    "bar_index": 5
}
```

This definition shows the resource/cooldown as a white bar with a bone icon.
<br>

```json
"hud_render": [
	{
		"sprite_location": "origins:textures/gui/community/spiderkolo/resource_bar_03.png",
		"bar_index": 3,
		"condition": {
			"type": "origins:relative_health",
			"comparison": "<=",
			"compare_to": 0.5
		}
	},
	{
		"sprite_location": "origins:textures/gui/community/spiderkolo/resource_bar_01.png",
		"bar_index": 4
	}
]
```
This definition will show the resource/cooldown as a white bar with a bone icon if the entity is sneaking. Otherwise, the resource/cooldown will be shown as a red bar with a heart icon.
