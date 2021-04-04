---
title: Food Level
date: 2021-04-04
---
# Food Level

[Entity Condition](../entity_conditions.md).

Checks the player's food level (chicken legs / hunger meter / whatever you wanna call it). The food level is in the range of 0 to 20.

Type ID: `origins:food_level`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | _How the food level should be compared to the specified value._
`compare_to` | [Float](../data_types/float.md) | | _Which value the food level should be compared to._
