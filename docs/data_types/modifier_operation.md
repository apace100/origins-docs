---
title: Modifier Operation (Data Type)
date: 2021-04-04
---
# Modifier Operation

[Data Type](../data_types.md).

A [String](string.md) used to specify an operation used by [Attribute Modifiers](attribute_modifier.md) and [Attributed Attribute Modifiers](attributed_attribute_modifier.md).

### Values:

Value  | Description
-------|------
`addition` | Adds (or subtracts) the modifier value to the base: NewValue = BaseValue + ModifierValue.
`multiply_base` | Adds (or subtracts) a portion of the base value: NewValue = CurrentValue + (BaseValue * ModifierValue)
`multiply_total` | Multiplies the total value by this value: NewTotalValue = TotalValue * (1 + ModifierValue)

### Examples:

```json
{
	"operation": "multiply_total"
}
```

Will multiply the total value.
<br>

```json
{
	"modifier": {
		"attribute": "reach-entity-attributes:reach",
		"operation": "addition",
		"value": -2
	}
}
```

A modifier operation used inside an [Attributed Attribute Modifier](attributed_attribute_modifier.md), which subtracts 2 blocks from the player's block reach.