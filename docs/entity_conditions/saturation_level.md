---
title: Saturation Level
date: 2021-04-04
---
# Saturation Level

[Entity Condition](../entity_conditions.md).

Checks the player's saturation level (the invisible value of how "full" you are, i.e. how long it takes before your hunger meter actually goes down).

Type ID: `origins:saturation_level`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | _How the saturation level should be compared to the specified value._
`compare_to` | [Float](../data_types/float.md) | | _Which value the saturation level should be compared to._
