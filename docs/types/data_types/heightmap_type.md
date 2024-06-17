---
title:	Heightmap Type (Data Type)
date:	2024-06-17
---

#	Heightmap Type

A [string](string.md) used for various game calculations to determine the highest Y level of a coordinate in a world.


###	Values

Value | Description
------|------------
`world_surface` 			|	Queries the Y level of the highest non-air block.
`world_surface_wg`			|	Queries the Y level of the highest non-air block (**only used on world generation**.)
`ocean_floor`				|	Queries the Y level of the highest block that has collision, except carpets.
`ocean_floor_wg`			|	Queries the Y level of the highest block that has collision, except carpets (**only used on world generation**.)
`motion_blocking`			|	Queries the Y level of the highest block that has collision or contains a fluid (e.g: water, lava, or fluidlogged blocks.)
`motion_blocking_no_leaves`	|	Queries the Y level of the highest block that has collision or contains a fluid, except leaves (e.g: water, lava, or fluidlogged blocks.)
