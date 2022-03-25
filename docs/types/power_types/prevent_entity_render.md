---
title: Prevent Entity Render (Power Type)
date: 2021-04-07
---

# Prevent Entity Render

[Power Type](../power_types.md)

Prevents an entity from being rendered to the entity that has the power, including their armor, shadow, and hitboxes.

Type ID: `apoli:prevent_entity_render`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_condition` | [Entity Condition Type](../entity_condition_types.md) | _optional_ | If specified, only entities which fulfills this condition will be affected.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | _optional_ | If specified, the power will only be active if this condition is fulfilled by either or both the 'actor' (the player that has the power) and 'target' (the entity that will not render) entities.


### Examples

```json
{
    "type": "apoli:prevent_entity_render",
    "entity_condition": {
		"type": "apoli:entity_type",
		"entity_type": "minecraft:creeper"
	},
	"condition": {
		"type": "apoli:daytime"
	}
}
```

This example will make creepers invisible for the player that has the power during the day.
<br>

```json
{
    "type": "apoli:prevent_entity_render",
    "bientity_condition": {
        "type": "apoli:and",
        "conditions": [
            {
                "type": "apoli:distance",
                "comparison": ">",
                "compare_to": 8
            },
            {
                "type": "apoli:target_condition",
                "condition": {
                    "type": "apoli:entity_group",
                    "group": "aquatic"
                }
            }
        ]
    },
    "condition": {
        "type": "apoli:submerged_in",
        "fluid": "minecraft:water"
    }
}
```

This example will prevent mobs that are from the 'aquatic' entity group from rendering for the entity that has the power only if the entity that has the power is submerged in water and those mobs are 9 or more blocks away.
