---
title: Block Collision
date: 2021-04-04
---
# Block Collision

[Entity Condition](../entity_conditions.md).

Checks whether the bounding box of the player collides with any block.

Type ID: `origins:block_collision`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`offset_x` | [Float](../data_types/float.md) | |  By how much of the bounding box size should the box be offset in the X direction (e.g.: 0 = no offset, 1 = offset of exact width, 2 = offset of twice the width of the bounding box)
`offset_y` | [Float](../data_types/float.md) | |  By how much of the bounding box size should the box be offset in the Y direction (e.g.: 0 = no offset, 1 = offset of exact height, 2 = offset of twice the height of the bounding box)
`offset_z` | [Float](../data_types/float.md) | | By how much of the bounding box size should the box be offset in the Z direction (e.g.: 0 = no offset, 1 = offset of exact depth, 2 = offset of twice the depth of the bounding box)
