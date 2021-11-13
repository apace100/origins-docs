---
title: Effect Immunity (Power Type)
date: 2021-04-07
---

# Effect Immunity

[Power Type](../power_types.md)

Prevents status effects from being applied to the entity that has the power.

Type ID: `origins:effect_immunity`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [Identifier](../data_types/identifier.md) |  | If specified, the status effect with this namespace and ID can not be applied to the entity that has the power.
`effects` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) |  | If specified, the status effects with the specified namespace and IDs can not be applied to the entity that has the power.

### Example
```json
{
	"type": "origins:effect_immunity",
	"effects": [
		"minecraft:weakness",
		"minecraft:strength"
	]
}
```
This power would make the player immune to the weakness and strength potion effects.
