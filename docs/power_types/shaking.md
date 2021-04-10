---
title: Shaking (Power Type)
date: 2021-04-10
---
# Shaking

[Power Type](../power_types.md).

Makes the player shake, similar to a strider out of lava or a zombie undergoing conversion.

Type ID: `origins:shaking`

### Fields

_None._

### Example
```json
{
  	"type": "origins:shaking",
  	"condition": {
    	"type": "origins:on_fire",
      "inverted": true
  	}
}
```
This power makes the player shake when they are not burning.
