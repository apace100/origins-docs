---
title: Destruction Types (Extras)
date: 2022-04-01
---

# Destruction Type

[Extra](../extras.md)

A [string](../../types/data_types/string.md) that is used to determine the effect of an explosion to the terrain.


### Values

Value       | Description
------------|------------
`"break"`   | The explosion will destroy the blocks and drop the loot of all blocks.
`"destroy"` | The explosion will destroy the blocks and drop the loot of some blocks (lower chance with higher explosion power, checks `survives_explosion` loot condition in loot tables.
`"none"`    | The explosion will **not** destroy the blocks nor drop the loot of the blocks.
