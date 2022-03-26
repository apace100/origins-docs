---
title: Fluid (Block Condition Type)
date: 2021-04-05
---

# Fluid

[Block Condition Type](../block_condition_types.md)

Checks the fluid state of the current position with a [Fluid Condition Type](../fluid_condition_types.md).

Type ID: `origins:fluid`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`fluid_condition` | [Fluid Condition Type](../fluid_condition_types.md) | | The fluid condition type to check the fluid state at the position.


### Examples

```json
"block_condition": {
    "type": "origins:fluid",
    "fluid_condition": {
        "type": "origins:still"
    }
}
```

This example will check if the block is a source fluid.
