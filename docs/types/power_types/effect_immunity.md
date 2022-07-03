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
`effect` | [Identifier](../data_types/identifier.md) | _optional_ | If specified, only the status effect with this namespace and ID can not be applied to the entity that has the power.
`effects` | [Array](../data_types/array.md) of [Identifiers](../data_types/identifier.md) | _optional_ | If specified, only the status effects with the specified namespace and IDs can not be applied to the entity that has the power.
`inverted` | [Boolean](../data_types/boolean.md) | `false` | Determines whether to make the entity immune to the status effect(s) that aren't specified.


### Examples

```json
{
	"type": "origins:effect_immunity",
	"effects": [
		"minecraft:weakness",
		"minecraft:strength"
	]
}
```

This example will make the entity immune to the Weakness and Strength status effects.
