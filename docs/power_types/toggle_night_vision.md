---
title: Toggle Night Vision (Power Type)
date: 2021-04-08
---
# Toggle Night Vision

[Power Type](../power_types.md).

Defines a [Night Vision](night_vision.md) power which can be toggled on and off with the active power key.

Type ID: `origins:toggle_night_vision`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`active_by_default` | [Boolean](../data_types/boolean.md) | true | Whether this power starts in the on or off state.
`strength` | [Float](../data_types/float.md) | 1.0 | How strong the night vision effect is. Range: 0 - 1.
`key` | [Key](../data_types/key.md) | _optional_ | Which active key this power should respond to. If none is specified, this power will use the primary active power key (by default G).

### Example
```json
{
  	"type": "origins:toggle_night_vision",
  	"strength": 0.5,
	"condition": {
		"type": "origins:submerged_in",
		"fluid": "minecraft:water"
	}
}
```
Gives the player night vision while underwater, improving their vision by quite a bit (though not as good as real night vision, because this is set to be only half as strong). However, this can be turned on and off with G!
