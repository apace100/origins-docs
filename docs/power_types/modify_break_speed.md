---
title: Modify Break Speed (Power Type)
date: 2021-04-04
---
# Modify Break Speed

[Power Type](../power_types.md).

Modifies how fast the player can break blocks.

Type ID: `origins:modify_break_speed`

### Fields

`block_condition`, [Block Condition](../block_conditions.md), optional: _If set, the modifiers will only apply to blocks which satisfy this condition._

`modifier`, [Attribute Modifier](../data_types/attribute_modifier.md), optional: _If set, this modifier will apply to the break speed._

`modifiers`, [Array](../data_types/array.md) of [Attribute Modifiers](../data_types/attribute_modifier.md), optional: _If set, these modifiers will apply to the break speed._

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
