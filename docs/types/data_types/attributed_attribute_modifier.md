---
title: Attributed Attribute Modifier (Data Type)
date: 2021-04-04
---

# Attributed Attribute Modifier

[Data Type](../data_types.md)

An [Object](object.md) used to specify how a specific attribute should be modified. Basically an [Attribute Modifier](attribute_modifier.md) with an additional `attribute` field.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`attribute` | [Identifier](identifier.md) | | ID of the attribute which will be modified by this modifier.
`operation` | [Attributed Attribute Modifier Operation](attributed_attribute_modifier_operation.md) | | The operation which will be performed by this modifier.
`value` | [Float](float.md) | | The value to use for the modifier operation.
`resource` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the value of this power will be used instead of the value specified in the `value` field.
`name` | [String](string.md) | _optional_ | A descriptive name for the modifier, describing where it comes from.


### Examples

```json
"modifier": {
    "attribute": "minecraft:generic.attack_damage",
    "operation": "addition",
    "value": 9
}
```

This example will add `9.0` to the base value of the entity's `minecraft:generic.attack_damage` attribute.
(For example: if the current base value is 1, the new base value will be 10 since `1 + 9 = 10`)
<br>

```json
"modifier": {
    "attribute": "minecraft:generic.max_health",
    "operation": "multiply_base",
    "value": 2
}
```

This example will add the base value multiplied by the modifier value to the current base value of the entity's `minecraft:generic.max_health` attribute.
(For example: if the current base value is 20, the new base value will be 60 since `20 + (20 * 2) = 60`)
<br>

```json
"modifier": {
    "attribute": "minecraft:generic.movement_speed",
    "operation": "multiply_total",
    "change": 0.5
}
```

This example will multiply the total value of the entity's `minecraft:generic.movement_speed` attribute by 1.5, essentially increasing the total value by 150%. 
(For example: if the total value is 0.7, the new total value will be 1.05 since `0.7 * (1 + 0.5) = 1.05`)
