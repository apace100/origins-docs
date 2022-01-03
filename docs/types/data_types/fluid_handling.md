---
title: Fluid Handling (Data Type)
date: 2021-01-04
---

# Fluid Handling

[Data Type](../data_types.md)

A [String](string.md) used mainly for ray-casting to determine how it will handle fluids.


### Values

Value | Description
------|------------
`"any"` | The ray will stop at both flowing and source fluids.
`"none"` | The ray will **not** stop at both flowing and source fluids.
`"source_only"` | The ray will only stop at source fluids.
