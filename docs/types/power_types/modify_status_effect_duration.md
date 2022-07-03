---
title: Modify Status Effect Duration (Power Type)
date: 2021-12-04
---

# Modify Status Effect Duration

[Power Type](../power_types.md)

Modifies the duration of the specified status effect(s) upon receiving the said status effect(s).

Type ID: `origins:modify_status_effect_duration`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`status_effect` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, only this status effect will have its duration modified upon being received.
`status_effects` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, only these status effects will have its duration modified upon being received.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the duration of the specified status effect(s).
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the duration of the specified status effect(s).


### Examples

```json
{
    "type": "origins:modify_status_effect_duration",
    "status_effect": "minecraft:speed",
    "modifier": {
        "operation": "multiply_base_multiplicative",
        "value": 0.25
    }
}
```

This example will modify the duration of the Speed status effect to have a 25% increase, making the entity that has the power receive Speed that initially lasted 60 seconds now last for 75 seconds.
