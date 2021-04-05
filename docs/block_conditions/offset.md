---
title: Offset (Condition)
date: 2021-04-05
---
# Offset

[Block Condition](../block_conditions.md).

A meta-condition which instead checks the provided [Block Condition](../block_conditions.md) at a position offset from the current position.

Type ID: `origins:offset`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` | [Block Condition](../block_conditions.md) | | _The condition to check with the given offset._
`x` | [Integer](../data_types/integer.md) | `0` |  _How much to offset the position on the x-axis._
`y` | [Integer](../data_types/integer.md) | `0` |  _How much to offset the position on the y-axis._
`z` | [Integer](../data_types/integer.md) | `0` |  _How much to offset the position on the z-axis._
