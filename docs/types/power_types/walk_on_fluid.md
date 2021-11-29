---
title: Walk On Fluid (Power Type)
date: 2021-04-08
---

# Walk On Fluid

[Power Type](../power_types.md)

Allows the entity that has the power to walk on fluid.

Type ID: `origins:walk_on_fluid`

!!! note

    It is suggested to use the [Fluid Height (Entity Condition Type)](../entity_condition_types/fluid_height.md) entity condition type to check if the height of the fluid the player is currently on/in is less or equal to 0.4, otherwise, the entity that has the power may have problems getting out of the fluid once they are submerged.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`fluid` | [Identifier](../data_types/identifier.md) | | The namespace and ID of the fluid tag on which the player should be able to walk onto. Most important examples: `minecraft:water` and `minecraft:lava`.


### Examples

```json
{
  	"type": "origins:walk_on_fluid",
  	"fluid": "minecraft:lava",
  	"condition": {
    	"type": "origins:fluid_height",
    	"fluid": "minecraft:lava",
    	"comparison": "<=",
    	"compare_to": 0.4
  	}
}
```

This example will allow the entity that has the power to walk on lava similar to Striders. The suggested condition was added to allow the entity to swim in lava once they sink, which may happens when they walk into a Lava-fall.
