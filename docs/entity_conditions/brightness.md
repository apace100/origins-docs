---
title: Brightness
date: 2021-04-04
---
# Brightness

[Entity Condition](../entity_conditions.md).

Checks the brightness at the player's eyes, which ranges from 0 to 1.

Type ID: `origins:brightness`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | How to compare the brightness against the specified value.
`compare_to` | [Float](../data_types/float.md) | | Which value to compare the brightness against.
