---
title: Fire Projectile (Power Type)
date: 2021-10-02
---

# Fire Projectile

[Power Type](../power_types.md)

Fires one or more projectiles upon pressing the specified [Key](../data_types/key.md).

Type ID: `origins:fire_projectile`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_type` | [Identifier](../data_types/identifier.md) | | The ID of the entity type that will be fired.
`cooldown` | [Integer](../data_types/integer.md) | `1` | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](../data_types/hud_render.md) | _optional_ | Determines how the cooldown of this power is visualized on the HUD.
`count` | [Integer](../data_types/integer.md) | `1` | The amount of projectiles to fire each use.
`interval` | [Integer](../data_types/integer.md) | `0` | Determines the interval for firing multiple projectiles consecutively (in ticks). If set to 0, it will fire all the projectiles at the same tick.
`start_delay` | [Integer](../data_types/integer.md) | `0` | Determines how long the start of the firing process is delayed (in ticks).
`speed` | [Float](../data_types/float.md) | `1.5` | The speed applied to the fired projectile.
`divergence` | [Float](../data_types/float.md) | `1.0` | How much each projectile fired is affected by random spread.
`sound` | [Identifier](../data_types/identifier.md) | _optional_ | If set, the sound with this ID will be played when the power is used.
`tag` | [NBT](../data_types/nbt.md) | _optional_ | NBT data of the entity.
`key` | [Key](../data_types/key.md) | _optional_ | Which active key this power should respond to. If none is specified, this power will use the primary active power key (by default G).


### Examples

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

This example will let the player fire arrows very rapidly by holding the left mouse button. They can't be picked up.
<br>

```json
{
    "type": "origins:fire_projectile",
    "entity_type": "minecraft:snowball",
    "cooldown": 100,
    "hud_render": {
        "should_render": false
    },
    "count": 4,
    "interval": 5,
    "tag": "{Item: {id: 'minecraft:slime_ball', Count: 1b}}",
    "key": {
        "key": "key.use",
        "continuous": false
    }
}
```

This example will let the player fire 4 snow balls disguised as slime balls consecutively, with an interval of 5 ticks upon pressing the right mouse button.
