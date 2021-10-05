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
`bientity_condition` | [Bi-entity Condition](../bientity_conditions) | _optional_ | If set, only entities which fulfill this bi-entity condition in relation to the power holder will glow for the player with this power.
`use_teams` | [Boolean](../data_types/boolean) | `true` | Whether glowing entities should use their team's color with their glow. If set to false the entity will instead use the `red`, `green` and `blue` fields within this power type.
`red` | [Float](../data_types/float.md) | 1.0 | Value by which the red component of the glow will be multiplied. Range: 0 - 1.
`green` | [Float](../data_types/float.md) | 1.0 | Value by which the green component of the glow will be multiplied. Range: 0 - 1.
`blue` | [Float](../data_types/float.md) | 1.0 | Value by which the blue component of the glow will be multiplied. Range: 0 - 1.

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
This power makes all entities which are not arthropods glow when they're in cobwebs. The glow is the same colour as the entity's team.

```json
{
	"type": "origins:entity_glow",
    "bientity_condition": {
		"type": "origins:can_see"
	},
	"use_teams": false,
	"red": 0.0,
	"green": 1.0,
	"blue": 0.0
}
```
This power makes all entities that the player is able to see glow with a green glow.