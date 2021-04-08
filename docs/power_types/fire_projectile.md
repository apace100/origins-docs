---
title: Fire Projectile (Power Type)
date: 2021-04-08
---
# Fire Projectile

[Power Type](../power_types.md).

An active power which fires one or more projectiles when the active power key is pressed.

Type ID: `origins:fire_projectile`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_type` | [Identifier](../data_types/identifier.md) | | The ID of the entity type that will be fired.
`cooldown` | [Integer](../data_types/integer.md) | | The number of ticks the player has to wait between uses of this power.
`hud_render` | [Hud Render](../data_types/hud_render.md) | | Specifies how and if a cooldown bar is rendered.
`count` | [Integer](../data_types/integer.md) | 1 | The amount of projectiles to fire each use.
`speed` | [Float](../data_types/float.md) | 1.5 | The speed applied to the fired projectile.
`divergence` | [Float](../data_types/float.md) | 1.0 | How much each projectile fired is affected by random spread.
`sound` | [Identifier](../data_types/identifier.md) | _optional_ | If set, the sound with this ID will be played when the power is used.
`tag` | [String](../data_types/string.md) | _optional_ | NBT data of the entity.
`key` | [Key](../data_types/key.md) | _optional_ | Which active key this power should respond to. If none is specified, this power will use the primary active power key (by default G).



### Example
```json
{
  	"type": "origins:fire_projectile",
	"entity_type": "minecraft:arrow",
  	"cooldown": 2,
	"hud_render": {
		"should_render": false
	},
	"tag": "{pickup:0b}",
	"key": {
		"key": "key.attack",
		"continuous": true
	}
}
```
This power will let the player fire arrows very rapidly by holding the left mouse button. They can't be picked up.
