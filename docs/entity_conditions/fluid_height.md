---
title: Fluid Height
date: 2021-04-04
---
# Fluid Height

[Entity Condition](../entity_conditions.md).

Checks how high a specific fluid is at the player. A fluid height of 0 means the player is not touching the fluid.

Type ID: `origins:fluid_height`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`fluid` | [String](../data_types/string.md) | | _ID of the fluid tag of which the height should be checked. Most important examples: `minecraft:water` and `minecraft:lava`._
`comparison` | [Comparison](../data_types/comparison.md) | | _How the fluid height should be compared to the specified value._
`compare_to` | [Float](../data_types/float.md) | | _Which value the fluid height should be compared to._
