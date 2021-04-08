---
title: Walk On Fluid (Power Type)
date: 2021-04-08
---
# Walk On Fluid

[Power Type](../power_types.md).

Allows the player to walk on a given fluid.

**Note:** a condition which checks for the height of said fluid to be below or equal to 0.4 is suggested, as otherwise the player will have problems getting out of the fluid once they are submerged.

Type ID: `origins:walk_on_fluid`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`fluid` | [Identifier](../data_types/identifier.md) | | ID of the fluid tag on which the player should be able to walk. Most important examples: `minecraft:water` and `minecraft:lava`.

### Example
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
With this power, players are able to walk on lava similar to Striders. The suggested condition was added to allow them to swim in lava once they sink (which happens e.g. when they walk into a lavafall).
