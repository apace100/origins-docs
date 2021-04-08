---
title: Model Color (Power Type)
date: 2021-04-08
---
# Model Color

[Power Type](../power_types.md).

Multiplies the color of the player's texture.

Type ID: `origins:model_color`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`red` | [Float](../data_types/float.md) | 1.0 | Value by which the red component of the texture will be multiplied. Range: 0 - 1.
`green` | [Float](../data_types/float.md) | 1.0 | Value by which the green component of the texture will be multiplied. Range: 0 - 1.
`blue` | [Float](../data_types/float.md) | 1.0 | Value by which the blue component of the texture will be multiplied. Range: 0 - 1.
`alpha` | [Float](../data_types/float.md) | 1.0 | Value by which the alpha (= transparency) component of the texture will be multiplied. Range: 0 - 1.

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
