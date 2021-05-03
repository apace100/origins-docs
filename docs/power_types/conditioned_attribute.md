---
title: Conditioned Attribute (Power Type)
date: 2021-04-07
---
# Conditioned Attribute

[Power Type](../power_types.md).

Applies one or more attribute modifiers, which may depend on a `condition` (use [Attribute](../power_types/attribute.md) if you are not using a `condition`).

Type ID: `origins:conditioned_attribute`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attributed Attribute Modifier](../data_types/attributed_attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to its corresponding attribute.
`modifiers` | [Array](../data_types/array.md) of [Attributed Attribute Modifiers](../data_types/attributed_attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to their corresponding attributes.
`tick_rate` | [Integer](../data_types/integer.md) | `20` | The frequency (in ticks) with which to check the condition. Lower values mean the condition changes are detected more quickly, but this comes at a potentially huge performance cost.


### Example
```json
{
    "type": "origins:conditioned_attribute",
    "modifier": {
        "attribute": "minecraft:generic.movement_speed",
        "operation": "addition",
        "value": 0.4,
        "name": "Increased sprinting speed"
    },
    "tick_rate": 20,
    "condition": {
        "type": "origins:sprinting"
    }
}
```
This power will add 0.4 to the player's `minecraft:generic.movement_speed` attribute if the player is sprinting.