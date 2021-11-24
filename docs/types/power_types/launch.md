---
title: Launch (Power Type)
date: 2021-04-08
---

# Launch

[Power Type](../power_types.md)

Launches the entity that has the power upwards upon pressing the specified [Key](../data_types/key.md).

Type ID: `origins:launch`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](../types/data_types/integer.md) | | Interval of ticks this power needs to recharge before the power can be triggered again.
`speed` | [Float](../types/data_types/float.md) | | The speed applied to the player in the upwards direction.
`hud_render` | [Hud Render](../types/data_types/hud_render.md) | | Determines how the cooldown of this power is visualized on the HUD.
`sound` | [Identifier](../types/data_types/identifier.md) | _optional_ | If specified, the sound event with this namespace and ID will be played when the power is triggered.
`key` | [Key](../data_types/key.md) | _optional_ | Which active key this power should respond to.

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
