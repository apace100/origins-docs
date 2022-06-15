---
title: Attribute Modifier (Data Type)
date: 2021-04-04
---

# Attribute Modifier

[Data Type](../data_types.md)

An [Object](object.md) used to specify how an attribute should be modified.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`operation` | [Modifier Operation](modifier_operation.md) | | The operation which will be performed by this modifier.
`value` | [Float](float.md) | | The value with which to apply the operation to the value.
`resource` | [Identifier](../data_types/identifier.md) | _optional_ | The namespace and ID of a resource power. If specified, the value of the designated `resource` will be added onto the `value` field.
`name` | [String](string.md) | _optional_ | A descriptive name for the modifier, describing where it comes from.


### Examples

```json
"modifier": {
    "operation": "multiply_base",
    "value": 1
}
```

This attribute modifier will multiply the base value by 2, stacking additively with other `multiply_base` operations on the same value.
<br>

```json
"modifier": {
	"operation": "multiply_total",
	"value": -1
}
```

This attribute modifier will multiply the total value by 0.
