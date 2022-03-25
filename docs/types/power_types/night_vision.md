---
title: Night Vision (Power Type)
date: 2021-04-08
---

# Night Vision

[Power Type](../power_types.md)

Grants night vision to the player without a status effect.

Type ID: `apoli:night_vision`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`strength` | [Float](../data_types/float.md) | `1.0` | How strong the night vision effect is. Range: 0.0 - 1.0.


### Examples

```json
{
  	"type": "apoli:night_vision",
  	"strength": 0.5,
	"condition": {
		"type": "apoli:submerged_in",
		"fluid": "minecraft:water"
	}
}
```

This example will give the player night vision while underwater, improving their vision by quite a bit.
