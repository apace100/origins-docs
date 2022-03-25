---
title: Modify Break Speed (Power Type)
date: 2021-04-04
---

# Modify Break Speed

[Power Type](../power_types.md)

Modifies how fast the player that has the power can break blocks.

Type ID: `apoli:modify_break_speed`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the modifier(s) will only apply to the blocks that fulfills this condition.
`modifier` | [Attribute Modifier](../data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the break speed.
`modifiers` | [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the break speed.


### Examples

```json
{
	"type": "apoli:modify_break_speed",
	"block_condition": {
		"type": "apoli:block",
		"block": "minecraft:netherrack"
	},
	"modifier": {
		"operation": "multiply_base",
		"value": 0.5
	}
}
```

This example will allow the player to break Netherrack 50% faster than usual.
