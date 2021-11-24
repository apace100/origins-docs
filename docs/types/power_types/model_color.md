---
title: Model Color (Power Type)
date: 2021-04-08
---

# Model Color

[Power Type](../power_types.md)

Multiplies the luminosity of the base color of the texture of the entity that has the power by the specified color values.

Type ID: `origins:model_color`

!!! caution

	The resulting color will **always** be a darker color. Currently, there is no way to make it bright due to how the power type blends the color.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`red` | [Float](../types/data_types/float.md) | `1.0` | Value by which the red component of the texture will be multiplied. Range: 0.0 - 1.0.
`green` | [Float](../types/data_types/float.md) | `1.0` | Value by which the green component of the texture will be multiplied. Range: 0.0 - 1.0.
`blue` | [Float](../types/data_types/float.md) | `1.0` | Value by which the blue component of the texture will be multiplied. Range: 0.0 - 1.0.
`alpha` | [Float](../types/data_types/float.md) | `1.0` | Value by which the alpha (= transparency) component of the texture will be multiplied. Range: 0.0 - 1.0.

### Example
```json
{
  	"type": "origins:model_color",
  	"red": 0.5,
  	"green": 0.5,
  	"alpha": 0.7
}
```
Gives the player's skin a bluish tint and makes it slightly transparent.
