---
title: Area of Effect (Entity Action Type)
date: 2021-12-03
---

# Area of Effect

[Entity Action Type](../entity_action_types.md)

Executes a [Bi-Entity Action](../bientity_action_types.md) within a specified radius.

Type ID: `origins:area_of_effect`


!!! note

    In the context of this entity action type, the '**actor**' is the entity that invoked the action and the '**target(s)**' is/are the entity/entities within the specified radius.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`radius` | [Float](../data_types/float.md) | `16.0` | Determines the radius of the area.
`shape` | [Shape](../data_types/shape.md) | `"cube"` | Determines the shape of the area.
`bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | | The bi-entity action to execute on either or both the '**actor**' or the '**target(s)**'.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | *optional* | If specified, the specified bi-entity action will only be executed on either or both the '**actor**' or '**target(s)**' that fulfill this bi-entity condition.
[`include_actor`](## "Aliases: ["include_target"]") | [Boolean](../data_types/boolean.md) | `false` | Determines whether the '**actor**' should be included as a target.


### Examples

```json
"entity_action": {
    "type": "origins:area_of_effect",
    "radius": 10,
    "shape": "sphere",
    "bientity_action": {
        "type": "origins:target_action",
        "action": {
            "type": "origins:spawn_entity",
            "entity_type": "minecraft:lightning_bolt"
        }
    }
}
```

This example will summon a lightning bolt on entities within a 10 block spherical radius.
<br>

```json
"entity_action": {
    "type": "origins:area_of_effect",
    "radius": 32,
    "bientity_action": {
        "type": "origins:target_action",
        "action": {
            "type": "origins:set_on_fire",
            "duration": 5
        }
    },
    "bientity_condition": {
        "type": "origins:can_see"
    }
}
```

This example will set entities within a 32 block radius on fire for 5 seconds if the entities that are within the radius can be "seen" by the entity that invoked the action.
