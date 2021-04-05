---
title: Relative Health
date: 2021-04-04
---
# Relative Health

[Entity Condition](../entity_conditions.md).

Checks the current health (relative value) of the player. Relative means it will check the percentage of the health, i.e. `currentHealth / maxHealth`.

Type ID: `origins:relative_health`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](../data_types/comparison.md) | | _How the relative health of the player should be compared to the specified value._
`compare_to` | [Float](../data_types/float.md) | | _Which value the relative health should be compared to._
