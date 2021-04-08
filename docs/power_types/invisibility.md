---
title: Invisibility (Power Type)
date: 2021-04-08
---
# Invisibility

[Power Type](../power_types.md).

Turns the player (and optionally their armor) invisible.

Type ID: `origins:invisibility`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`render_armor` | [Boolean](../data_types/boolean.md) | | Whether or not the player's armor should be shown.

### Example
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
Makes the player invisible if they're not burning, even hiding the armor.
