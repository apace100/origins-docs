---
title: Prevent Entity Render (Power Type)
date: 2021-04-07
---
# Prevent Entity Render

[Power Type](../power_types.md).

Completely prevents a player with this power to see an entity. This will also hide armor, the shadow, and even the hitboxes (which would be shown when F3+B was used).

Type ID: `origins:prevent_entity_render`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If set, only entities which fulfill this condition will be invisible.

### Example
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
This power makes creepers invisible for the player during day.
