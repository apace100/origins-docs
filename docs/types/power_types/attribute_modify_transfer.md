---
title: Attribute Modify Transfer (Power Type)
date: 2021-10-06
---

# Attribute Modify Transfer

[Power Type](../power_types.md)

Transfers the value of an attribute modifier from a specified attribute to a specified class.

Type ID: `origins:attribute_modify_transfer`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`class` | [Identifier](../types/data_types/identifier.md) | | The path and ID of the class to transfer the value of an attribute modifier to.
`attribute` | [Identifier](../types/data_types/identifier.md) | | The namespace and ID of the attribute to transfer the value from.
`multiplier` | [Float](../types/data_types/float.md) | `1.0` | Determines the multiplier for the value.
 
### Example
```json
{
    "type": "origins:attribute_modify_transfer",
    "class": "modify_break_speed",
    "attribute": "minecraft:generic.movement_speed",
    "multiplier": 1.25
}
```
This example transfers the attribute modifier value of the `minecraft:generic.movement_speed` attribute to the `modify_break_speed` (`io.github.apace100.apoli.power.ModifyBreakSpeedPower`) class, essentially giving you mining speed boost if your movement speed is high.