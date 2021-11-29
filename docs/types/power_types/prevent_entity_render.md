---
title: Prevent Entity Render (Power Type)
date: 2021-04-07
---

# Prevent Entity Render

[Power Type](../power_types.md)

Prevents an entity from being rendered to the entity that has the power, including their armor, shadow, and hitboxes.

Type ID: `origins:prevent_entity_render`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified, only entities which fulfills this condition will be affected.


### Examples

```json
{
    "type": "origins:prevent_entity_render",
    "entity_condition": {
		"type": "origins:entity_type",
		"entity_type": "minecraft:creeper"
	},
	"condition": {
		"type": "origins:daytime"
	}
}
```

This example will make creepers invisible for the player that has the power during the day.
