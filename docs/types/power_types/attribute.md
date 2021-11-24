---
title: Attribute (Power Type)
date: 2021-04-07
---

# Attribute

[Power Type](../power_types.md)

Applies one or more attribute modifiers.

Type ID: `origins:attribute`

!!! caution

    This power type does **not** support a `condition`. If the `condition` field is present, it will be ignored. If you wish to check for an entity condition before applying the attribute modifier(s), you can use the [Conditioned Attribute](../power_types/conditioned_attribute.md) power type instead.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attributed Attribute Modifier](../types/data_types/attributed_attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to its corresponding attribute.
`modifiers` | [Array](../types/data_types/array.md) of [Attributed Attribute Modifiers](../types/data_types/attributed_attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to their corresponding attributes.
`update_health` | [Boolean](../types/data_types/boolean.md) | `true` | When true, the player's health percentage will update to match their new maximum health.

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
