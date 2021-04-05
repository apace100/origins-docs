---
title: In Block Anywhere
date: 2021-04-04
---
# In Block Anywhere

[Entity Condition](../entity_conditions.md).

Checks whether the entity is overlapping with a block anywhere.

Type ID: `origins:in_block_anywhere`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](../block_condition.md) | |  The block condition which blocks need to fulfill in order to count for this power.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` |  How the number of blocks which overlap and fulfill block_condition should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` |  The value to compare the number to.
