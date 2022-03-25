---
title: Toggle Night Vision (Power Type)
date: 2021-04-08
---

# Toggle Night Vision

[Power Type](../power_types.md)

Defines a [Night Vision (Power Type)](night_vision.md) which can be toggled on and off with the specified [Key](../data_types/key.md).

Type ID: `apoli:toggle_night_vision`

### Fields

| Field               | Type                                | Default    | Description                                                                                                                           |
| ------------------- | ----------------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| `active_by_default` | [Boolean](../data_types/boolean.md) | `true`     | Whether this power starts in the on or off state.                                                                                     |
| `strength`          | [Float](../data_types/float.md)     | `1.0`      | How strong the night vision effect is. Range: 0.0 - 1.0.                                                                              |
| `key`               | [Key](../data_types/key.md)         | _optional_ | Which active key this power should respond to. If none is specified, no key will be set by default. |

### Examples

```json
{
	"type": "apoli:toggle_night_vision",
	"strength": 0.5,
	"condition": {
		"type": "apoli:submerged_in",
		"fluid": "minecraft:water"
	}
}
```

This example will give the player night vision while underwater, improving their vision by quite a bit that can be turned on and off by pressing the Primary ability key.
