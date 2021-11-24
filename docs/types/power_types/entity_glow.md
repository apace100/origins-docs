---
title: Entity Glow (Power Type)
date: 2021-04-08
---

# Entity Glow

[Power Type](../power_types.md)

Makes other entities glow (as with the glowing status effect), but only for the player that has the power.

Type ID: `origins:entity_glow`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_condition` | [Entity Condition](../entity_conditions.md) | _optional_ | If specified, only entities which fulfill this condition will glow for the player that has the power.
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, the power will only be active if this condition is fulfilled by either or both the 'actor' (the player that has the power) and 'target' (the entity that would glow) entities.
`use_teams` | [Boolean](../data_types/boolean) | `true` | Determines whether glowing entities should use their team's color with their glow. If set to false, the entity will instead use the `red`, `green` and `blue` fields within this power type.
`red` | [Float](../types/data_types/float.md) | `1.0` | Value by which the red component of the glow will be multiplied. Range: 0.0 - 1.0.
`green` | [Float](../types/data_types/float.md) | `1.0` | Value by which the green component of the glow will be multiplied. Range: 0.0 - 1.0.
`blue` | [Float](../types/data_types/float.md) | `1.0` | Value by which the blue component of the glow will be multiplied. Range: 0.0 - 1.0.

### Examples
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
This power makes all entities which are not arthropods glow when they're in cobwebs. The glow is the same color as the entity's team.
<br>

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