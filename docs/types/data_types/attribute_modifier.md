---
title: Attribute Modifier (Data Type)
date: 2021-04-04
---

# Attribute Modifier

[Data Type](../data_types.md)

An [Object](object.md) used to specify how a value should be modified.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`operation` | [Attribute Modifier Operation](attribute_modifier_operation.md) | | The operation which will be performed by this modifier.
`value` | [Float](float.md) | | The value to use for the modifier operation.
`resource` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, the value of this power will be used instead of the value specified in the `value` field.
`name` | [String](string.md) | _optional_ | A descriptive name for the modifier, describing where it comes from.
`modifier` | [Attribute Modifier](attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the value of the modifier.


### Examples

```json
"modifier": {
    "operation": "add_base_early",
    "value": 9
}
```

This example will add `9.0` to the base value.
(For example: if the current base value is 6.0, the new base value will be 15 since `6 + 9 = 15`)
<br>

```json
"modifier": {
    "operation": "multiply_base_additive",
    "value": 2
}
```

This example will add the base value multiplied by the modifier value to the current base value.
(For example: if the current base value is 5, the new base value will be 15 since `5 + (5 * 2) = 15`)
<br>

```json
"modifier": {
    "operation": "multiply_total_multiplicative",
    "value": 0.25
}
```

This example will multiply the total value by 1.25, essentially increasing the total value by 125%.
(For example: if the current total value is 30, the new total value will be 37.5 since `30 * (1 + 0.25) = 37.5`)
<br>

```json
"modifier": {
    "operation": "add_base_early",
    "resource": "example:resource",
    "value": 0
}
```

This example will add the value of the `example:resource` (`data/example/powers/resource.json`) power to the base value.
(For example: if the current base value is 20.0 and the value of the `example:resource` power is 10, the new base value will be 30.0 since `20.0 + 10 = 30`)
<br>

```json
"modifier": {
    "operation": "add_base_early",
    "resource": "example:resource",
    "value": 0,
    "modifier": {
        "operation": "multiply_total_multiplicative",
        "value": -0.999
    }
}
```

This example will add the value of the `example:resource` (`data/example/powers/resource.json`) power to the base value of the modifier and multiply it by 0.01.
(For example: if the current base value is 0.1 and the value of the `example:resource` power is 25, the new base value will be 0.125 since `0.1 + (25 * (1 - 0.999)) = 0.125`)
