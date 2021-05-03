---
title: Modify Swim Speed (Power Type)
date: 2021-04-06
---
# Modify Swim Speed

[Power Type](../power_types.md).

Modifies how fast the player swims.

Type ID: `origins:modify_swim_speed`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If set, this modifier will apply to the swim speed.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If set, these modifiers will apply to the swim speed.


### Example
```json
{
    "type": "origins:modify_swim_speed",
    "modifier": {
        "operation": "addition",
        "value": 0.025
    }
}
```
This power makes the player swim/walk significantly faster in water.