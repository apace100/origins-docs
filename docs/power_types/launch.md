---
title: Launch (Power Type)
date: 2021-04-08
---
# Launch

[Power Type](../power_types.md).

An active power which launches the player into the air.

Type ID: `origins:launch`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](../data_types/integer.md) | | The number of ticks the player has to wait between uses of this power.
`speed` | [Float](../data_types/float.md) | | The speed applied to the player in the upwards direction.
`hud_render` | [Hud Render](../data_types/hud_render.md) | | Specifies how and if a cooldown bar is rendered.
`sound` | [Identifier](../data_types/identifier.md) | _optional_ | If set, the sound with this ID will be played when the power is used.
`key` | [Key](../data_types/key.md) | _optional_ | Which active key this power should respond to. If none is specified, this power will use the primary active power key (by default G).

### Example
```json
{
  	"type": "origins:launch",
  	"cooldown": 600,
  	"hud_render": {
    	"bar_index": 4
  	},
  	"sound": "minecraft:entity.parrot.fly",
  	"speed": 2,
  	"key": {
    	"key": "key.origins.primary_active",
    	"continuous": true
  	}
}
```
Launches the player far into the air, with a cooldown of 30 seconds.
