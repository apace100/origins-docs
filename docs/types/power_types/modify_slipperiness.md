---
title: Modify Slipperiness (Power Type)
date: 2021-11-30
---

# Modify Slipperiness

[Power Type](../power_types.md)

Adjusts your friction, allowing you to emulate or counter the effects of ice blocks under certain conditions.

Type ID: `apoli:modify_slipperiness`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`block_condition` | [Block Condition](../block_condition_types.md) | _optional_ | If specified, the modifier(s) will only apply to the blocks that fulfills this condition.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the entity's slipperiness.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the entity's slipperiness.


### Examples

```json
{
    "type": "apoli:modify_slipperiness",
    "modifier": {
        "operation": "multiply_total",
        "value": 0.5
    },
    "block_condition": {
        "type": "apoli:block",
        "block": "minecraft:dirt"
    }
}
```

This example will increase the entity's friction by 50% while standing on dirt blocks.
