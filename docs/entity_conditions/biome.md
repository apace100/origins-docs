---
title: Biome
date: 2021-04-04
---
# Biome

[Entity Condition](../entity_conditions.md).

Checks whether the player is in a specific biome.

Type ID: `origins:biome`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`biome` | [String](../data_types/string.md) | _Optional_ |  _If set, this is the ID of the biome the player needs to be in for this condition to evaluate to true, e.g. `minecraft:savannah`._
`biomes` | [Array](../data_types/array.md) | _Optional_ |  _If set, these are the allowed biome IDs the player can be in for this condition to evaluate to true._
`condition` | [Biome Condition](../data_types/biome_condition.md) | _Optional_ | _If set, this condition needs to be fulfilled (in addition to having the right ID, if provided) by the biome in order for the condition to evaluate to true._
