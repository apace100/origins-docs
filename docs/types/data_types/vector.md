---
title: Vector (Data Type)
date: 2021-12-03
---

# Vector

[Data Type](../data_types.md)

An [Object](object.md) that specifies the size of a three-dimensional cuboid, accepting [Floats](float.md) for each axis.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`x` | [Float](float.md) | `0` | The size of the cuboid to the X axis.
`y` | [Float](float.md) | `0` | The size of the cuboid to the Y axis.
`z` | [Float](float.md) | `0` | The size of the cuboid to the Z axis.

### Examples

```json
"spread": {
    "x": 3.0,
    "y": 0.0,
    "z": 3.0
}
```

A cuboid of about 5x0x5 in size, which has a volume of 25 blocks. 
