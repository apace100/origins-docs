---
title: Modify Velocity (Power Type)
date: 2022-06-07
---

# Modify Velocity

[Power Type](../power_types.md)

Modifies all velocity in a specified axis.

Type ID: `origins:modify_velocity`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`axes` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md)| `["x","y","z"]` | Used to specify the axes affected by this modifier. 
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to velocity in the specified axes.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the specified axes.


### Examples

```json
{
  "type": "origins:modify_velocity",
  "modifier": {
    "value": -2,
    "operation": "multiply_total"
  },
  "axes": [
    "x",
    "y",
    "z"
  ]
}
```

This example will make all of the player's velocity reversed. You'll fall upwards, your movement keys will be inverted, etc.
