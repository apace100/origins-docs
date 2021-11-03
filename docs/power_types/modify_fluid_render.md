---
title: Modify Fluid Render (Power Type)
date: 2021-10-05
---

# Modify Fluid Render

[Power Type](../power_types.md)

Modifies how a fluid would look like to the entity.

Type ID: `origins:modify_fluid_render`

!!! note

    This power type does **not** support a `condition`. If the `condition` field is present, it will be ignored.

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`block_condition` | [Block Condition](../block_conditions.md) | _optional_ | If set, modifies how the block that meets this condition would look like.
`fluid_condition` | [Fluid Condition](../fluid_conditions.md) | _optional_ | If set, modifies how the fluid that meets the condition would look like.
`fluid` | [Identifier](../data_types/identifier.md) | | The ID of the fluid that would replace how the block/fluid that meets the conditions in the `block_condition` and/or `fluid_condition` object field would look like.

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