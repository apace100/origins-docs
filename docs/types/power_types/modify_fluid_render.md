---
title: Modify Fluid Render (Power Type)
date: 2021-10-05
---

# Modify Fluid Render

[Power Type](../power_types.md)

Modifies how a fluid would look like to the entity that has the power.

Type ID: `origins:modify_fluid_render`

!!! note

    This power type does **not** support a `condition`. If the `condition` field is present, it will be ignored.

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`block_condition` | [Block Condition](../block_conditions.md) | _optional_ | If specified, only modify how the blocks that fulfills this condition would look like.
`fluid_condition` | [Fluid Condition](../fluid_conditions.md) | _optional_ | If specified, only modify how the fluids that fulfills this condition would look like.
`fluid` | [Identifier](../types/data_types/identifier.md) | | The namespace and ID of the replacement fluid.

### Example
```json
{
    "type": "origins:modify_fluid_render",
    "block_condition": {
        "type": "origins:block",
        "block": "minecraft:water"
    },
    "fluid": "minecraft:lava"
}
```
This example will make Water look like Lava.