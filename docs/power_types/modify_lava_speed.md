---
title: Modify Lava Speed (Power Type)
date: 2021-04-06
---
# Modify Lava Speed

[Power Type](../power_types.md).

Modifies how fast the player moves in lava.

Type ID: `origins:modify_lava_speed`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If set, this modifier will apply to the speed in lava.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If set, these modifiers will apply to the speed in lava.


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