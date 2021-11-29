---
title: Modify Swim Speed (Power Type)
date: 2021-04-06
---

# Modify Swim Speed

[Power Type](../power_types.md)

Modifies how fast the entity that has the power swims.

Type ID: `origins:modify_swim_speed`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will apply to the swim speed.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will apply to the swim speed.



### Examples

```json
{
    "type": "origins:modify_swim_speed",
    "modifier": {
        "operation": "addition",
        "value": 0.025
    }
}
```

This power will make the entity that has the power swim/walk significantly faster in water.
