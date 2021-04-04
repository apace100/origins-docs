---
title: Block In Radius
date: 2021-04-04
---
# Block In Radius

[Entity Condition](../entity_conditions.md).

Checks whether the player has a specified number of blocks blocks that match a specified block condition in a specified radius. The radius originates at the player's lower body block position.

Type ID: `origins:block_in_radius`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](../data_types/block_condition.md) | |  _The block condition which is applied to the block at the player's feet._
`radius` | [Integer](../data_types/integer.md) | |  _The radius to check blocks in._
`shape` | [String](../data_types/string.md) | `"cube"` | _Whether to check in a cube- or a star-shaped form. Either `"cube"` or `"star"`_
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | _How the number of blocks in the radius which fulfill `block_condition` should be compared to the specified value._
`compare_to` | [Integer](../data_types/integer.md) | `1` | _The value to compare the number to._
