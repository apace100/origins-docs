---
title: Prevent Death (Power Type)
date: 2021-04-07
---

# Prevent Death

[Power Type](../power_types.md)

Prevents death; any damage which would kill the entity that has the power will instead reduce their health to half a heart.

Type ID: `origins:prevent_death`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`damage_condition` | [Damage Condition Type](../damage_condition_types.md) | _optional_ | If specified, death will only be prevented if the damage dealt to the entity fulfills this condition.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | If specified, this action will be executed on the entity when death is prevented.


### Examples

```json
{
    "type": "origins:prevent_death",
    "entity_action": {
		"type": "origins:and",
		"actions": [
			{
				"type": "origins:clear_effect"
			},
			{
				"type": "origins:apply_effect",
				"effects": [
					{
						"effect": "minecraft:regeneration",
						"amplifier": 1,
						"duration": 900
					},
					{
						"effect": "minecraft:fire_resistance",
						"duration": 800
					},
					{
						"effect": "minecraft:absorption",
						"amplifier": 1,
						"duration": 100
					}
				]
			}
		]
	}
}
```

This example will always prevent the entity from dying and then apply the same effects as a Totem of Undying, e.g: clear all status effects on the entity an then apply Regeneration II, Fire Resistance I and Absorption I.
