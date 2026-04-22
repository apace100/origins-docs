---
title: Spawn Effect Cloud (Entity Action Type)
date: 2021-04-05
---

# Spawn Effect Cloud

[Entity Action Type](../entity_action_types.md)

Spawns an area effect cloud (as from a lingering potion) at the position of the entity.

Type ID: `origins:spawn_effect_cloud`


### Fields

| Field              | Type                                                                                          | Default    | Description                                                                                          |
| --------------------| -----------------------------------------------------------------------------------------------| ------------| ------------------------------------------------------------------------------------------------------|
| `radius`           | [Float](../data_types/float.md)                                                               | `3.0`      | The radius of the cloud.                                                                             |
| `radius_on_use`    | [Float](../data_types/float.md)                                                               | `-0.5`     | How much the radius should change when an effect is applied.                                         |
| `wait_time`        | [Integer](../data_types/integer.md)                                                           | `10`       | How many ticks to wait until the cloud takes effect.                                                 |
| `effect_component` | [Potion Contents (Component)](https://minecraft.wiki/w/Data_component_format#potion_contents) | _optional_ | If specified, this potion content component will be applied to the spawned area effect cloud entity. |


### Examples

```json
"entity_action": {
    "type": "origins:spawn_effect_cloud",
    "radius": 5.0,
    "wait_time": 20,
    "effect_component": {
        "potion": "minecraft:strong_harming"
    }
}
```
This example will spawn a small Area Effect Cloud, which will apply Instant Damage II to entities in contact with the cloud.
<br>

```json
"entity_action": {
    "type": "origins:spawn_effect_cloud",
    "radius": 10.0,
    "wait_time": 40,
    "effect_component": {
        "custom_effects": [
            {
                "id": "minecraft:poison",
                "duration": 80,
                "amplifier": 0
            },
            {
                "id": "minecraft:slowness",
                "duration": 200,
                "amplifier": 1
            }
        ]
    }
}
```
This example will spawn a big Area Effect Cloud, which will apply Poison I (that will last 3 seconds) and Slowness II (that will last 10 seconds) to entities in contact with the cloud.