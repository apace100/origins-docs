---
title: Night Vision (Power Type)
date: 2021-04-08
---

# Night Vision

[Power Type](../power_types.md)

Grants night vision to the player without the Night Vision status effect.

Type ID: `origins:night_vision`


!!! note

    The strength value of the Night Vision status effect is the default value, which is 1.0.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`strength` | [Float](../data_types/float.md) | `1.0` | Determines how strong the night vision effect is. Accepted range is from 0.0 to 1.0.


### Examples

```json
{
    "type": "origins:night_vision"
}
```

This example will give the player regular night vision.
<br>


```json
{
  	"type": "origins:night_vision",
  	"strength": 0.5,
	"condition": {
		"type": "origins:submerged_in",
		"fluid": "minecraft:water"
	}
}
```

This example will give the player night vision with 50% strength upon being submerged in water.
