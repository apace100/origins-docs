---
title: Shape Type (Data Type)
date: 2021-01-04
---

# Shape Type

[Data Type](../data_types.md)

A [String](string.md) used mainly for ray-casting to determine how it will handle blocks.


### Values

Value | Description
------|------------
`"collider"` | The ray will only stop at blocks that cannot be walked through.
`"outline"` | The ray will take the shape of the block into account, only stopping if the ray has hit a face of the block.
`"visual"` | The ray will only stop at blocks that are not see-through.
