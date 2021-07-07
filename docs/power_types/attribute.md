---
title: Attribute (Power Type)
date: 2021-04-07
---
# Attribute

[Power Type](../power_types.md).

Applies one or more attribute modifiers. Does *NOT* support a `condition`, use [Conditioned Attribute](../power_types/conditioned_attribute.md) instead if you need one.

Type ID: `origins:attribute`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attributed Attribute Modifier](../data_types/attributed_attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to its corresponding attribute.
`modifiers` | [Array](../data_types/array.md) of [Attributed Attribute Modifiers](../data_types/attributed_attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to their corresponding attributes.
`update_health` | [Boolean](../data_types/boolean.md) | true | When true, the player's health percentage will update to match their new maximum health.

### Example
```json
{
	"type": "origins:attribute",
	"modifier": {
		"name": "Max health increase",
		"attribute": "minecraft:generic.max_health",
		"value": 4,
		"operation": "addition"
	}
}
```
This power would increase the player's maximum health by 4 (two hearts).
