---
title: Attribute (Power Type)
date: 2021-04-07
---

# Attribute

[Power Type](../power_types.md)

Modifies one or more attributes using [Attributed Attribute Modifiers](../data_types/attributed_attribute_modifier.md)

Type ID: `origins:attribute`

!!! caution

    This power type does **not** support a `condition`. If the `condition` field is present, it will be ignored. If you wish to check for an entity condition before applying the attribute modifier(s), you can use the [Conditioned Attribute](../power_types/conditioned_attribute.md) power type instead.

!!! note

    Refer to the [Minecraft Wiki: Attribute](https://minecraft.wiki/w/Attribute) page for a list of **vanilla** attributes that you can modify.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attributed Attribute Modifier](../data_types/attributed_attribute_modifier.md) | _optional_ | If specified, this modifier will be applied to its corresponding attribute.
`modifiers` | [Array](../data_types/array.md) of [Attributed Attribute Modifiers](../data_types/attributed_attribute_modifier.md) | _optional_ | If specified, these modifiers will be applied to their corresponding attributes.
`update_health` | [Boolean](../data_types/boolean.md) | `true` | When true, the player's health percentage will update to match their new maximum health.


### Examples

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

This example will increase the entity's maximum health by 2 hearts.
