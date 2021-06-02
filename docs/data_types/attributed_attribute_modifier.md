---
title: Attributed Attribute Modifier (Data Type)
date: 2021-04-04
---
# Attributed Attribute Modifier

[Data Type](../data_types.md).

An [Object](object.md) used to specify how a specific attribute should be modified. Basically an [Attribute Modifier](attribute_modifier.md) with an additional `attribute` field.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`attribute` | [Identifier](identifier.md) | | ID of the attribute which will be modified by this modifier.
`operation` | [Modifier Operation](modifier_operation.md) | | The operation which will be performed by this modifier.
`value` | [Float](float.md) | | The value with which to apply the operation to the value.
`name` | [String](string.md) | _optional_ | A descriptive name for the modifier, describing where it comes from.

### Example:

```json
{
	"modifier": {
		"attribute": "minecraft:generic.attack_speed",
		"operation": "multiply_total",
		"value": -0.25
	}
}
```

This modifier reduces the total attack speed of the player by 25%.