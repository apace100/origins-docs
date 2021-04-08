---
title: Lava Vision (Power Type)
date: 2021-04-08
---
# Lava Vision

[Power Type](../power_types.md).

Changes how far the player can see when submerged in lava.

Type ID: `origins:lava_vision`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`s` | [Float](../data_types/float.md) | | Near view. Vanilla default is 0.25, or 0.0 if you are under the effect of Fire Resistance.
`v` | [Float](../data_types/float.md) | | Far view. Vanilla default is 1.0, or 3.0 if you are under the effect of Fire Resistance.

### Example
```json
{
  	"type": "origins:lava_vision",
  	"s": 0,
  	"v": 15
}
```
Allows the player to see 15 blocks far while submerged in lava.
