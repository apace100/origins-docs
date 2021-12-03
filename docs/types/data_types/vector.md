---
title: Vector (Data Type)
date: 2021-12-03
---

# Vector

[Data Type](../data_types.md)

An [Object](object.md) that specifies the size of a three-dimensional cuboid, accepting floating-point number values for each coordinate, which are then multiplied by 8.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`x` | [Float](float.md) | `0` | The size of the cuboid to the X axis.
`y` | [Float](float.md) | `0` | The size of the cuboid to the Y axis.
`z` | [Float](float.md) | `0` | The size of the cuboid to the Z axis.

### Examples

```json
"spread": {
    "x": 0.8,
    "y": 0.8,
    "z": 0.8
}
```

A cuboid of about 6.4x6.4x6.4 in size. (`0.8 * 8 = 6.4`)
