---
title: Attributed Attribute Modifier (Data Type)
date: 2021-04-04
---

# Attributed Attribute Modifier

[Data Type](../data_types.md)

An [object](object.md) used to specify how the numerical value of a specific attribute should be modified.


!!! note

    Not to be confused with [Attribute Modifier](attribute_modifier.md), which do not use vanilla's attribute modifier system.


### Fields

| Field       | Type                                                                                  | Default | Description                                                      |
| -------------| ---------------------------------------------------------------------------------------| ---------| ------------------------------------------------------------------|
| `attribute` | [Identifier](identifier.md)                                                           |         | The ID of the attribute which will be modified by this modifier. |
| `operation` | [Attributed Attribute Modifier Operation](attributed_attribute_modifier_operation.md) |         | The operation will be performed by this modifier.                |
| `amount`    | [Float](float.md)                                                                     |         | The amount to be used for the modifier operation.                |
| `id`        | [Identifier](identifier.md)                                                           |         | The identifier of the modifier, describing where it comes from.  |


### Examples

```json
"modifier": {
    "attribute": "minecraft:generic.attack_damage",
    "operation": "addition",
    "amount": 9,
    "id": "example:additional_attack_damage"
}
```
This example will add `9.0` to the base value of the entity's `minecraft:generic.attack_damage` attribute.
(For example: if the current base value is 1, the new base value will be 10 since `1 + 9 = 10`)
<br>

```json
"modifier": {
    "attribute": "minecraft:generic.max_health",
    "operation": "multiply_base",
    "amount": 2,
    "id": "example:heavy_heart"
}
```
This example will add the base value multiplied by the modifier value to the current base value of the entity's `minecraft:generic.max_health` attribute.
(For example: if the current base value is 20, the new base value will be 60 since `20 + (20 * 2) = 60`)
<br>

```json
"modifier": {
    "attribute": "minecraft:generic.movement_speed",
    "operation": "multiply_total",
    "amount": 0.5,
    "id": "example:swift"
}
```
This example will multiply the total value of the entity's `minecraft:generic.movement_speed` attribute by 1.5, essentially increasing the total value by 50%. 
(For example: if the total value is 0.7, the new total value will be 1.05 since `0.7 * (1 + 0.5) = 1.05`)
