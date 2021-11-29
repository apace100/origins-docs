---
title: Modify Block Render (Power Type)
date: 2021-10-05
---

# Modify Block Render

[Power Type](../power_types.md)

Modifies how a block would look like to the entity that has the power.

Type ID: `origins:modify_block_render`

!!! note

    This power type does **not** support a `condition`. If the `condition` field is present, it will be ignored.


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, only modify how the blocks that fulfill this condition would look like.
`block` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the replacement block.


### Examples

```json
{
    "type": "origins:modify_block_render",
    "block_condition": {
        "type": "origins:block",
        "block": "minecraft:diamond_ore"
    },
    "block": "minecraft:diamond_block"
}
```

This example will make Diamond Ore blocks look like Diamond Blocks.
