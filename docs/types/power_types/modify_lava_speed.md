---
title: Modify Lava Speed (Power Type)
date: 2021-04-06
---

# Modify Lava Speed

[Power Type](../power_types.md)

Modifies how fast the entity that has the power moves in lava.

Type ID: `origins:modify_lava_speed`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../types/data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the movement speed while in lava.
`modifiers` | [Array](../types/data_types/array.md) of [Attribute Modifiers](../types/data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the movement speed while in lava.


### Example
```json
{
    "type": "origins:modify_lava_speed",
    "modifier": {
        "operation": "addition",
        "value": 0.4
    }
}
```
This power makes the player swim/walk significantly faster in lava.