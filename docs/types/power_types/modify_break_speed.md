---
title: Modify Break Speed (Power Type)
date: 2021-04-04
---

# Modify Break Speed

[Power Type](../power_types.md)

Modifies how fast the player can break blocks.

Type ID: `origins:modify_break_speed`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](../block_conditions.md) | _optional_ | If specified, the modifier(s) will only apply to the blocks that fulfills this condition.
`modifier` | [Attribute Modifier](../types/data_types/attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to the break speed.
`modifiers` | [Array](../types/data_types/array.md) of [Attribute Modifiers](../types/data_types/attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to the break speed.

### Example
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
This power allows the player to break Netherrack 50% faster than usual.
