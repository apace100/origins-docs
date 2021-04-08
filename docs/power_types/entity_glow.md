---
title: Entity Glow (Power Type)
date: 2021-04-08
---
# Entity Glow

[Power Type](../power_types.md).

Other entities will appear as if they glow (as with the glowing status effect), but only for the player with this power.

Type ID: `origins:entity_glow`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If set, only entities which fulfill this condition will glow for the player with this power.

### Example
```json
{
	"type": "origins:entity_glow",
    "entity_condition": {
      	"type": "origins:and",
      	"conditions": [
        	{
          		"type": "origins:in_block_anywhere",
          		"block_condition": {
            		"type": "origins:in_tag",
            		"tag": "origins:cobwebs"
          		}
        	},
        	{
          		"type": "origins:entity_group",
          		"group": "arthropod",
          		"inverted": true
        	}
      	]
    }
}
```
This power makes all entities which are not arthropods glow when they're in cobwebs.
