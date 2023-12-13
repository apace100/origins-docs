---
title: Modify Break Speed (Power Type)
date: 2021-04-04
---

# Modify Break Speed

[Power Type](../power_types.md)

Modifies how fast the player that has the power can break blocks.

Type ID: `origins:modify_break_speed`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | *optional* | If specified, the modifier(s) will only apply to the blocks that fulfills this condition.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | *optional* | If specified, this modifier will be applied to the break speed.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | *optional* | If specified, these modifiers will be applied to the break speed.
`hardness_modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | *optional* | If specified, this modifier will be applied to the *effective* hardness value of the block while calculating the block's break speed.
`hardness_modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | *optional* | If specified, these modifiers will be applied to the *effective* hardness value of the block while calculating the block's break speed.


### Examples

```json
{
	"type": "origins:modify_break_speed",
	"block_condition": {
		"type": "origins:block",
		"block": "minecraft:netherrack"
	},
	"modifier": {
		"operation": "multiply_base",
		"value": 0.5
	}
}
```

This example will allow the player to break Netherrack 50% faster than usual.
<br>

```json
{
	"type": "origins:modify_break_speed",
	"modifier": {
		"operation": "multiply_base",
		"value": -0.9
	},
	"hardness_modifiers": [
		{
			"operation": "max_total",
			"value": -1.0
		},
		{
			"operation": "min_total",
			"value": 0.1
		}
	]
}
```

This example will make the player break blocks 90% slower than usual, which also applies to blocks that can be mined instantly (which is handled by assigning a minimum value of `0.1` if the hardness value of the block is `0`, which is the case for such blocks.)
