---
title: Modify Block Render (Power Type)
date: 2021-10-05
---
# Modify Block Render

[Power Type](../power_types.md)

Modifies how a block would look like to the entity.

Type ID: `origins:modify_block_render`

!!! note

    This power type does **not** support a `condition`. If the `condition` field is present, it will be ignored.

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`block_condition` | [Block Condition](../block_conditions.md) | _optional_ | If set, modifies how the block would look like that meets this condition.
`block` | [Identifier](../data_types/identifier.md) | | The ID of the block that would replace the block that meets the condition from the `block_condition` object field would look like.

### Example
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
This example makes it so that a Diamond Ore block would look like a Diamond Block.