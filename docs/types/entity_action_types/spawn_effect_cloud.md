---
title: Spawn Effect Cloud (Entity Action Type)
date: 2021-04-05
---

# Spawn Effect Cloud

[Entity Action Type](../entity_action_types.md)

Spawns an area effect cloud (as from a lingering potion) at the position of the entity.

Type ID: `origins:spawn_effect_cloud`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`radius` | [Float](../data_types/float.md) | `3` | The radius of the cloud.
`radius_on_use` | [Float](../data_types/float.md) | `-0.5` | How much the radius should change when an effect is applied.
`wait_time` | [Integer](../data_types/integer.md) | `10` | How many ticks to wait until the cloud takes effect.
`effect` | [Status Effect Instance](../data_types/status_effect_instance.md) | _optional_ | If specified, this status effect will be applied by the cloud to entities inside of it.
`effects` | [Array](../data_types/array.md) of [Status Effect Instances](../data_types/status_effect_instance.md) | _optional_ | If specified, these status effects will be applied by the cloud to entities inside of it.


### Examples

```json
"entity_action": {
    "type": "origins:spawn_effect_cloud",
    "radius": 10.0,
    "wait_time": 40,
    "effect": {
        "effect": "minecraft:resistance",
        "amplifier": 3,
        "duration": 100
    }
}
```

This example will spawn a large Area Effect Cloud, which provides the Resistance IV status effect that will last for 5 seconds at the entity's position.
