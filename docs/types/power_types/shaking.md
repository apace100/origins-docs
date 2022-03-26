---
title: Shaking (Power Type)
date: 2021-04-10
---

# Shaking

[Power Type](../power_types.md)

Makes the entity that has the power shake, similar to a Strider out of lava or a Zombie undergoing conversion.

Type ID: `origins:shaking`


### Fields

_None._


### Examples

```json
{
  	"type": "origins:shaking",
  	"condition": {
    	"type": "origins:on_fire",
      "inverted": true
  	}
}
```

This example will make the entity shake if the entity is not burning.
