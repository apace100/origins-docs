---
title: Fluid Handling (Extras)
date: 2021-01-04
---

# Fluid Handling

[Extra](../extras.md)

A [string](../../types/data_types/string.md) used mainly for ray-casting to determine how it will handle fluids.


### Values

Value           | Description
----------------|------------
`"any"`         | The ray will stop at both flowing and source fluids.
`"none"`        | The ray will **not** stop at both flowing and source fluids.
`"source_only"` | The ray will only stop at source fluids.
