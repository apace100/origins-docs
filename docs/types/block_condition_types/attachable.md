---
title: Attachable (Block Condition Type)
date: 2021-04-05
---

# Attachable

[Block Condition Type](../block_condition_types.md)

Checks whether the block is in a place where a supported block can be attached (i.e. checks whether any of the adjacent blocks' sides towards this block position are solid).

Type ID: `origins:attachable`

### Fields:

_None._

### Example:
```json
"block_condition": {
    "type": "origins:attachable"
}
```