---
title: Hud Render (Data Type)
date: 2021-04-04
---
# Hud Render

[Data Type](../data_types.md).

An [Object](object.md) used to define how a resource or cooldown bar should be rendered.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`should_render` | [Boolean](boolean.md) | true | Whether the bar should be visible or not.
`sprite_location` | [Identifier](identifier.md) | "origins:textures/gui/resource_bar.png" | The path to the file in the assets which contains what the bar looks like. See the [List of resource bar files](../misc/resource_bars.md) for a list of files included by default in the mod.
`bar_index` | [Integer](integer.md) | 0 | The indexed position of the bar on the sprite to use.
`condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If set (and `should_render` is true), the bar will only display when the entity with the power fulfills this condition.

### Examples:

```json
{
	"hud_render": {
		"bar_index": 4,
		"condition": {
			"type": "origins:power_active",
			"power": "origins:phantomize"
		}
	}
}
```

This definition shows the resource/cooldown as the Elytrian bar (white and with a wings icon), but only while the player is phantomized.
<br>

```json
{
	"hud_render": {
		"sprite_location": "origins:textures/gui/community/spiderkolo/resource_bar_03.png",
		"bar_index": 5
	}
}
```

This definition shows the resource/cooldown as a white bar with a bone icon.