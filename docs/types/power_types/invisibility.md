---
title: Invisibility (Power Type)
date: 2021-04-08
---

# Invisibility

[Power Type](../power_types.md)

Grants the entity that has the power invisibility; may or may not affect their worn armor.

Type ID: `origins:invisibility`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`render_armor` | [Boolean](../data_types/boolean.md) | `false` | Determines whether armor should be shown or not.
`render_outline` | [Boolean](../data_types/boolean.md) | `false` | Determines whether the glowing outline should be shown or not.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the '**target**' will only be invisible to '**actors**' (either the player or mobs that may see the target) if the bi-entity condition is fulfilled by either or both of them.


### Examples

```json
{
  	"type": "origins:invisibility",
	"render_armor": false,
	"condition": {
		"type": "origins:on_fire",
		"inverted": true
	}
}
```

This example will make the entity that has the power invisible if the entity is not burning, even hiding the armor.
