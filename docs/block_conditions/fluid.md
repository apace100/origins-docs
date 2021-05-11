---
title: Fluid (Condition)
date: 2021-04-05
---
# Fluid

[Block Condition](../block_conditions.md).

Checks the fluid state of the current position with a [Fluid Condition](../fluid_conditions.md).

Type ID: `origins:fluid`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`fluid_condition` | [Fluid Condition](../fluid_conditions.md) | | The fluid condition to check the fluid state at the position.

### Example:
```json
"block_condition": {
    "type": "origins:fluid",
    "fluid_condition": {
        "type": "origins:still"
    }
}
```
This example checks if the fluid block is a source fluid block.