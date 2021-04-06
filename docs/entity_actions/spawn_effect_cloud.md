---
title: Spawn Effect Cloud (Action)
date: 2021-04-05
---
# Spawn Effect Cloud

[Entity Action](../entity_actions.md).

Spawns an effect cloud (as from a lingering potion) at the position of the entity.

Type ID: `origins:spawn_effect_cloud`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`radius` | [Float](../data_types/float.md) | `3` | The radius of the cloud.
`radius_on_use` | [Float](../data_types/float.md) | `-0.5` | How much the radius should change when an effect is applied.
`wait_time` | [Integer](../data_types/integer.md) | `10` | How many ticks to wait until the cloud takes effect.
`effect` | [Status Effect Instance](../data_types/status_effect_instance.md) | _optional_ | If set, this status effect will be applied by the cloud to entities inside of it.
`effects` | [Array](../data_types/array.md) of [Status Effect Instance](../data_types/status_effect_instance.md) | _optional_ | If set, these status effects will be applied by the cloud to entities inside of it.

### Example
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
This action spawns a large effect cloud, which provides a Resistance IV effect, at the entity position.
